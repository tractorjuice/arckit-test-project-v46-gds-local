# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project: GDS Local

Architecture governance project for GDS Local using the **ArcKit plugin** (v2.4.5). This is a documentation-only repository — there are no build, lint, or test commands. All functionality comes from ArcKit slash commands.

## Setup

The ArcKit plugin is auto-enabled via `.claude/settings.json`. In GitHub Codespaces, Claude Code installs automatically via `.devcontainer/devcontainer.json`. Run `/arckit.init` to verify the plugin is working.

## ArcKit Commands

48 slash commands are available via the ArcKit plugin. Key starting commands:

- `/arckit.plan` - Project planning (Tier 0, no dependencies)
- `/arckit.principles` - Architecture principles (Tier 0, no dependencies)
- `/arckit.stakeholders` - Stakeholder analysis (needs principles)
- `/arckit.risk` - Risk assessment (needs stakeholders)
- `/arckit.sobc` - Strategic Outline Business Case (needs stakeholders, risk)
- `/arckit.requirements` - Requirements specification (needs stakeholders, sobc)
- `/arckit.adr` - Architecture Decision Records
- `/arckit.diagram` - Architecture diagrams (C4, sequence, etc.)
- `/arckit.analyze` - Quality analysis across all artifacts
- `/arckit.story` - Comprehensive project narrative (run last)
- `/arckit.pages` - Generate GitHub Pages documentation site

Full command reference: https://tractorjuice.github.io/arc-kit/

## Command Execution Order

Commands have a strict dependency hierarchy. The three most-consumed artifacts are:

1. **Requirements** (`ARC-*-REQ-*.md`) — consumed by 38 commands (mandatory for most)
2. **Principles** (`ARC-000-PRIN-v*.md`) — consumed by 21 commands
3. **Stakeholders** (`ARC-*-STKE-*.md`) — consumed by 23 commands

Always produce these foundation artifacts before running downstream commands. See `DEPENDENCY-MATRIX.md` for the full dependency structure matrix and `WORKFLOW-DIAGRAMS.md` for visual workflow paths.

### Recommended Critical Path (UK Government)

```
plan -> principles -> stakeholders -> risk -> sobc -> requirements -> datascout -> data-model -> research -> wardley -> gcloud-search -> gcloud-clarify -> evaluate -> hld-review -> dld-review -> backlog -> servicenow -> devops -> operationalize -> traceability -> tcop -> secure -> principles-compliance -> analyze -> service-assessment -> story
```

Other paths exist for Standard (non-government), UK Gov AI, MOD Defence, and MOD Defence AI projects — see `WORKFLOW-DIAGRAMS.md`.

## Project Structure

- `projects/000-global/` — Cross-project artifacts (principles, standards shared across all projects)
- `projects/001-*/` — Numbered project directories containing architecture documents
- `docs/` — Documentation and guides

## Document Naming Convention

All documents follow: `ARC-{PROJECT_ID}-{TYPE_CODE}-v{VERSION}.md`

- Single-instance: `ARC-001-REQ-v1.0.md` (requirements for project 001)
- Multi-instance (ADR, DIAG, WARD, DMC): `ARC-001-ADR-001-v1.0.md`
- Principles are global: `ARC-000-PRIN-v1.0.md`

## External Dependencies

Some commands require external services:
- `/arckit.azure-research` — requires Microsoft Learn MCP server
- `/arckit.aws-research` — requires AWS Knowledge MCP server
- `/arckit.gcp-research` — requires Google Developer Knowledge MCP server + `GOOGLE_API_KEY`
- `/arckit.trello` — requires `TRELLO_API_KEY` and `TRELLO_TOKEN` environment variables
- HLD/DLD documents are created externally and validated by `/arckit.hld-review` and `/arckit.dld-review`
