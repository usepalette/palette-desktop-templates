---
description: Add a new competitor to this project's market landscape.
---

Add a new competitor to the project's market landscape.

The user will give you a competitor name (and optionally a URL or short
positioning hint). You should:

1. Find the market folder — look for `landscape.md` under
   `gtm/foundations/market/` or wherever the project keeps it. If you
   can't find one, ask the user where the market docs live.
2. Use the `competitor-research` skill to gather a profile.
3. Write the profile to `<market>/competitors/<slug>.md` using the
   shape of existing profiles in that folder (read one first). If the
   folder is empty, fall back to the `competitors/_template.md` shape
   that came with the workflow.
4. Update `<market>/landscape.md` — add the competitor to the
   appropriate tier in the tier table, and to the threat assessment if
   warranted.
5. Summarize what you wrote and link to the new file.

Don't overwrite an existing profile without asking.
