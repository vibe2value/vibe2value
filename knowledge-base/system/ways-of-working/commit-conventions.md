[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Ways of working](README.md) / Commit conventions

# Commit conventions

PROJECT_NAME uses Conventional Commits. The format is small, it reads well for people and it lets tooling build changelogs later.

## Format

```
<type>: <summary> (#issue)
```

- `type` is one of: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`. These are the Conventional Commit types; note the branch prefix `feature/` maps to the commit type `feat`.
- `summary` is a short imperative line. Write "add search filter", not "added" or "adds".
- `(#issue)` links the commit to its issue. Every commit ends with it.

Keep the summary under about 70 characters. Lower case after the colon. No full stop at the end. Commits are a single subject line, with no body.

Examples:

```
feat: add search filter to list (#12)
fix: stop crash on empty list (#41)
docs: write ways of working docs (#7)
chore: bump dependencies (#23)
```

## Rules of thumb

- One logical change per commit. If you need the word "and" in the summary, it is probably two commits.
- Commit often while you work. You can tidy the history before opening the pull request.
- Write the summary so a reader scanning `git log` understands the change without opening it.
