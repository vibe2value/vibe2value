[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Environments](README.md) / Secrets

# Secrets

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** Where do secrets live and how are they set per environment?

This file records where to find things and how to set them. It never records a secret itself. If a value belongs in here, it is not a secret.

## What to write down

### What counts as a secret in PROJECT_NAME

API keys, database URLs, signing keys, webhook tokens. Name the classes rather than the values, so a reader can tell whether the thing in their hand is one.

### Where each environment keeps them

For every environment in [`README.md`](README.md), say what holds the values. A platform settings panel, a secret manager, a local file that is never committed. Local is usually different from the rest and that difference is worth stating rather than assuming.

### How a value gets set and changed

The actual route. Who can do it, through which interface and whether the change takes effect immediately or needs a redeploy. A secret that silently needs a redeploy is a good way to spend an afternoon.

### Which names exist

The list of names the code reads, with a one-line description of each and which environments need it. Keep the names here and the values elsewhere. An example file committed alongside the code is the usual way to do this, holding every name with no real value against any of them.

### How a new person or a new AI gets what it needs

What someone does on day one to run PROJECT_NAME locally. If the answer is that they ask a particular person, say so plainly, because that is a dependency worth seeing.

### What happens when one is rotated

Who changes it, in what order across the environments and what breaks in between. Rotation is the moment the gaps in this file show up.

## The check

**Pass:** a new person can get PROJECT_NAME running from this file without being handed a value out of band. Every name the code reads appears here.

**Fail:** a real value has been written into this file, or the code reads a name that nobody has listed.

## PROJECT_NAME's answer

Fill this in.
