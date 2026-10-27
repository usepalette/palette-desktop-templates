---
type: doc
read_when:
  - You are naming a feature, a part in a scope, a page in a design file or a screen on it
---

# Naming

> **Not confirmed yet.** A starter set. Change it until it says what the team believes, then delete this box.

How the parts of the product get their names: the features in a scope, the docs that describe them and the pages in the design file. A name is the handle everyone uses for a part, so it is chosen once and used the same way everywhere.

## A name is a thing you can point at

Name a part after the thing a person could point at, or the one action they take on it. Never after a description of it.

| Shape | What it names | Examples |
|---|---|---|
| **An entity** | Something in the product with an identity of its own | Invoice, Comment, Project |
| **A specific action** | One thing the person does to one entity | Send Invoice, Archive Project |
| **A named feature** | A feature the product shows under that name | Inbox, Search, Settings |

The test: a user, a developer and a designer would all say the name the same way, and it fits on a tab, a menu row or a page title.

## The rules

- **Short** — One to three words. A longer name is describing the part
- **The content, not the screen** — *Page*, *screen*, *view* and *tab* stay out: *Invoices page* is *Invoice*
- **Singular** — The spec describes one, and every one follows it
- **An action carries its entity** — *Archive Project*, not *Archive*
- **No "and"** — A name that needs it holds two parts. Split it
- **No point of view** — Not *My projects* or *Your invoices*
- **No invented abstractions** — Use the product's own word before coining one
- **Title Case** — A part's name is a proper name. Text on the screen stays in sentence case, per [`typography.md`](typography.md)

## One name everywhere

A part has the same name in the scope, the file names, the design file and the log, and a rename moves all of them the same day.
