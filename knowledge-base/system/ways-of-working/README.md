[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / Ways of working

# Ways of working

The conventions for getting a change from an idea into production. Small, grounded in common practice and meant to be followed by both people and AI.

This is a perspective, not a law. It is the default the base ships with because it works well for a small team building in the open. Change it as the project requires, and write the change down here so the next person and the next AI work from the current way, not the original one.

## Documents

- [`branching-strategy.md`](branching-strategy.md) the develop, staging and main flow, branch naming and how work ties to an issue.
- [`commit-conventions.md`](commit-conventions.md) how to write commit messages.

## The short version

1. Every change starts from an issue.
2. Branch off `develop` using `<type>/<topic>/<what>`.
3. Commit with Conventional Commits, ending every commit with `(#n)`.
4. Open a pull request back into `develop`.
5. Promote `develop` to `staging`, then `staging` to `main` to release.

Read the two documents above for the detail.
