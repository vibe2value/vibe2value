# vibe2value base

A cloneable starting point for a new project built with AI assisted coding, using the vibe2value shape+build+launch framework. Clone this, rename it and fill it in. There is no application code yet on purpose: the value here is the scaffold and the conventions, so a person or an AI picks up the project from a clear, written starting point.

The framework this is built around lives at https://vibe2value.com .

## What you get

- A [`knowledge-base/`](knowledge-base/README.md) laid out for the framework: `product/` (what it is), `shape-build-launch/` (one file per idea across the three phases) and `system/` (ways of working, architecture, decisions, testing, environments, running).
- A [`CLAUDE.md`](CLAUDE.md) that points an AI assistant at the knowledge base and the working rules.
- Fully written `system/ways-of-working/` (branching and commit conventions) and a written method in `system/running/` (how a failure surfaces and what comes to a person). Everything else is a stub that names the one question it will answer.
- A stack-neutral `system/architecture/stack/`: the base picks no tools for you, it gives you the place and the template to record the stack you choose and the assumptions it puts on the build.
- An MIT [`LICENSE`](LICENSE) and a starter `.gitignore`.

## Start a new project from it

1. Click **Use this template** on GitHub to create a fresh repo with clean history, or clone this one and re-point the remote.
2. Replace `PROJECT_NAME` everywhere with your project's name:
   ```bash
   grep -rl PROJECT_NAME . --exclude-dir=.git | xargs sed -i 's/PROJECT_NAME/your-name/g'
   ```
3. Work through Shape first: fill in [`knowledge-base/shape-build-launch/shape/`](knowledge-base/shape-build-launch/shape/README.md) and [`knowledge-base/product/`](knowledge-base/product/README.md). Each stub names the one question it answers.
4. Record the stack you choose in [`knowledge-base/system/architecture/stack/`](knowledge-base/system/architecture/stack/README.md), one file per tool, and the call as an ADR in [`knowledge-base/system/decisions/`](knowledge-base/system/decisions/README.md).
5. Add the app code when Build starts. Wire the toolchain commands into `CLAUDE.md`.

## How to work in it

- Start at the README in any folder. It links every document below it.
- Each document does one job and answers one question. Keep documents short, plain and current.
- Fix a document in the same change that made it wrong. The git history is the decision log.
- Write with no emdashes and no Oxford comma, plain enough for a person or an AI to read.

## License

MIT, see [LICENSE](LICENSE).
