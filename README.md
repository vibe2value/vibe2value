# vibe2value base

A starting point for a project built with AI, using the vibe2value framework.

**This repo holds questions, not answers.** Every file in `knowledge-base/` names one thing that has to be discovered about your project and leaves the space for what you find. There is no application code and no method written down in here, on purpose.

**The method lives in a skill.** How to decide, what a good answer looks like and how to tell when yours is not good enough yet. The skill is versioned on its own and improves without you touching your repo.

Two halves. The repo is yours. The skill is ours.

The framework behind both is at https://vibe2value.com .

## What is in here

- [`knowledge-base/`](knowledge-base/README.md) the only folder, laid out for the framework: `product/` what it is, `shape-build-launch/` one file per idea and `system/` how it is built and run.
- [`CLAUDE.md`](CLAUDE.md) points an AI assistant at the knowledge base and the working rules.
- An MIT [`LICENSE`](LICENSE) and a starter `.gitignore`.

Every file is in one of two states, explained in [`system/README.md`](knowledge-base/system/README.md). Fully written means the answer ships with the base. A stub names its one question and nothing else.

Nothing here picks your stack. `system/architecture/stack/` gives you the place to record what you chose and what it commits you to.

## Install the skill

```
/plugin marketplace add vibe2value/claude-plugins
/plugin install shape-build-launch@vibe2value
```

Then run it on whatever you are building:

```
/shape-build-launch:guide
```

## Start a new project

1. Click **Use this template** on GitHub for a fresh repo with clean history.
2. Replace `PROJECT_NAME` with your project's name:
   ```bash
   grep -rl PROJECT_NAME . --exclude-dir=.git | xargs sed -i 's/PROJECT_NAME/your-name/g'
   ```
3. Install the skill and start with Shape. The skill asks the questions. You bring the answers. Each one lands in the file that names it.
4. Record the stack you choose in [`system/architecture/stack/`](knowledge-base/system/architecture/stack/README.md), one file per tool, with the call written up as an ADR in [`system/decisions/`](knowledge-base/system/decisions/README.md).
5. Add the app code when Build starts, then wire the toolchain commands into `CLAUDE.md`.

## What the skill does not cover yet

The skill answers Shape, Build and Launch. It does not yet cover `system/`, which is everything about getting the project running and keeping it there.

Those stubs still name the right questions. Until the skill reaches them you are answering them unaided, so treat anything an AI writes into `system/` as a first draft rather than a decision.

This is a known gap and it is named here rather than left to be discovered.

## How to work in it

- Start at the README in any folder. It links every document below it.
- Each document does one job and answers one question. Keep documents short, plain and current.
- Fix a document in the same change that made it wrong. The git history is the decision log.
- Write with no emdashes and no Oxford comma, plain enough for a person or an AI to read.

## License

MIT, see [LICENSE](LICENSE).
