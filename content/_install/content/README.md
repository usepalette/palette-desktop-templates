# Content

A home for the writing you ship — blog posts, social posts, newsletters,
pitches, copy. Driven by the `/content` skill, but everything is just markdown
you can edit by hand.

## Layout

```text
content/
├── content.md      # the log — what you've shipped and what's in flight
├── voice.md        # how you sound — tone, principles, words to avoid, self-check
├── playbook.md     # how you think about content — approach, channels, distribution
└── drafts/         # pieces in progress, one markdown file each
```

## How it works

1. **Start a draft** — `/content new "<topic>"` creates a file in `drafts/`
   with a target channel and the one takeaway pinned down.
2. **Refine it** — `/content refine <slug>` tightens it against `playbook.md`.
3. **Check the voice** — `/content voice-check <slug>` runs the self-check in
   `voice.md` against the copy.
4. **Plan distribution** — `/content distribute <slug>` maps primary channel,
   amplification, and repurposing.
5. **Log it** — `/content log` records what shipped in `content.md`.

## The two reference files

- **`voice.md`** is the source of truth for how you sound. It was personalized
  at install — keep it current as your voice evolves. The `voice-check` mode
  reads it every time.
- **`playbook.md`** is how your team approaches content: philosophy, the
  before/while/after of writing, content types, and distribution.

Both are yours to edit. The more they reflect how you actually write, the
better the skill's output.
