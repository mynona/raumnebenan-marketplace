# raumnebenan Plugin Template & Blueprint

This directory is an **offline blueprint reference** and is not published as an active plugin.

Use this directory as a template to develop new custom **skills** and **agents** for the `raumnebenan` plugin.

## Directory Layout
- **`skills/dummy-skill/`**: Blueprint showing how to structure a reusable skill with frontmatter, workflow steps, references, and MCP tool triggers.
- **`com.github.copilot/agents/dummy-agent.agent.md`**: Blueprint custom Copilot agent template configuring tool permissions (`raumnebenan/*`, `read`, `search`) and system behavior.

## How to Author New Capabilities for `raumnebenan`
1. Copy a skill template folder from here into `../raumnebenan/skills/<your-skill-name>/`.
2. Add `"skills": "skills/"` to `../raumnebenan/plugin.json` and `../../plugin/marketplace.json`.
3. If creating a custom agent, copy the agent template into `../raumnebenan/com.github.copilot/agents/<your-agent-name>.agent.md` and declare `"agents": "com.github.copilot/agents/"` in `marketplace.json`.
