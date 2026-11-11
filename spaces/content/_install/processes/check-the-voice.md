---
type: process
owner: "[Owner]"
status: active
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
cadence: ""
---

# Check the voice

Reads a piece against the company's voice and lists what doesn't sound like us, each flag quoting the line on the voice page it breaks, with a fix. It runs before a piece goes to review, and whenever someone asks.

## When to run this

- Someone asks "does this sound like us?" or "check this against our voice", or pastes a draft for a voice check.
- A piece is about to go to review, or to go out.

## Steps

1. **Read the piece and the voice.** The piece, its channel and who it goes out as. Then [`company/brand/voice.md`](../../../company/brand/voice.md), and [`company/brand/messaging.md`](../../../company/brand/messaging.md) for how we describe ourselves. For a piece under a person's name, their `people/<name>/tone-of-voice.md` comes first and the company voice sits under it.
2. **Say what the check stands on.** If the voice page still says **Not filled in yet**, say so in one line, check against the five questions below and the principles in [`playbooks/content.md`](../playbooks/content.md) instead, and offer to fill the voice page in, following its own box. Never present a guess as the company's voice. A voice page that says **Not confirmed yet** can be used; say that its lines are not confirmed.
3. **Ask the five questions** of the whole piece:
   1. Would I say this to a smart friend over coffee?
   2. Is there a specific outcome or example?
   3. Could a competitor say the same thing? If yes, it is too generic.
   4. Am I leading with the problem or the product?
   5. Would a sceptic roll their eyes? If yes, dial it back.
4. **Go through it line by line.** Flag, quoting the line from the piece:
   - hype, corporate language or consulting-speak
   - a word or phrase the voice page lists under **We avoid**
   - a vague claim with no specifics, or a pile of adjectives
   - feature soup: capabilities listed where a workflow or an outcome should be
   - anything that goes against the voice, or against how the messaging describes us
   - a number, quote or name with no source under the piece's **Notes**
5. **Quote what each flag breaks, and suggest a fix.** For every flag, quote the line on the voice page it breaks, or the line in the person's tone of voice, then give the rewritten line. A flag that breaks no written line says where it comes from instead ("not on the voice page: question 3"), so nobody mistakes it for a rule.
6. **Report, most important first.** One line per flag: the line from the piece, what it breaks, and the fix. If nothing is flagged, say so in one line. No essay on voice.
7. **Change the piece after a yes.** Apply the fixes the person accepts, in place, and update `last_updated` and `last_updated_by`. When the author says the piece is ready for someone else to read, set `status: in-review` in the piece and in its row in [`pieces/README.md`](../pieces/README.md).
8. **Write back what repeats.** A correction to one draft is not a brand change. When the same flag comes back across pieces, propose a line for [the voice page](../../../company/brand/voice.md) to its owner, or for the author's `people/<name>/tone-of-voice.md`, under Corrections, when it is about one person, and write it after a yes. Until then it is a line in this space's [`lessons.md`](../lessons.md).

## Done when

- Every flag quotes the line from the piece and the line it breaks, or says where it comes from, with a fix.
- The person has the list, and the piece changed only where they said yes.
