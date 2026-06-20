# clawgenius-agent-creative

Creative studio agent for image, video, audio, and design assets.

## Install

```bash
hermes profile install github.com/sontakey/clawgenius-agent-creative --alias --name creative
```

## Update

```bash
hermes profile update creative
```

## What ships

- `SOUL.md` — profile persona and operating contract
- `skills/` — bundled ClawGenius operating skills
- `mcp.json` — MCP placeholder, intentionally empty until integrations are picked
- `cron/` — cron placeholder, intentionally empty by default
- `distribution.yaml` — manifest and update ownership

## What never ships

No credentials, memories, sessions, logs, workspaces, or local user customization.

## Recommended toolsets

`image_gen, video, vision, file, terminal, skills`

Configure locally after install with:

```bash
hermes -p creative tools
hermes -p creative model
```
