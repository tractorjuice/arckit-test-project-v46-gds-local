# GDS Local

GDS Local

## Overview

This repository uses **ArcKit v2.4.5** for enterprise architecture governance and documentation.

## Getting Started

### Prerequisites

- [Claude Code](https://claude.ai/code) installed
- GitHub Codespaces (recommended) or local development environment

### Setup

1. Open this repo in a GitHub Codespace (or clone locally)
2. Claude Code will auto-install via `.devcontainer/devcontainer.json`
3. The ArcKit plugin is auto-enabled via `.claude/settings.json`
4. Restart Claude Code once to resolve the marketplace plugin

### First Commands

```bash
# Check ArcKit is working
/arckit.init

# Define architecture principles (if not already done)
/arckit.principles

# Start with stakeholder analysis
/arckit.stakeholders GDS Local

# Generate requirements
/arckit.requirements GDS Local
```

## Project Structure

```
projects/
├── 000-global/          # Cross-project artifacts (principles, standards)
└── 001-gds-local/ # Project-specific artifacts (created by commands)
```

## Available Commands

This project uses the ArcKit plugin which provides 48 slash commands for architecture governance. See the [full command reference](https://tractorjuice.github.io/arc-kit/).

## Links

- [ArcKit Documentation](https://tractorjuice.github.io/arc-kit/)
- [ArcKit Repository](https://github.com/tractorjuice/arc-kit)
- [ArcKit Plugin Marketplace](https://github.com/tractorjuice/arc-kit)