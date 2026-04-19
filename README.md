# renovate-config

## usage

store in `.github/renovate.json`.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "local>tsuyoshicho/renovate-config"
  ]
}
```

For repositories where you want platform-based GitHub automerge, use:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "local>tsuyoshicho/renovate-config:platform-automerge"
  ]
}
```

## presets

- `default`: main config with best practices, reviewers, semantic commits, vulnerability alerts, platformAutomerge off.
- `schedule`: timezone Asia/Tokyo, PR creation on weekday nights, automerge weekends.
- `automerge`: rules for patch, dev minor, dev major; platformAutomerge is not enabled in the default preset.
- `docker`: rules for Docker images, follow latest tags with SHA pin, reviewer required, automerge on weekends after approval.
- `platform-automerge`: alternate entrypoint name that extends the default config and enables platformAutomerge.
  - ⚠️ **Important**: This preset enables automerge for major updates to dev dependencies. Branch protection and CI approval requirements are mandatory for safe operation.
  - Use this preset only if your repository has branch protection with required CI status checks configured.
