---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Review product work

Reviews work in this space as a product teammate, not as a linter: the evidence, the reasoning and the hygiene, with the smallest fix for each finding. It reports, and changes nothing unless the person asks for the fixes.

## When to run this

- Before a spec or a strategy thesis is shared.
- When someone asks: "review this spec", "check the evidence behind this", "is this ready to share?".

## Steps

1. **Understand the scope.** Read the files that changed, or ask what to review. Say what kind of work it is: capture, synthesis, discovery, strategy, a spec, competitor research or a change of structure. Run only the checks that apply.
2. **Run the checks.**
   - **Source fidelity,** for feedback and interviews: quotes are verbatim or labelled as paraphrases; the person, the company, the date and the source are not guessed; context never passes for the source's own words.
   - **Synthesis discipline,** for painpoints and requests: each has valid `source_files`; a recurring painpoint has two independent sources, or one blocking interview that says so; the same job is updated rather than split into near-identical files; the scores match the evidence and don't pretend to be roadmap priority.
   - **Product reasoning:** a discovery file frames an open question rather than hiding a preferred answer; a strategy thesis has evidence and credible counter-arguments; a spec traces to its evidence, names its audience, defines measurable success and says what it won't do; a claim about a competitor cites a primary source and keeps fact apart from inference.
   - **Roadmap boundary:** initiatives, projects, tasks, status, owners and delivery dates stay in the tracker named in [`company/tools.md`](../../../company/tools.md); the space links to them rather than rebuilding them.
   - **Hygiene:** relative links resolve; a new file is listed where its folder keeps a list; a full page has the frontmatter in [the workspace's file conventions](../../../.agents/conventions.md); dates are absolute and attribution names a person; a bracket left in a real page is an open question on purpose, not a slot someone forgot.
   - **Dashboard:** when feedback changed, the dashboard was rebuilt and shows the source.
   - **Data boundaries:** customer names, quotes and source links suit everyone who reads the space; secrets, restricted raw exports and needless private details stayed in their source; anonymised or summarised material says so.
3. **Report,** blocking issues first, then important improvements. For each one: the file, the problem, the evidence or the rule, and the smallest useful fix. Skip the checks that don't apply. If nothing material is wrong, say "No issues found."
4. **Fix only on request.** When the person asks for the fixes, make the ones they named and say what changed.

## Done when

- Every finding names its file, its problem and its fix, or the report says "No issues found."
