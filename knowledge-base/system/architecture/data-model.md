[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / [Architecture](README.md) / Data model

# Data model

> Status: the method below is written. PROJECT_NAME's answer is not filled in yet.

**Question this file answers:** What are the core entities and how do they relate?

The schema is the truth about the columns. This file is the truth about the meaning, which is the part a schema cannot carry and the part a person or an AI needs before touching anything.

Use the words the product uses. If the code calls it something else, say both, because that gap is exactly where mistakes get made.

## What to write down

### The entities

The few things the product is really about, each with a sentence saying what it is in the language of the people who use it. Not every table. The ones the product would be meaningless without.

### How they relate

Which one belongs to which, what can exist on its own and what cannot exist without something else. Say the direction plainly. One of these has many of those.

### What identifies each one

What makes two of them the same thing or different things. This is where duplicates come from later. It is nearly always decided by accident if it is not decided here.

### What is deliberately not modelled

The things kept out on purpose, with the reason. This mirrors the intentional gaps in [`../../product/intentional-gaps.md`](../../product/intentional-gaps.md) on the data side.

### Where the real shape lives

The file or the migrations that define it, so a reader knows where to go for the detail. Say how this file is kept in step with that one.

## The check

**Pass:** someone can read this and predict the shape of the data before opening the schema and say what would be wrong about adding a field in the obvious place.

**Fail:** it repeats the schema column by column, or it no longer matches it.

## PROJECT_NAME's answer

Fill this in.
