[PROJECT_NAME](../README.md) / Knowledge base

# Knowledge base

Everything to do with the PROJECT_NAME project lives here: what it is, how it is built and how we work. It is written to be read by both people and AI. Keep documents short, plain and current.

Most files are stubs, each naming the one question it will answer. A few are fully written. [`system/README.md`](system/README.md) explains the two states.

## Map

- [`product/`](product/README.md) what PROJECT_NAME is. Spec, assumptions, intentional gaps and open questions. Mirrors the public page at <link to your public project page> .
- [`shape-build-launch/`](shape-build-launch/README.md) your Shape, Build and Launch decisions. One file per idea across the vibe2value framework.
- [`system/`](system/README.md) how the project runs, in the order a change moves: ways of working, architecture, decisions, testing, environments and running.

## How to use it

- Start at the README in any folder. It links every document below it.
- Each document does one job and answers one question. If a document grows a second job, split it.
- If something here goes out of date, fix it in the same change that made it wrong. The git history is the decision log.

## Is it working?

Run the test in the root [`README.md`](../README.md) and record what you get. Take the first reading before you write anything.

| Date | Invented | Named gaps | Size | Note |
|---|---|---|---|---|
| | | | | baseline, before anything was filled in |

**Invented** is the count of statements an AI made about this project that are not true. It should fall to zero. It is the number that matters.

**Named gaps** is the count of places it said something is not decided yet rather than filling the space. It should rise while the base is being filled in, then fall as the gaps get answered.

**Size** is the word count of everything here, from `find knowledge-base -name '*.md' | xargs wc -w`. It only matters when it gets big enough that you can no longer hand the whole thing to an AI at once. Watch it because it grows quietly. Words that do not belong here are easier to spot as a number than as a file.

If invented is not falling, the answers being written are not the answers it needed.

## How to use it with AI

Ground every prompt about PROJECT_NAME in these files. Paste the relevant file, or the whole folder on a fresh thread, so the assistant works from the same product and the same decisions you did. The repo root [`CLAUDE.md`](../CLAUDE.md) points here for exactly this reason.
