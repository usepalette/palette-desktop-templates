---
title: Workspace heal
summary: A check of the whole workspace for broken links, lists that no longer match and unfinished pages, with the safe fixes when you ask.
category: team
order: 6
tags: [workspace, maintenance, links, health]
request: "Check the workspace for broken links, lists that are out of date and pages nobody finished, and fix the safe things."
type: artifact
artifact_kind: skill
version: 2611111
author: Palette
updated: 2026-11-11
---

# Workspace heal

A check of the whole workspace for broken links, lists that no longer match and unfinished pages, with the safe fixes when you ask.

## What it does

One skill that checks the workspace against its own rules and reports what has drifted: links that go nowhere, lists that no longer match their folders, pages still waiting for someone, spaces missing their rules, commands without their pointers. Each finding names the file, the rule and the smallest fix, with the decisions first.

It changes nothing until you ask it to fix the safe things. Then it repairs only what is clear, such as a link to a renamed file, a stale row or a missing pointer, and asks before anything else.

In a workspace made from Company OS Core, it checks everything Core's own workspace check does, and follows that page where the two differ. It finds where things live from the workspace's map and its folders, so it keeps working after you rename, remove or add a folder. In any other workspace, it uses the rules it finds there.

## The request

> Check the workspace for broken links, lists that are out of date and pages nobody finished, and fix the safe things.

Said in the person's own words. "Is anything broken?" works too.

## What it reads

- **The workspace's rules**: the root `AGENTS.md` and `README.md`, and in Company OS Core, `.agents/conventions.md`, `.agents/page-states.md` and the workspace's own check in `.agents/commands/`.
- **Every page and folder** in the workspace, except Git, dependency and build folders.

It reads no outside tool and sends nothing anywhere.

## What lands in the workspace

At the root of the workspace, where agents look for skills:

```
.claude/skills/workspace-heal/SKILL.md     the check, the report and the safe fixes
```

Palette lists the skill for every agent. In a Company OS Core workspace it takes the place of Core's `workspace-heal` command in the list, and follows the same page.

## How it stays current

Ask for a check whenever you want one; once a week keeps drift small. A new version replaces the skill's folder and never touches the workspace.

## Example

A report in a workspace made from Company OS Core, where the team renamed `customers/` to `clients/`. The findings are made up.

```
Mostly healthy: 1 decision, 3 safe fixes.
Basis: Core. Scope: the whole workspace, .git left out. Complete.

Decisions
- spaces/research/: no AGENTS.md. Every space keeps one, with its two pointers. Write it with the owner?

Safe fixes
- clients/README.md: the row for Fjord has no folder; the folder was removed on 2026-11-03. Remove the row.
- people/mia/README.md:12: links to projects/portal/, which is now projects/portal-v2/. Fix the link.
- .claude/commands/new-client.md: missing for .agents/commands/new-client.md. Add the pointer.

Optional
- company/brand/voice.md is still Not filled in yet.

Findings 5 · safe fixes 3 · decisions 1 · optional 1
```
