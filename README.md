# renovate-config

Shared Renovate configuration for @dnbhq projects.

## Installation

Add a `renovate.json5` file to your repository root:

```json5
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>dnbhq/renovate-config"
  ]
}
```

## Included behavior

This preset provides:

- `config:recommended` base preset
- Semantic commit type set to `chore`
- Dependency Dashboard disabled
- Scheduled updates on weekends (Asia/Bangkok timezone)
- Grouped and auto-merged updates for selected package families
- Lock file maintenance enabled and auto-merged

See [`default.json`](./default.json) for full details.

## Release process

Releases are managed with [`release-it`](https://github.com/release-it/release-it) and [`@release-it/conventional-changelog`](https://github.com/release-it/conventional-changelog):

- `npm run release` → patch release
- `npm run release:minor` → minor release

The process updates `CHANGELOG.md`, creates a signed Git tag, and creates a GitHub release.
