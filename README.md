# raumnebenan Marketplace Plugin

Marketplace repository for **raumnebenan** agent plugins, skills, custom agents, and MCP server connectivity.

Provides product thinking knowledge, frameworks, user research guidelines, and terminology from [raumnebenan.de](https://www.raumnebenan.de).

---

## 🚀 Installation

### 1. GitHub Copilot (VS Code & GitHub CLI)

Add the marketplace catalog to GitHub Copilot:
```bash
gh copilot plugin marketplace add mynona/raumnebenan-marketplace
```

Install the `raumnebenan` plugin:
```bash
gh copilot plugin install raumnebenan
```

---

### 2. Claude Code CLI

Add the MCP server directly to Claude Code:
```bash
claude mcp add raumnebenan https://www.raumnebenan.de/mcp
```

Or, if working inside this repository, Claude Code automatically discovers the root `.mcp.json`.

---

### 3. Claude Desktop

Add the following to your `claude_desktop_config.json` (on macOS: `~/Library/Application Support/Claude/claude_desktop_config.json`, on Windows: `%APPDATA%\Claude\claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "raumnebenan": {
      "type": "http",
      "url": "https://www.raumnebenan.de/mcp"
    }
  }
}
```

---

### 4. VS Code Extension (Official Marketplace)

You can package and publish this repository directly as a VS Code Extension contributing the agent plugin:

```bash
# Package extension into .vsix
npm run package

# Publish to Visual Studio Marketplace (requires personal access token)
npm run publish
```

---

## 📦 What's Included

- **MCP Server**: Pre-configured connection to `https://www.raumnebenan.de/mcp` providing:
  - `search_articles`: Search articles on product thinking & agile methods.
  - `get_article_details_by_slugs`: Retrieve full article markdown content.
  - `list_glossary`: Access comprehensive definitions for product management & user research terms.
  - `list_categories` & `get_stories_by_category`: Browse the Product Thinking pillars (foundation, sense, focus, discover, deliver).
- **Blueprint Skill**: [dummy-skill](.github/plugins/raumnebenan/skills/dummy-skill/SKILL.md) for easily authoring new skills.
- **Blueprint Agent**: [dummy-agent](.github/plugins/raumnebenan/com.github.copilot/agents/dummy-agent.agent.md) for customizing subagents with MCP tool permissions.

---

## 🛠 Repository Structure

```
.
├── .github/
│   ├── CODEOWNERS                           # Code ownership (@mynona)
│   ├── plugin/
│   │   └── marketplace.json                 # Marketplace catalog
│   └── plugins/
│       └── raumnebenan/                     # The raumnebenan plugin package
│           ├── plugin.json                  # Manifest (Agent Plugins v1.1.0)
│           ├── mcp.json                     # MCP server config (https://www.raumnebenan.de/mcp)
│           ├── README.md                    # Package documentation
│           ├── CHANGELOG.md                 # Version changelog
│           ├── LICENSE                      # MIT license
│           ├── skills/                      # Bundled skills
│           │   └── dummy-skill/
│           └── com.github.copilot/          # Copilot-specific contributions
│               └── agents/
│                   └── dummy-agent.agent.md
├── .mcp.json                                # MCP config for local workspace & Claude Code
├── package.json                             # VS Code Extension manifest for vsce packaging
├── LICENSE                                  # MIT license
└── README.md                                # Root documentation
```

---

## 📄 License
MIT License. See [LICENSE](LICENSE) for details.
