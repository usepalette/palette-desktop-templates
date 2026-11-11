---
type: playbook
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - "You're launching a feature or a product"
  - "You're planning the comms for a launch, or a release kit"
---

# Launch

> **Not confirmed yet.** A starter playbook. Change it until it says how the team launches, then delete this box.

How we ship product updates to the world, from a small changelog entry to a full launch. Load it before planning a launch or writing any piece for one. The formats are in [`templates/launch/`](../templates/launch/README.md).

Before writing any launch content, read how the company sounds in [`company/brand/voice.md`](../../../company/brand/voice.md), and how it looks in [`company/brand/design.md`](../../../company/brand/design.md) for anything visual, so every piece sounds and looks like the same company.

## How we think about it

- **Story first, format second.** Before choosing a medium, settle what we are saying: the hook, the problem, the transformation. The messaging is the launch; everything else is formatting it for a channel.
- **Different, not better.** Position what is new as a new approach, not only an improvement on the old one.
- **One thing.** If people remember only one thing about this launch, what should it be?
- **Every launch is earned attention.** Don't waste it on a weak hook or an unclear message.

## Launch tiers

Not every update gets the same treatment. Match the effort to the impact.

- **Tier 1, a changelog update.** Small improvements, fixes and minor features. Things people notice but don't need to learn: a faster sync, a new shortcut, a fixed edge case.
- **Tier 2, a feature update.** A new capability that changes how someone works: a new integration, a new view, a redesigned flow. Existing customers think "oh, I can do that now?"; prospects get a reason to look again.
- **Tier 3, a product launch.** A significant new capability or product area that changes what we sell, not only what the product can do. The timing is coordinated across channels, and everything goes out together. A new product line, a major workflow, or a shift in who we sell to.

### Choosing the tier

**Default to Tier 2.** Most things are Tier 2. Tier 3 is rarer than it feels in the moment: a well-told story about a feature is not evidence that it needs a full launch.

**The test:** does this change what we sell, or what the thing we sell can do? If customers would still describe us the same way after it ships, only with more reasons to like us, it is Tier 2.

Signs it really is Tier 3:

- Who we sell to shifts or widens: a new persona, a new segment. [`company/market/ideal-customer.md`](../../../company/market/ideal-customer.md) would change
- Pricing or packaging changes because of it
- We would rewrite the homepage hero, not just add a section
- The competitive set changes: we are compared with different products now

If none of these apply, it is Tier 2. Ship it with confidence, and save the full push for when it counts.

## Approach

Two phases, with a hard checkpoint between them.

### Phase 1: research and messaging, for every launch

The messaging brief is the launch. No content is written until it is agreed.

1. **Understand what shipped.** Read the spec, the pull request or the description of the feature. Don't write anything until you can explain it in one sentence.
2. **Check who asked for it.** Read the customers' briefs in [`customers/`](../../../customers/README.md), what they care about, and their meeting notes; and the feature requests in the Product space when the workspace has one. The customers who asked, and the words they used, shape the framing.
3. **Check the landscape.** Read the files in [`company/market/competitors/`](../../../company/market/competitors/README.md): do they have this, and how do they position it? This shapes the angle.
4. **Draft the messaging brief** with the person, from [`templates/launch/messaging-brief.md`](../templates/launch/messaging-brief.md), and agree it before moving on:
   - **One-liner:** the launch in a sentence
   - **Audience:** who it is for
   - **Problem:** what was painful before
   - **Transformation:** what is now possible
   - **Hook:** the sharpest way to open
   - **Why now:** why it matters today
   - **Positioning angle:** the frame. Different, not better
5. **Iterate.** Review it with the team. Push back on a weak hook, and test the one-liner out loud. Every piece in Phase 2 depends on getting this right.

**Output:** an agreed messaging brief in the launch's folder (**Where the work lives**, below).

### Phase 2: content, once the messaging is agreed

Pick the pieces by tier, and by what fits this launch: not everything applies every time.

| Piece, linked to its format | Tier 1 | Tier 2 | Tier 3 |
|---|:---:|:---:|:---:|
| [Docs update](../templates/launch/docs-update.md) | ✓ | ✓ | ✓ |
| [Changelog entry](../templates/launch/changelog.md) | ✓ | ✓ | ✓ |
| [Community post](../templates/launch/community-post.md) | ✓ | ✓ | ✓ |
| Product-update email, no format yet | ✓ | ✓ | ✓ |
| [Customer blurb](../templates/launch/customer-blurb.md) | optional | ✓ | ✓ |
| [Blog post](../templates/launch/blog-post.md) | | ✓ | ✓ |
| [Account messaging](../templates/launch/account-messaging.md) | | ✓ | ✓ |
| [LinkedIn posts](../templates/launch/linkedin-post.md) | | optional | ✓ |
| [Landing page](../templates/launch/landing-page.md) | | | ✓ |
| [Video or demo script](../templates/launch/video-script.md) | | | ✓ |

Each format carries its own "How to write this". The playbook says which pieces to make; the format says how to make each one ([`templates/launch/`](../templates/launch/README.md)).

**The Tier 1 floor:** the changelog on the website and a community post, so people hear about it where they already are, plus a product-update email for anything worth emailing.

## Where the work lives

- **Tier 1:** no project. The changelog entry and the community post are written in the Content space when the workspace has one, otherwise in the person's scratchpad until they go out.
- **Tier 2 and 3:** a project in [`projects/`](../../../projects/README.md) ("we're starting a new project"), with `space: gtm` in its frontmatter. The messaging brief lives in its folder. Each piece is written in the Content space when the workspace has one, and linked from the project; otherwise it sits in the project's folder next to the brief.

## Preferences

What worked and what to avoid, per channel, as the team launches more things. One dated line each, newest on top.

_None yet._
