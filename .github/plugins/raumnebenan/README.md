# raumnebenan Plugin

**Version**: 1.0.0

A portable Agent Plugin providing product thinking knowledge, skills, agents, and MCP server connectivity from [raumnebenan.de](https://www.raumnebenan.de).

## Capabilities

### 1. Model Context Protocol (MCP) Server
- **Endpoint**: `https://www.raumnebenan.de/mcp`
- Configured in [mcp.json](mcp.json).
- Provides tools for searching articles, fetching article markdown, exploring stories, and querying product thinking glossary definitions.

### 2. Skills
- Located in [skills/](skills/).
- [dummy-skill](skills/dummy-skill/SKILL.md): Blueprint skill template.

### 3. Agents
- Located in [com.github.copilot/agents/](com.github.copilot/agents/).
- [dummy-agent](com.github.copilot/agents/dummy-agent.agent.md): Blueprint agent template.
