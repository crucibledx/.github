<div align="center">

# Crucible

**Developer tools for teams that ship with AI assistants.**

[![Website](https://img.shields.io/badge/crucibledx.dev-%23e84d00)](https://crucibledx.dev)
[![License: MIT](https://img.shields.io/badge/license-MIT-%23a0aec0)](https://github.com/crucibledx/forge-cli/blob/main/LICENSE)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/crucibledx/assets/raw/main/crucible/diagrams/dark/crucible-ecosystem.svg">
  <img alt="Crucible Ecosystem" src="https://github.com/crucibledx/assets/raw/main/crucible/diagrams/light/crucible-ecosystem.svg" width="800">
</picture>

</div>

---

Your team uses Claude Code, Cursor, Windsurf, Copilot, Cline — maybe all of them. Each tool has its own config format, its own rules location, its own way of doing things.

**Crucible** is a platform of focused CLIs that solve the AI developer experience — from syncing configs across tools, to building and testing the skills those tools consume, to observing how they're actually used.

Each product is independent enough to be useful alone, but shares infrastructure for leverage.

## Products

### Shipped

| Product                                                                        | Description                                                                                            | Links                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **[Forge CLI](https://github.com/crucibledx/forge-cli)**                       | Sync AI assistant configs from a central source to every tool, in the right format                     | [Docs](https://crucibledx.dev/forge/commands) · [Install](https://crucibledx.dev/getting-started/installation) |
| **[Forge Skills Starter](https://github.com/crucibledx/forge-skills-starter)** | Convention-over-configuration platform for designing, developing, testing, and delivering AI resources | [Docs](https://crucibledx.dev/starter/overview)                                                                |

### Researched

| Product   | Description                                                                        |
|-----------|------------------------------------------------------------------------------------|
| **Ember** | Cross-tool AI assistant observability — Prometheus-model collector for AI sessions |

### Planned

| Product     | Description                                                                               |
|-------------|-------------------------------------------------------------------------------------------|
| **Smelt**   | Shared plugin engine library — will be extracted from Forge when a second consumer exists |
| **Anvil**   | Plugin development SDK — types, validation, and testing utilities                         |
| **Lathe**   | MCP server — exposes Forge commands as MCP tools for AI assistants                        |
| **Foundry** | Plugin registry and marketplace — discover, share, and install community resources        |
| **Cast**    | Frontend/embed scaffolding CLI — micro-frontend patterns powered by Smelt                 |

## Forge CLI at a Glance

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/crucibledx/assets/raw/main/forge/demos/dark/01-set-and-forget.gif">
  <img alt="Forge CLI — set and forget" src="https://github.com/crucibledx/assets/raw/main/forge/demos/light/01-set-and-forget.gif" width="720">
</picture>

```bash
forge init    # wizard detects your AI tools, configures a source
forge sync    # pulls files, transforms & places them for each tool
forge health  # dashboard: sync status, drift, source reachability
```

- **12 commands** — init, sync, status, health, config, source management, scheduler, telemetry, uninstall
- **5 assistants** — Claude Code, Cursor, Windsurf, GitHub Copilot, Cline
- **2 source types** — git, local
- **3 layouts** — canonical, pre-structured, hybrid (auto-detected)
- **687 tests**, 6,369 LOC production code

## How It All Connects

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/crucibledx/assets/raw/main/ember/diagrams/dark/ember-closed-loop.svg">
  <img alt="Forge → Ember → Skills Starter — closed loop" src="https://github.com/crucibledx/assets/raw/main/ember/diagrams/light/ember-closed-loop.svg">
</picture>

**Skills Starter** builds the resources (skills, rules, workflows) with a full engineering lifecycle — design, develop, test against real code specimens, version, release.

**Forge CLI** delivers those resources to every developer's machine, transformed into the right format for each AI tool.

**Ember** (researched) will measure how those resources are actually used, closing the feedback loop.

## Technology

- **TypeScript + Bun** — fast iteration, single native binary via `bun build --compile`
- **DDD architecture** — domain / application / infrastructure layering
- **MIT licensed** — maximum adoption

## Get Started

```bash
# Install Forge CLI
curl -fsSL https://crucibledx.dev/install.sh | bash

# Or via npm
npm i -g @crucibledx/forge-cli

# Initialize in your project
forge init
```

📖 **[Documentation](https://crucibledx.dev)** · 🛠️ **[Forge CLI](https://github.com/crucibledx/forge-cli)** · 📐 **[Skills Starter](https://github.com/crucibledx/forge-skills-starter)**
