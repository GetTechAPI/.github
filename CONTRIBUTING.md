# Contributing to GetTechAPI

This guide applies to every repository in the organisation. Each repository's
README has its own layout and commands; read it before you start.

## Pick the repository

| You want to change | Repository |
| --- | --- |
| A hardware, software or website record, or the public site | [TechAPI](https://github.com/GetTechAPI/TechAPI) |
| The validator, the API, the collectors or the verification tiers | [TechEngine](https://github.com/GetTechAPI/TechEngine) |
| A video game record | [game-catalog](https://github.com/GetTechAPI/game-catalog) |
| An engineering-sample CPU record | [cpu-engineering-samples](https://github.com/GetTechAPI/cpu-engineering-samples) |
| The repository health check or the satellite scaffolder | [TechMachine](https://github.com/GetTechAPI/TechMachine) |
| The organisation profile or these shared files | [.github](https://github.com/GetTechAPI/.github) |

Not sure a record is wrong? Open an issue first with
[TechAPI's issue forms](https://github.com/GetTechAPI/TechAPI/issues/new/choose).

## Branches

- TechAPI, TechMachine, game-catalog and cpu-engineering-samples: `develop` is
  the default and integration branch. Cut your branch from `develop` and open
  the pull request against `develop`.
- `main` in those repositories is the released state. It moves only through a
  release pull request from `develop`.
- TechEngine and `.github` work on `main`: branch from it and target it.
- Name work branches `feat/*`, `data/*`, `fix/*`, `chore/*`, `docs/*` or `ci/*`.

## Titles and commits

Pull request titles and commits follow
[Conventional Commits](https://www.conventionalcommits.org/), for example
`feat(data/cpu): add EPYC Rome SKUs` or `fix(validate): reject empty slugs`.

## Data and sources

- Every data record needs `source_urls` with at least one canonical reference.
- Wikipedia (CC BY-SA) and Wikidata (CC0) data may be used.
- Vendor pages are cited as references, not scraped.
- Images come only from Wikimedia Commons.
- One record is one JSON file. Follow the paths and slug rules in the
  repository's README.

## Before you open the pull request

Run the repository's validator, and its tests where it has them. The validator
must pass. The commands are in each README under "Self-check" (TechEngine:
"Quickstart"; TechMachine: "Health check").

Fill in the pull request template. Keep one topic per pull request.

## Checks

- Every pull request runs the repository's checks with a read-only token.
- For an important pull request a maintainer adds the `final-check` label. A
  full check then runs and the TechEngineBot account posts one comment with the
  verdict. You do not need to ask for it.
- Nothing runs on a schedule, and no workflow opens pull requests.

## Licence

By contributing you agree that data is published under CC BY-SA 4.0 and code
under MIT, as stated in each repository.
