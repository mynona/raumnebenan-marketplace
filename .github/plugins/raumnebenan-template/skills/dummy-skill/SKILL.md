---
name: dummy-skill
description: "Blueprint template for a raumnebenan skill. Demonstrates how to structure instructions, invoke tools, and reference documentation."
compatibility: "GitHub Copilot Chat & Claude"
tags:
  - "product-thinking"
  - "template"
  - "blueprint"
---

# Dummy Skill (Blueprint)

This is a blueprint skill template showing how to structure a reusable agent skill for the raumnebenan plugin.

## Purpose
Use this skill as a template to create real skills (such as article discovery, method guides, or workshop facilitation).

## When to Trigger
Invoke this skill when:
- The user requests a template or reference for creating a new skill.
- The user asks how skills interact with the `https://www.raumnebenan.de/mcp` server.

## Workflow Steps

1. **Understand User Intent**:
   - Determine what product thinking concept, method, or article the user is inquiring about.

2. **Access MCP Tooling**:
   - When tools from the `raumnebenan` MCP server are available, query relevant resources or endpoints:
     - `search_articles` to find articles by keyword.
     - `get_article_details_by_slugs` to read full markdown content.
     - `list_glossary` for terminology definitions.

3. **Synthesize & Ground Advice**:
   - Provide clear, actionable product management or design thinking recommendations.
   - Refer to [references/reference.md](references/reference.md) for domain conventions and formatting standards.

4. **Response Format**:
   - Keep answers structured with headers, bullet points, and actionable next steps.
