[PROJECT_NAME](../../README.md) / [Knowledge base](../README.md) / System

# System

How the PROJECT_NAME project runs as an engineering effort: the process, conventions and shape behind the code.

The folders are ordered by the path a change takes. It starts as a piece of work, it becomes part of something, it gets a reason recorded, it gets proved, it gets deployed and then it has to keep running.

## Contents

1. [`ways-of-working/`](ways-of-working/README.md) **how a change moves.** What counts as one change and how it gets from an idea to live. Fully written.
2. [`architecture/`](architecture/README.md) **what it is made of.** How the system fits together, plus one file per tool in the stack.
3. [`decisions/`](decisions/README.md) **why it is this way.** Architecture decision records, for the calls that are costly to reverse.
4. [`testing/`](testing/README.md) **what proves it works.** What is tested, at what level and what is deliberately not tested.
5. [`environments/`](environments/README.md) **where it runs and how it gets there.** Local, develop, staging and main, with secrets and deploy.
6. [`running/`](running/README.md) **what happens when it breaks.** How a failure surfaces and what comes to a person.

`ways-of-working/` is fully written. In `running/` the method is written and PROJECT_NAME's own answer is not. Everything else is a stub that names its question.
