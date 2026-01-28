# opencode-discord-notification

OpenCode plugin that sends Discord notifications on session completion and permission requests.

![Example Notification](screenshots/example.png)

## Features

- ✅ **Completion Notifications:** Get a Discord message when OpenCode finishes a long task.
- 📊 **Context Stats:** Includes context usage percentage and total tokens.
- 🤖 **Model Info:** Shows which model was used for the response.
- ⚠️ **Permission Alerts:** Real-time notifications when OpenCode is blocked waiting for terminal permissions, including the command it's trying to run.

## Installation

Add it to your `opencode.json`:

```json
{
  "plugin": ["opencode-discord-notification@0.1.1"]
}
```

## Configuration

Add the following section to your `opencode.json`:

```json
{
  "discordNotifications": {
    "enabled": true,
    "webhookUrl": "https://discord.com/api/webhooks/...",
    "username": "OpenCode Notifier",
    "avatarUrl": "https://opencode.ai/logo.png"
  }
}
```

> **Note:** If your OpenCode version has strict schema validation and doesn't allow the `discordNotifications` key, the plugin will also look for a configuration file at `~/.config/opencode/plugins/discord-notification-config.json`.

## Development

1. Clone the repo.
2. Install dependencies: `bun install`.
3. Type-check: `bun x tsc`.

## License

MIT
