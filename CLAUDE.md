# CLAUDE.md

Guidance for AI assistants working in the PROJECT_NAME repo. Keep it short. The detail lives in the knowledge base.

> Status: stub. Fill the sections as the project takes shape.

## What this is

PROJECT_NAME is one line saying what it is and who it is for. Fill this in once Shape is done; `knowledge-base/product/spec.md` is the longer version.

This repo starts from the vibe2value base. The knowledge base holds the questions. The method for answering them is a skill, not a document in this repo. See the root [`README.md`](README.md).

## The method

Answering a stub is a shape+build+launch decision, so use the `shape-build-launch` skill for it. The skill can surface on its own, but that is a per-message judgement rather than a guarantee, so name it: say "use the shape-build-launch skill", or run `/shape-build-launch:guide`.

If it is not installed:

```
/plugin marketplace add vibe2value/claude-plugins
/plugin install shape-build-launch@vibe2value
```

The skill covers Shape, Build and Launch. It does not reach `knowledge-base/system/` yet, so those answers are unaided for now.

## Read these first

- `knowledge-base/product/` what PROJECT_NAME is and is not.
- `knowledge-base/system/ways-of-working/` how we branch, commit and ship. Follow this.
- `knowledge-base/system/architecture/` the stack and how the pieces fit.

Ground every change in the knowledge base. If a decision is not written down there, that is a gap to close, not a detail to invent.

Where you cannot answer a stub from what is in the repo, write down that it is not decided yet and say what you would need to decide it. Do not fill the space with a plausible answer. A named gap is worth more than a confident guess.

## Working rules

- Every change starts from an issue and a branch off `develop` named `<type>/<topic>/<what>`. See `knowledge-base/system/ways-of-working/branching-strategy.md`.
- Commit with Conventional Commits, ending every commit with the issue number `(#n)` and no body. See `knowledge-base/system/ways-of-working/commit-conventions.md`.
- Write docs with no emdashes and no Oxford comma, plain enough for a person or an AI to read.

## Commands

To be added once the toolchain is wired (install, dev, test, build, deploy).
