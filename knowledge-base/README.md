[PROJECT_NAME](../README.md) / Knowledge base

# Knowledge base

Everything to do with the PROJECT_NAME project lives here: what it is, how it is built and how we work. It is written to be read by both people and AI. Keep documents short, plain and current.

Most files are stubs for now. Each names the one question it will answer. Two areas are further along: `system/ways-of-working/` is fully written and `system/running/` carries the method with your own answer still to fill in.

## Map

- [`product/`](product/README.md) what PROJECT_NAME is. Spec, assumptions, intentional gaps and open questions. Mirrors the public page at <link to your public project page> .
- [`shape-build-launch/`](shape-build-launch/README.md) your Shape, Build and Launch decisions. One file per idea across the vibe2value framework.
- [`system/`](system/README.md) how the project runs, in the order a change moves: ways of working, architecture, decisions, testing, environments and running.

## How to use it

- Start at the README in any folder. It links every document below it.
- Each document does one job and answers one question. If a document grows a second job, split it.
- If something here goes out of date, fix it in the same change that made it wrong. The git history is the decision log.

## How to use it with AI

Ground every prompt about PROJECT_NAME in these files. Paste the relevant file, or the whole folder on a fresh thread, so the assistant works from the same product and the same decisions you did. The repo root [`CLAUDE.md`](../CLAUDE.md) points here for exactly this reason.
