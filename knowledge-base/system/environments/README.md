[PROJECT_NAME](../../../README.md) / [Knowledge base](../../README.md) / [System](../README.md) / Environments

# Environments

The four places PROJECT_NAME runs, and how config and deploys differ between them. The branch behind each environment is defined in [`../ways-of-working/branching-strategy.md`](../ways-of-working/branching-strategy.md); this folder covers the runtime side.

| Environment | Branch    | Purpose                                   |
| ----------- | --------- | ----------------------------------------- |
| local       | none      | Your machine.                             |
| develop     | `develop` | Integration. First place a merge deploys. |
| staging     | `staging` | Pre-production. Mirrors production.        |
| main        | `main`    | The live product.                          |

## Documents

- [`secrets.md`](secrets.md) where secrets live and how they are set per environment.
- [`deploy.md`](deploy.md) how each environment gets deployed.
