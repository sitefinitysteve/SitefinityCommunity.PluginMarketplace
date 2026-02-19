# SitefinityCommunity Claude Plugin

> **Community-maintained** — This is an unofficial, community-driven plugin. It is not affiliated with or endorsed by Progress Software or the Sitefinity product team.

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces) that provides Sitefinity CMS development skills for Claude Code.

## Available Skills

| Skill | Invocation | Description |
|-------|-----------|-------------|
| **Widget Expert** | `/sitefinity:sitefinity-widget-expert` | MVC widget development, designer configuration, JSON persistence, and Sitefinity 4.8 best practices |

## Installation

### Add the marketplace

```shell
/plugin marketplace add sitefinitysteve/SitefinityCommunity.ClaudePlugin
```

### Install the plugin

```shell
/plugin install sitefinity@sitefinity-community
```

### Use the skills

Once installed, skills are available as slash commands:

```shell
/sitefinity:sitefinity-widget-expert
```

Claude will also automatically invoke these skills when it recognizes a relevant task (e.g., creating a Sitefinity widget).

## Updating

Pull the latest skills:

```shell
/plugin marketplace update
```

## Adding to a team project

Add the marketplace to your repository's `.claude/settings.json` so team members are automatically prompted to install it:

```json
{
  "extraKnownMarketplaces": {
    "sitefinity-community": {
      "source": {
        "source": "github",
        "repo": "sitefinitysteve/SitefinityCommunity.ClaudePlugin"
      }
    }
  },
  "enabledPlugins": {
    "sitefinity@sitefinity-community": true
  }
}
```

## Local development

Test the plugin locally without installing:

```shell
claude --plugin-dir ./SitefinityCommunity.ClaudePlugin
```

Validate the plugin structure:

```shell
/plugin validate .
```

## Companion: MCP Server

For live Sitefinity diagnostics (logs, status, metadata), pair this plugin with the [SitefinityCommunity MCP Server](https://github.com/SitefinityCommunity/Mcp). The MCP server provides tools for reading error logs, checking site status, listing content types, and more.

## Contributing

To add a new skill:

1. Create a folder under `skills/` with your skill name
2. Add a `SKILL.md` file with frontmatter (`name`, `description`) and instructions
3. Test locally with `claude --plugin-dir .`
4. Submit a pull request

## License

MIT
