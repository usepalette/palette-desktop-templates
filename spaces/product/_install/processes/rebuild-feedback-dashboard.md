---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Rebuild the feedback dashboard

Rebuilds the data in `user-feedback/index.html` from the markdown beside it. The markdown is the source of truth and the page only shows it, so the data is never edited by hand. The page's HTML, style and script never change.

## When to run this

- After feedback, an interview, a request or a painpoint is added, changed or removed. The other feedback processes run it as their last step.
- When someone asks: "rebuild the feedback dashboard", "update the dashboard".

## Steps

1. **Collect the entries.** Read the markdown in `user-feedback/feedback/`, `user-feedback/user-interviews/`, `user-feedback/feature-requests/` and `user-feedback/painpoints/`. Skip each `README.md` and each mold.
2. **Check access before anything goes in.** The page can be shared as one file, so everything copied into it reaches whoever reads the page, not only the readers of the source. For each source, check that the page's readers may see it; anonymise or summarise restricted names, companies and quotes; and leave out private transcripts and any source whose access you can't check. `people`, `companies`, `source_url`, `summary` and `details` are the fields that leak: treat them as the gate.
3. **Make one item per entry:**

   ```json
   {
     "kind": "feedback | interview | feature-request | painpoint",
     "file": "feedback/YYYY-MM-DD_company_person_topic.md",
     "date": "YYYY-MM-DD",
     "title": "Short title",
     "people": ["Full name"],
     "companies": ["Company"],
     "tags": ["tag"],
     "summary": "Primary section text",
     "details": "Supporting context",
     "source_count": 1,
     "source_url": "https://example.com/original",
     "capture_mode": "verbatim | paraphrase | summary",
     "sentiment": "positive | neutral | negative | mixed",
     "priority_signal": "low | medium | high",
     "severity": "low | medium | high",
     "frequency": "occasional | recurring | blocking"
   }
   ```

   Include an optional field only when the entry has it. `file` is the path from `user-feedback/`, inside one of its four folders, such as `feedback/<file>.md`. `source_url` must be an `http` or `https` address: leave out `unavailable` and anything malformed.

   | Kind | Taken from |
   |---|---|
   | Feedback | The person, company, tags, sentiment, source link and capture mode from the frontmatter; `summary` from `## Feedback`, `details` from `## Context` |
   | Interview | The same as feedback, with `kind` set to `interview` |
   | Feature request | The person from `requested_by`; `summary` from `## Request`, `details` from `## Why they want it` and `## Evidence`; `source_count` from `source_files` |
   | Painpoint | `companies` from the frontmatter; `summary` from `## Painpoint`, `details` from `## Evidence` and `## Impact`; `source_count` from `source_files` |

   The title is the first `#` heading, or a readable version of the file name. A missing date comes from the file name only when it starts with `YYYY-MM-DD`. Sort the items by date, newest first, then by company and title.
4. **Build the JSON:** an object with `updated` set to today's date and `items` holding the list. Print it with two-space indentation and valid JSON escaping. Then make it safe to sit inside the page without changing the values it parses to:
   - replace every literal `<` with `<`, every `>` with `>` and every `&` with `&`
   - escape U+2028 and U+2029 if the serialiser leaves them literal

   Valid JSON is not enough on its own: text from a source that contains `</script>` must never be able to close the data block.
5. **Replace only the data block.** In `user-feedback/index.html`, find the one block that runs from the `FEEDBACK_DATA_START` comment to the `FEEDBACK_DATA_END` comment, around the `feedback-data` script:

   ```html
   <!-- FEEDBACK_DATA_START -->
   <script id="feedback-data" type="application/json">
   ...
   </script>
   <!-- FEEDBACK_DATA_END -->
   ```

   Replace that whole block with the new JSON inside the same markers and script tag. Change nothing around it. If either marker is missing or appears more than once, stop and say so.
6. **Check the result.**
   - The two markers and the `feedback-data` script each appear exactly once.
   - The script's text parses as JSON.
   - No literal `<`, `>` or `&` is left inside the JSON text.
   - Every `file` is inside one of the four folders, and every `source_url` is an `http` or `https` address.
   - The page's own script still parses.
7. **Say what you did:** the number of items of each kind, the path `user-feedback/index.html`, and that the data passed the checks.

## Done when

- The data block holds one item for every entry the page's readers may see, and nothing else on the page changed.
- Every check in step 6 passes.
