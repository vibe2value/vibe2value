[PROJECT_NAME](../../../../README.md) / [Knowledge base](../../../README.md) / [System](../../README.md) / [Architecture](../README.md) / Stack

# Stack

The tools PROJECT_NAME is built with, documented one file per tool and grouped by what kind of dependency it is. The base ships no stack and takes no side: the choice is yours. These files exist to make the choice explicit and to record the assumptions a build rests on, so a person or an AI does not have to guess what the project runs on.

The split is by how the dependency relates to the code:

- [`platform/`](platform/README.md) where it runs. The runtime, hosting and platform-native primitives it deploys onto.
- [`frameworks/`](frameworks/README.md) what the code is built with. The language, libraries and frameworks bundled into the project.
- [`external-services/`](external-services/README.md) what it talks to. Third-party services reached over the network at runtime.

Each file answers the same questions for its tool: why this, not the obvious alternative, how it is used, and what choosing it commits the build to. File a choice where it most lives, and link across if it spans two folders.

## What a build needs to decide

Whatever the answers turn out to be, a build should be able to point to where each is written down:

- the language and frameworks the code is built with: `frameworks/`
- the runtime or platform it deploys to: `platform/`
- how data is stored: `platform/` if platform-native, otherwise `frameworks/` or `external-services/`
- how the interface is built, if it has one: `frameworks/`
- how input is validated, tested and built: `frameworks/`
- any third-party service it depends on: `external-services/`

Add a file for each choice that matters to PROJECT_NAME, in whatever stack you land on.
