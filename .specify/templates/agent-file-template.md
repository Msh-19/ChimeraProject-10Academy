# Project Chimera Development Guidelines

Auto-generated from all feature plans.  
Last updated: 2026-02-04

---

## Active Technologies

> Extracted from approved `plan.md` files and architectural decisions.

- **Language**: Python 3.12+
- **Dependency Management**: `uv`
- **Specification Framework**: GitHub Spec Kit
- **Testing**: `pytest`
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Agent Tooling (Dev-time)**:
  - MCP Sense (traceability)
  - git-mcp
  - filesystem-mcp
- **Runtime Paradigm**:
  - Agent + Skills architecture
  - Contract-first, test-driven
- **Data Layer (Planned / Specified)**:
  - SQL-based relational database (schema-first, migrations required)

Only technologies explicitly declared in specs and plans may be used.

---

## Project Structure

```text
project-chimera/
├── specs/                     # Source of truth (intent)
│   ├── _meta.md
│   ├── functional.md
│   ├── technical.md
│   └── openclaw_integration.md
│
├── skills/                    # Runtime agent capabilities
│   ├── README.md              # Skill index + contracts
│   ├── skill_trend_fetcher/
│   ├── skill_content_generator/
│   └── skill_publisher/
│
├── tests/                     # Test-first enforcement
│   ├── test_trend_fetcher.py
│   ├── test_skills_interface.py
│   └── contracts/
│
├── research/                  # Non-binding context & analysis
│   ├── architecture_strategy.md
│   └── tooling_strategy.md
│
├── .cursor/
│   └── rules                  # Agent behavior rules
│
├── .github/
│   └── workflows/
│       └── main.yml           # CI pipeline
│
├── Dockerfile
├── Makefile
├── pyproject.toml
└── README.md
