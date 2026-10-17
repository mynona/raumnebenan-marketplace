# raumnebenan Marketplace Plugin

Marketplace repository for **raumnebenan** agent plugins, skills, custom agents, and MCP server connectivity.

Provides product thinking knowledge, frameworks, user research guidelines, and terminology from [raumnebenan.de](https://www.raumnebenan.de).

---

## 🚀 Quick Install Guide

### 💻 1. For VS Code Users (Recommended — Takes 30 seconds)

You can add the `raumnebenan` plugin to GitHub Copilot in VS Code in 3 simple steps:

1. **Open Settings**:  
   Press `Cmd + Shift + P` (Mac) or `Ctrl + Shift + P` (Windows/Linux), type:  
   `Preferences: Open User Settings (JSON)` and press **Enter**.
2. **Add the Marketplace**:  
   Add this entry to your `settings.json`:
   ```json
   "chat.plugins.marketplaces": [
     "https://github.com/mynona/raumnebenan-marketplace"
   ]
   ```
   Save the file (`Cmd + S` / `Ctrl + S`).
3. **Install the Plugin**:  
   Press `Cmd + Shift + P` (or `Ctrl + Shift + P`), type:  
   `Chat: Manage Plugins` (or open **Agent Customizations → Plugins**).  
   Find **raumnebenan** and click **Install**.

*That's it! The raumnebenan knowledge base and tools are now active in your Copilot Chat.*

---

### ⚡ 2. For Terminal / GitHub CLI Users

If you use the `gh` command-line tool:

```bash
gh copilot plugin marketplace add mynona/raumnebenan-marketplace
gh copilot plugin install raumnebenan
```

---

### 🤖 3. For Claude Users

#### Claude Code CLI:
```bash
claude mcp add raumnebenan https://www.raumnebenan.de/mcp
```
*(Or simply open this repository in Claude Code — it will auto-detect `.mcp.json` automatically).*

#### Claude Desktop:
Add the following to your `claude_desktop_config.json`:

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

## 📦 What's Included

- **MCP Server**: Pre-configured connection to `https://www.raumnebenan.de/mcp` providing:
  - `search_articles`: Search articles on product thinking & agile methods.
  - `get_article_details_by_slugs`: Retrieve full article markdown content.
  - `list_glossary`: Access comprehensive definitions for product management & user research terms.
  - `list_categories` & `get_stories_by_category`: Browse the Product Thinking pillars (foundation, sense, focus, discover, deliver).

---

## 🛠 Repository Structure

```
.
├── .github/
│   ├── CODEOWNERS                           # Code ownership (@mynona)
│   ├── plugin/
│   │   └── marketplace.json                 # Marketplace catalog
│   └── plugins/
│       ├── raumnebenan/                     # The published plugin package
│       │   ├── plugin.json                  # Manifest (Agent Plugins v1.1.0)
│       │   ├── mcp.json                     # MCP server config (https://www.raumnebenan.de/mcp)
│       │   ├── README.md                    # Package documentation
│       │   └── CHANGELOG.md                 # Version changelog
│       └── raumnebenan-template/            # Offline blueprint reference for skills & agents
│           ├── skills/                      # Skill templates
│           └── com.github.copilot/          # Agent templates
├── .mcp.json                                # MCP config for local workspace & Claude Code
├── LICENSE                                  # MIT license
└── README.md                                # Root documentation
```

---

## 📄 License
MIT License. See [LICENSE](LICENSE) for details.
