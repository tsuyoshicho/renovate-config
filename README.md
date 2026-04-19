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

## presets

- `default`: main config with best practices, reviewers, semantic commits, vulnerability alerts, platformAutomerge off.
- `schedule`: timezone Asia/Tokyo, PR creation on weekday nights, automerge weekends.
- `automerge`: rules for patch, dev minor, dev major; platformAutomerge is not enabled in the default preset.
- `docker`: rules for Docker images, follow latest tags with SHA pin, reviewer required, automerge on weekends after approval.
- `renovate-automerge-config`: alternate entrypoint that extends the default config and enables platformAutomerge.
