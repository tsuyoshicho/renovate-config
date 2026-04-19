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

- `default`: main config with best practices, reviewers, semantic commits, vulnerability alerts.
- `schedule`: timezone Asia/Tokyo, lock file maintenance every weekend, automerge weekends.
- `automerge`: platform automerge enabled, rules for patch, dev minor, dev major.
- `docker`: rules for Docker images, follow latest tags with SHA pin, automerge on weekends.
