---
type: doc
owner: "[Owner]"
status: draft
last_updated: YYYY-MM-DD
last_updated_by: "[Owner]"
edit_policy: team
read_when:
  - Before designing a new screen, component or flow
---

# Philosophy

> **Not confirmed yet.** A starter set. Change it until it says what the team believes, then delete this box.

## Simplicity comes from the system

A product can be complex underneath and calm on the surface. The foundations carry the complexity: tokens, semantic names, shared components. If a value or a pattern repeats, it belongs in the system, not in one screen.

## One job per screen

Each screen does one thing well. Secondary actions stay hidden until the person shows they want them. If a screen feels busy, it is doing too much. The product should feel simple on the first visit and powerful on the tenth.

A need found along the way that reaches past the screen, such as permissions or sync, is solved once for the whole product. Split it into its own piece of work.

## Tokens are the bridge

Tokens are the one source of truth between design and code. They are named by purpose, not by appearance: `text-primary`, not `gray-900`. The semantic layer is what makes dark mode, theming and platform differences possible without touching component code.

## Follow the platform

Use the conventions people already know on the platform you design for before inventing your own. Consistency across platforms comes from shared tokens and patterns, not from one shared look.

## Interaction is a material

Motion, focus, hover and gesture are design decisions. They communicate state and guide attention, and they are tuned in a running prototype or the code, because feel cannot be judged in a static frame.

## Prototypes are disposable, systems are durable

A prototype answers a question fast and is thrown away. The system evolves slowly, is documented carefully and carries what the team has learned. Experiment freely; change the system on purpose.

## Design every state

Empty, loading, error, long content and no permission are part of the design. A part that only looks right with good data is not finished.

## Accessible by default

Everyone can use what we design: real buttons and links, a label on every input, visible focus, enough contrast, and everything works with the keyboard.

## Convention over enforcement

A clear written convention aligns the whole team, people and agents, at a fraction of the cost of enforcing it in code. Write down what to use, when and why.

## What ships is the strongest reference

When designing inside an existing product, read what ships before you design: the code, or the library it is built from. Find the screens and components closest to what you are building and match them: spacing, structure, naming, interaction. When a principle and the shipped product disagree, the product wins, or the pattern changes everywhere, on purpose.

The same holds for components. When one cannot do what a screen needs, extend it with a slot, a property or a variant, and use it. Never build around it in one screen.

## Name the principle

When a decision matters, say which principle it follows, so the next person can follow the reasoning and knows what they are breaking if they change it.
