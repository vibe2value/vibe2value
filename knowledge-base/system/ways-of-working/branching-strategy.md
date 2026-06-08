[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Ways of working](README.md) / Branching strategy

# Branching strategy

How code moves from a local change to production in PROJECT_NAME. Read this before you start a feature.

## Environments and long-lived branches

PROJECT_NAME has four environments. Three of them are tracked by a long-lived branch that always reflects what is deployed there.

| Branch    | Environment | Purpose                                              |
| --------- | ----------- | ---------------------------------------------------- |
| `main`    | production  | The live product. Always deployable. Protected.      |
| `staging` | staging     | Pre-production. Mirrors production for final checks.  |
| `develop` | develop     | Integration. Where finished feature branches land.    |

`local` is your machine. It has no shared branch.

Code only moves forward: `feature -> develop -> staging -> main`. Nothing is committed straight onto a long-lived branch.

## The cycle

1. Pick an issue. Every change starts from a tracked issue (see How work ties to an issue below).
2. Branch off `develop`.
3. Do the work in small commits (see `commit-conventions.md`).
4. Open a pull request back into `develop`. CI runs and someone reviews it.
5. Merge into `develop`. It deploys to the develop environment.
6. Promote `develop` into `staging` when you are ready to verify a release. Check it in the staging environment.
7. Promote `staging` into `main` to go live. Tag the release.

Promotion between long-lived branches is a pull request too, never a force push.

## Branch naming

Use this format:

```
<type>/<topic>/<what>
```

- `type` is the kind of work: `feature`, `fix`, `chore`, `docs`, `refactor`, `test`.
- `topic` is the area of the project the work sits in, for example `email`, `auth` or `dashboard`.
- `what` is the specific change, two to four words, lower case, hyphen separated.

Examples:

```
feature/email/welcome
feature/auth/password-reset
fix/dashboard/empty-state-crash
chore/deps/bump-dependencies
```

Keep one branch to one change. If the work splits, branch again.

## How work ties to an issue

Every change still maps to an issue, but the link lives in the commits, not the branch name. Every commit ends with the issue number as `(#n)`, so you keep a clean trail from issue to commits to pull request to merge.

- Open or pick the issue first. If there is no issue, the work is not ready to start.
- Name the branch by topic, not by number.
- End every commit with `(#n)` and reference the issue in the pull request, so GitHub links and closes it for you.
- Close the issue by merging the pull request, not by hand.

One issue, one branch, one pull request is the default. Keep each one small so it is easy to review and easy to revert.
