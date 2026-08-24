[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Environments](README.md) / Deploy

# Deploy

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** How does each environment get deployed and how does a deploy get undone?

The branch behind each environment is set in [`../ways-of-working/branching-strategy.md`](../ways-of-working/branching-strategy.md). This file is the runtime half: what actually happens when code arrives and what to do when it should not have.

Write it for someone who has never deployed PROJECT_NAME and has to do it today.

## What to write down

### What triggers a deploy to each environment

For every environment in [`README.md`](README.md), say what causes it to deploy. A merge, a tag, a manual run, a schedule. Anything a person does by hand is worth naming as such, because hand steps are the ones that get skipped under pressure.

### What runs as part of a deploy

The steps between the code arriving and the thing being live. A build, a migration, a cache clear, a smoke test. Say which of these can fail the deploy and which only warn, because that difference is what decides whether a half-finished deploy stays up.

### How data changes ride along

If the project has a database, say whether schema changes go with the deploy or separately and whether a rollback of the code implies a rollback of the data. These usually come apart. Finding that out during an incident is expensive.

### How you know it worked

Name the check that confirms it. Prefer confirming against the running thing itself over trusting the report of whatever ran the deploy. A runner can report success for a step that did nothing.

### How it gets undone

The exact route back and how long it takes. Redeploying the previous version, reverting the merge, a platform rollback button. Undoing is the part people find out they never built, so this section is worth writing before it is needed rather than after.

### What is never deployed by hand

The things that must go through the pipeline whatever the hurry.

## The check

**Pass:** someone who has not done it before can deploy PROJECT_NAME to each environment from this file, confirm it landed and get back to the previous version.

**Fail:** the route back is not written down, or "how you know it worked" is that nobody complained.

## PROJECT_NAME's answer

Fill this in.
