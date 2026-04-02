# OpenTweet Plugin for Claude Code

Manage your X/Twitter presence directly from Claude Code. Create tweets, schedule posts, manage evergreen queues, view analytics, and more.

## Installation

### From the OpenTweet marketplace

```bash
# Add the marketplace (one-time)
/plugin marketplace add opentweetio/claude-code-plugin

# Install the plugin
/plugin install opentweet@opentweet-claude-code-plugin
```

You'll be prompted for your OpenTweet API key during installation. Get one at [opentweet.io/developer](https://opentweet.io/developer).

### Local development

```bash
claude --plugin-dir ./path/to/opentweet-claude-code-plugin
```

## Slash Commands

| Command | Description |
|---------|-------------|
| `/opentweet:tweet <topic>` | Create and schedule a tweet |
| `/opentweet:analytics [overview\|best-times\|tweets]` | View posting analytics and insights |
| `/opentweet:schedule [days]` | Review and schedule draft tweets |
| `/opentweet:evergreen [status\|add\|history]` | Manage your evergreen tweet queue |

## Features

- **19 MCP tools** for full Twitter/X management
- **Smart scheduling** with optimal posting time suggestions
- **Evergreen queue** management for automatic content recycling
- **Multi-account support** for managing multiple X accounts
- **Analytics** with posting stats, streaks, and engagement data

## How It Works

This plugin connects to the [OpenTweet](https://opentweet.io) API via the hosted MCP endpoint at `https://opentweet.io/mcp`. No local server or npm packages needed.

## Requirements

- An [OpenTweet](https://opentweet.io) account with an active subscription
- An API key from [opentweet.io/developer](https://opentweet.io/developer)

## Links

- [OpenTweet](https://opentweet.io)
- [API Documentation](https://opentweet.io/developer)
- [MCP Server (npm)](https://www.npmjs.com/package/@opentweet/mcp-server)

## License

MIT
