# GTA Foundation

GTA Foundation — short for **G**et **T**ech **API** — maintains open data for every device.

We keep hardware specifications free, structured, and versioned — brands, SoCs, CPUs, GPUs, smartphones, tablets, watches, PDAs, laptops and monitors, plus a device catalog, software and websites. Every record is plain JSON, gated by automated validation, and served as a static REST API that anyone can query without a key.

## Repositories

| Repository | What it holds | Default branch |
| --- | --- | --- |
| [TechAPI](https://github.com/GetTechAPI/TechAPI) | The dataset (one JSON file per record under `data/`) and the public site with the generated API | `develop` |
| [TechEngine](https://github.com/GetTechAPI/TechEngine) | The engine around the data: validator, API server, static API generator, collectors and verification tiers | `main` |
| [game-catalog](https://github.com/GetTechAPI/game-catalog) | Satellite data repository: video game records, split out of TechAPI | `develop` |
| [cpu-engineering-samples](https://github.com/GetTechAPI/cpu-engineering-samples) | Satellite data repository: engineering-sample CPUs, kept apart from the retail CPUs in TechAPI | `develop` |
| [TechMachine](https://github.com/GetTechAPI/TechMachine) | The organisation's repository health check and the scaffolder for new satellite repositories | `develop` |
| [.github](https://github.com/GetTechAPI/.github) | This profile and the community files every repository inherits | `main` |

## How they connect

```text
TechAPI      --pins-->          TechEngine (git submodule: validates the data, builds the API)
TechAPI site <--summary.json--  game-catalog, cpu-engineering-samples (own validator and Pages site)
TechMachine  --checks-->        the other repositories (workflow runs, secrets, endpoints)
TechMachine  --scaffolds-->     new satellite data repositories
.github      --shares-->        contributing guide, default issue and PR templates
```

## Where to start

- **A wrong or missing record**: open an issue with the forms in [TechAPI](https://github.com/GetTechAPI/TechAPI/issues/new/choose).
- **The validator, the API, collectors or verification**: [TechEngine](https://github.com/GetTechAPI/TechEngine).
- **Video games**: [game-catalog](https://github.com/GetTechAPI/game-catalog).
- **Engineering-sample CPUs**: [cpu-engineering-samples](https://github.com/GetTechAPI/cpu-engineering-samples).
- **Contributing to any of them**: [CONTRIBUTING.md](https://github.com/GetTechAPI/.github/blob/main/CONTRIBUTING.md).

## Licence

Data is CC BY-SA 4.0; code is MIT. Each repository's README has the exact terms and the attribution line.
