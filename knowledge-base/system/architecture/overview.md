[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Architecture](README.md) / Architecture overview

# Architecture overview

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** How is the system put together at a high level?

This file and [`../../shape-build-launch/build/system-shape.md`](../../shape-build-launch/build/system-shape.md) are close together and they are not the same job. That file is the decision, pinned down once and sharpened until two people would draw the same boundaries. This one is the description of what is actually there now, kept current as the system changes.

Write it for someone who has to make a change tomorrow and needs to know what their change will touch.

## What to write down

### The parts and what each one owns

A handful, not a catalogue. Give each part one job in a sentence. If a part needs two sentences it is probably two parts.

### Where each part runs

Which machine, service or runtime holds it. The tool behind each answer goes in its own file under [`stack/`](stack/README.md); here it is one line so the shape can be read in one go.

### The handoffs

Where one part passes work to another, plus what crosses that line. Handoffs are where changes go wrong, so name them even when they look obvious.

### What sits outside the boundary

The things PROJECT_NAME depends on but does not own. Say what happens to the system when one of them is unavailable.

### What this file does not cover

Point onward rather than repeating. The data shape is in [`data-model.md`](data-model.md), each tool is under [`stack/`](stack/README.md) and why a tool was chosen is an ADR in [`../decisions/`](../decisions/README.md).

## Keeping it current

This file goes stale faster than anything else in the knowledge base, because the system moves and the description does not follow on its own. Fix it in the same change that made it wrong. A stale overview is worse than none, because it gets believed.

## The check

**Pass:** someone new can read this and say which part they would change for a given piece of work and what else that change would touch.

**Fail:** it is a list of tools rather than a set of parts with owners and handoffs.

## PROJECT_NAME's answer

Fill this in.
