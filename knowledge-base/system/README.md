[PROJECT_NAME](../../README.md) / [Knowledge base](../README.md) / System

# System

How the PROJECT_NAME project runs as an engineering effort: the process, conventions and shape behind the code.

The folders are ordered by the path a change takes. It starts as a piece of work, it becomes part of something, it gets a reason recorded, it gets proved, it gets deployed and then it has to keep running.

## Contents

1. [`ways-of-working/`](ways-of-working/README.md) **how a change moves.** What counts as one change and how it gets from an idea to live. Fully written.
2. [`architecture/`](architecture/README.md) **what it is made of.** How the system fits together, plus one file per tool in the stack. Method written for the stack, stubs for the overview and the data model.
3. [`decisions/`](decisions/README.md) **why it is this way.** Architecture decision records, for the calls that are costly to reverse. Method written, records to add.
4. [`testing/`](testing/README.md) **what proves it works.** What is tested, at what level and what is deliberately not tested. Stub.
5. [`environments/`](environments/README.md) **where it runs and how it gets there.** Local, develop, staging and main, with secrets and deploy. Method written.
6. [`running/`](running/README.md) **what happens when it breaks.** How a failure surfaces and what comes to a person. Method written.

## The three states a file can be in

The difference matters, because two of them are your work and one of them is not.

- **Fully written.** The answer ships with the base. Change it if PROJECT_NAME needs something else and write the change down here.
- **Method written.** You are told how to decide, not what to decide. The file names what to write down and how to tell when it is good enough. Your answer goes at the bottom.
- **Stub.** The file names the one question it will answer and nothing more. A stub means the base has not told you how yet.
