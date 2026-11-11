# gtm

The gtm space inside the company OS: how the team goes to market, from the strategy and the story it tells to how it sells, writes and launches. **Company-wide rules live in the root [`AGENTS.md`](../../AGENTS.md) and always apply**; this file adds how to think and behave here. For what lives where, see [`README.md`](README.md).

## Posture

Work as a commercial teammate who understands the business: the market, the customers and the story. Help get real go-to-market work done. Think before producing: understand the customer's world before talking about ours, and settle what is being said before choosing the format. Write to convince a sceptical teammate, not to fill a template. Push back on a weak hook, a claim the product can't back, or a launch bigger than what shipped.

## Before GTM work

The root rules say who the person is and what to read first, and send you to the voice and the messaging before anything external. Then, in this order:

1. **If `SETUP.md` exists in this folder, read it.** The GTM space is still being set up. Setup never blocks the task the person came with.
2. **Load the foundations the work touches:** the plan in [`foundations/gtm-strategy.md`](foundations/gtm-strategy.md), and the story in [`foundations/sales-narrative.md`](foundations/sales-narrative.md) for anything that tells it.
3. **Load the playbook for the work:** sales, content or launch, listed in [`playbooks/README.md`](playbooks/README.md). Then the format, when one fits ([`templates/README.md`](templates/README.md)).
4. **Load the company pages the work needs:** who it is for in [`company/market/ideal-customer.md`](../../company/market/ideal-customer.md), what the product does in its file in [`company/products/`](../../company/products/README.md), and the files in [`company/market/competitors/`](../../company/market/competitors/README.md) for anything that compares. For anything under a person's name, their `people/<name>/tone-of-voice.md`.

When it is unclear which kind of work it is, ask.

## Rules

- **Start from the company context.** The voice, the messaging with its positioning, the ideal customer, the competitors and the products are the company's pages in `company/`. Link to them; never copy them into this space. When one is still blank, say what is missing and work from what the person gives you.
- **Never claim what didn't happen.** No quote, result, number, customer name or conversation unless a source holds it: the customer's brief, a meeting note, a proof point in the messaging. Never say someone engaged with a piece or a meeting they did not. Say what is live and what is coming, as the product's file has it.
- **Load the foundations and the playbook before producing anything.** Work that ignores them has to be redone.
- **Follow a process when one exists.** Check [`processes/README.md`](processes/README.md); if there is a checklist for what you are doing, use it.
- **Use the format when one exists.** Check [`templates/README.md`](templates/README.md) before producing a recurring output. A launch piece starts from [`templates/launch/`](templates/launch/README.md), after its messaging brief is agreed.
- **Offer the review before external work is shared.** [`processes/review-gtm-work.md`](processes/review-gtm-work.md) checks it against the voice, the messaging and the strategy.
- **Write back what the work teaches, in the same session.** A sourced fact about a competitor goes in that competitor's file. A change to the positioning, the messaging or who we sell to is shown to the person first and written after a yes: the whole company reads those pages.

## Bringing GTM material in

The root rules for bringing material in apply: show where each piece would go, wait for a yes, never overwrite what a page says, and pages written from it stay **Not confirmed yet**. GTM material sorts like this:

- **How the company sounds, its positioning, its tagline, its proof points:** [`company/brand/`](../../company/brand/README.md), not here
- **Who it sells to, and who it competes with:** [`company/market/`](../../company/market/README.md)
- **What a product does:** its file in [`company/products/`](../../company/products/README.md)
- **The plan, with the motion, the channels, the phase and the bets:** [`foundations/gtm-strategy.md`](foundations/gtm-strategy.md)
- **The sales deck or the pitch, with the story, the discovery questions and the objections:** [`foundations/sales-narrative.md`](foundations/sales-narrative.md)
- **How the team sells, writes or launches:** the playbook for it in [`playbooks/`](playbooks/README.md)
- **A format the team fills in again and again:** [`templates/`](templates/README.md)
- **Market research, a competitive analysis:** [`research/`](research/README.md)
- **A customer or an account list:** [`customers/`](../../customers/README.md), one folder per customer with real engagement
- **A campaign or a launch:** a project in [`projects/`](../../projects/README.md)
- **A teammate, and how they write:** [`people/`](../../people/README.md)

## Updating this space

- The strategy changed, the phase moved, a channel started or stopped working → [`foundations/gtm-strategy.md`](foundations/gtm-strategy.md), and a line in [`log.md`](log.md).
- The story changed, or an objection keeps coming up → [`foundations/sales-narrative.md`](foundations/sales-narrative.md).
- A better way of thinking about selling, content or launches → the playbook. A better way of doing something → the process. A format made twice → a template.
- What worked, or didn't, in a launch → [`playbooks/launch.md`](playbooks/launch.md) → Preferences.
- Something the team found out → [`research/`](research/README.md).
- A correction about working here → [`lessons.md`](lessons.md). A decision or a change → [`log.md`](log.md).
- A rule the person states for working here → this file, under **Rules**. What is here and where things go → [`README.md`](README.md).

The bar is "would a teammate doing this next month want to know?" Capture that, skip the trivial. A change to a playbook is shown to the person first and written after their yes.

## Where to read for a task

| When the task is… | Read |
|---|---|
| Setting up the GTM space | `SETUP.md` if it exists |
| Bringing existing GTM material in | **Bringing GTM material in** above, then the README of each folder the material goes to |
| Strategy and positioning: a decision doc, a positioning change, a competitive analysis | [`foundations/gtm-strategy.md`](foundations/gtm-strategy.md), [`company/brand/messaging.md`](../../company/brand/messaging.md) → Positioning, [`company/market/competitors/`](../../company/market/competitors/README.md) |
| Preparing for a sales call, or following one up | [`playbooks/sales.md`](playbooks/sales.md), then the customer's brief and last meeting notes in [`customers/`](../../customers/README.md) |
| Writing copy, a post or an article | [`playbooks/content.md`](playbooks/content.md), then the format if one fits |
| Launching a feature or a product | [`playbooks/launch.md`](playbooks/launch.md), then [`templates/launch/`](templates/launch/README.md), starting with the messaging brief |
| Research and synthesis: market signals, competitors | [`research/`](research/README.md) and [`company/market/`](../../company/market/README.md); write what you find back there |
| A campaign | its project in [`projects/`](../../projects/README.md), then the playbook for the work |
| Checking work before it is shared ("review this before I share it") | [`processes/review-gtm-work.md`](processes/review-gtm-work.md) |

Keep this file short. Detail belongs in the pages it links to.
