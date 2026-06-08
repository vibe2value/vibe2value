[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / Decisions

# Decisions

Architecture decision records (ADRs). One file per decision that is costly to reverse: a tool choice, a data shape, a boundary. Each captures the context, the decision and the consequences so a later reader knows why, not just what.

## How to add one

1. Copy [`template.md`](template.md) to `NNNN-short-title.md`, using the next number.
2. Fill in context, decision, status and consequences. Keep it to a page.
3. Reference the issue and link the stack file or document it affects.

ADRs are not edited once accepted. To change a decision, write a new ADR that supersedes the old one and update the old one's status.

## Records

- [`template.md`](template.md) the shape to copy.
- [`0001-record-architecture-decisions.md`](0001-record-architecture-decisions.md) why we keep ADRs at all.
