---
name: resolve-pr-comments
description: Fetch and resolve PR review comments from GitHub. Use when iterating on PR feedback from reviewers or bots.
---

Resolve PR review comments for the current branch.

## Arguments

- `--auto` — Skip user acknowledgement and execute all recommendations automatically. Use when running in a loop (e.g., "keep iterating until PR is approved").

## Setup

- Get PR number: `gh pr view --json number -q .number`
- Get owner/repo: `gh repo view --json owner,name -q '"\(.owner.login)/\(.name)"'`

## Steps

1. **Fetch unresolved comments**: Use the GraphQL API to get only unresolved review threads (REST API doesn't support filtering by resolved status):
   ```
   gh api graphql -f query='{
     repository(owner: "{owner}", name: "{repo}") {
       pullRequest(number: {number}) {
         reviewThreads(first: 100) {
           nodes {
             isResolved
             comments(first: 5) {
               nodes {
                 databaseId
                 body
                 path
                 line
                 author { login }
               }
             }
           }
         }
       }
     }
   }'
   ```
   Filter to threads where `isResolved == false`.

2. **Show overview**: Present a summary table for the user to review. For each comment:
   - **Author** | **File:Line** | **Summary** (1-line) | **Recommendation** (Fix / Skip / Reply) | **Link**
   - Include a direct link to each comment (format: `https://github.com/{owner}/{repo}/pull/{number}#discussion_r{comment_id}`)
   - For "Skip" recommendations, include a brief reason why
   - For "Reply" recommendations (e.g., questions), include the proposed answer
   - Group by file for readability

3. **Wait for user acknowledgement** (skip if `--auto`): Do NOT start fixing or replying until the user confirms the plan. The user may override recommendations. In `--auto` mode, proceed immediately with all recommendations.

4. **Execute the plan**: For each comment based on the agreed plan:

   **Fix**: Make the code change, then reply on the comment:
   ```
   gh api repos/{owner}/{repo}/pulls/{number}/comments/{comment_id}/replies -f body="Fixed. — Authored by Claude"
   ```

   **Skip (won't fix)**: Reply with the reason:
   ```
   gh api repos/{owner}/{repo}/pulls/{number}/comments/{comment_id}/replies -f body="Not fixing because: {reason} — Authored by Claude"
   ```

   **Reply (answer question)**: Reply with the answer:
   ```
   gh api repos/{owner}/{repo}/pulls/{number}/comments/{comment_id}/replies -f body="{answer} — Authored by Claude"
   ```

5. **Show results**: After executing all actions, present an updated summary with a link to each reply posted (format: `https://github.com/{owner}/{repo}/pull/{number}#discussion_r{reply_id}` — get the reply ID from the API response).

6. **Verify & push**: After all fixes, run `/check` to verify locally, then commit and push using `gt submit --stack --no-edit` (for Graphite stacks) or `git push` (for standalone branches).

## Notes

- All GitHub comment replies MUST end with " — Authored by Claude"
- Never dismiss or resolve review threads — let the reviewer do that
- For bot comments (CodeRabbit), prioritize bugs/vulnerabilities, skip low-priority style nits unless trivial to fix
