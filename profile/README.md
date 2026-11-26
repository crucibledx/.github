<div align="center">

# Crucible

**Ship shared context. Trace agent work.**

[![Website](https://img.shields.io/badge/crucibledx.dev-%23e84d00)](https://crucibledx.dev)
[![License: MIT](https://img.shields.io/badge/license-MIT-%23a0aec0)](https://github.com/crucibledx/forge-cli/blob/main/LICENSE)

</div>

Crucible builds open-source infrastructure for coding harnesses. Forge distributes skills, rules, and workflows across your tools. Ember reconstructs agent session trees and groups cross-harness work with `ember.work.id`.

**Don't compete. Complete.** Each product integrates with the coding harnesses and observability backends developers already use.

## Products

| Product | Status | Description | Links |
| --- | --- | --- | --- |
| **[Forge CLI](https://github.com/crucibledx/forge-cli)** | Shipped (v0.7.0) | Distributes skills, rules, and workflows from Git or local sources to coding harnesses | [Docs](https://crucibledx.dev/forge) · [Install](https://crucibledx.dev/getting-started/installation) |
| **[Forge Skills Starter](https://github.com/crucibledx/forge-skills-starter)** | Shipped | Convention-based template for building, testing, and delivering agent resources | [Docs](https://crucibledx.dev/starter/overview) |
| **[Ember](https://github.com/crucibledx/ember)** | In development | Go OpenTelemetry Collector distribution for session trees, usage, MCP, and work attribution | [Overview](https://crucibledx.dev/ember) |
| **Smelt** | Designed | Shared plugin engine library | [Roadmap](https://crucibledx.dev/platform/roadmap) |
| **Anvil** | Designed | SDK for third-party plugin development | [Roadmap](https://crucibledx.dev/platform/roadmap) |
| **Lathe** | Designed | MCP server that exposes Forge commands as MCP tools | [Roadmap](https://crucibledx.dev/platform/roadmap) |
| **Foundry** | Designed | Plugin registry and marketplace for community resources | [Roadmap](https://crucibledx.dev/platform/roadmap) |
| **Cast** | Designed | Frontend and embed scaffolding CLI | [Roadmap](https://crucibledx.dev/platform/roadmap) |

## Forge CLI at a glance

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/crucibledx/assets/raw/main/forge/demos/dark/01-set-and-forget.gif">
  <img alt="Forge CLI — set and forget" src="https://github.com/crucibledx/assets/raw/main/forge/demos/light/01-set-and-forget.gif" width="720">
</picture>

```bash
forge init    # detect coding harnesses and configure a source
forge sync    # transform and place resources for each harness
forge health  # sync status, drift, and source reachability
```

- **12 commands** — init, sync, status, health, config, source management, scheduler, telemetry, uninstall
- **5 coding harnesses** — Claude Code, Cursor, Windsurf, GitHub Copilot, Cline
- **2 source types** — Git and local directories
- **3 layouts** — canonical, pre-structured, and hybrid, auto-detected
- **Transactional writes** — dry-run, backups, drift detection, and rollback with explicit incomplete-recovery reporting

Forge v0.8 will add Agent Plugins 1.0 delivery through Droid and Claude Code first. The v0.9 compiler remains roadmap work; its detailed capabilities are not yet approved.

## Ember

Ember is written in Go as a custom OpenTelemetry Collector distribution. Machine agents and an optional gateway reconstruct one trace tree per session or workstream across processes and machines. `ember.work.id` groups related work across coding harnesses.

The initial design supports Droid and Claude Code, standard OTLP export to existing backends, usage and MCP attribution, and content capture off by default.

## Get started

```bash
# Homebrew
brew install crucibledx/tap/forge

# npm (requires Bun 1.4.2 or later)
npm install -g @crucibledx/forge-cli

# Configure a source and sync
forge init
forge sync
```

**[Documentation](https://crucibledx.dev)** · **[Products](https://crucibledx.dev/platform/products)** · **[Roadmap](https://crucibledx.dev/platform/roadmap)**
