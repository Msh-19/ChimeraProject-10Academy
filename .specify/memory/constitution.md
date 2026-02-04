# Project Chimera Constitution
<!-- Specification-Driven Development Constitution -->

## Core Principles

### I. Specification Supremacy (NON-NEGOTIABLE)
Specifications are the single source of truth.

All code, tests, tasks, and infrastructure **must be derived from approved specifications** located in `specs/`.

Rules:
- No implementation code may be written without a corresponding spec
- If code conflicts with specs, **the code is wrong**
- Ambiguities must be surfaced explicitly using `[NEEDS CLARIFICATION]`
- Fixing behavior means updating specs first, then regenerating outputs

This project practices **intent-driven development**. Code exists only as an expression of intent.

---

### II. Test-First Enforcement (RED REQUIRED)
All behavior is defined by tests before implementation.

Rules:
- Tests must be written **before** implementation
- Tests must be reviewed and approved before any code is generated
- Tests must **fail** prior to implementation (Red phase)
- Implementation exists solely to make tests pass (Green phase)
- Refactoring must not change test intent

A passing test suite is evidence of **spec compliance**, not developer success.

---

### III. Contract-First Design
All inter-component behavior must be governed by explicit contracts.

Rules:
- APIs, skills, and data boundaries require defined input/output contracts
- Contracts must be documented before implementation
- JSON schemas are preferred for structured data exchange
- Contract changes require corresponding spec and test updates

Agents may not infer or invent interfaces.

---

### IV. Skill vs Tool Separation
Agent capabilities must be cleanly separated from developer tooling.

Definitions:
- **Skills**: Runtime capabilities used by the Chimera agent (e.g., fetch trends, transcribe audio)
- **Tools (MCP)**: Development-time utilities used by humans or IDE agents (e.g., git, filesystem, database access)

Rules:
- Skills must live under `skills/`
- Each skill must define explicit inputs, outputs, and failure modes
- MCP tools must never be treated as runtime skills
- No hidden side effects across the boundary

---

### V. Simplicity & Anti-Abstraction
Complexity is a liability and must be justified.

Rules:
- Prefer direct framework usage over custom abstractions
- No speculative or “future-proof” features
- Each abstraction must have a clear, current justification
- Fewer components are preferred over “clean” but unnecessary layering

If complexity is introduced, it must be **documented and defended** in the specification.

---

## Architectural Constraints

### Data & State
- Canonical data models must be defined in specifications
- One authoritative schema per domain concept
- Migrations and breaking schema changes require explicit planning

### Execution Model
- Agent behavior must be deterministic given the same inputs
- Non-determinism (e.g., external APIs, time) must be isolated and documented
- Side effects must be observable and testable

### Security & Safety
- Human-in-the-loop approval points must be explicitly defined
- Unsafe actions must be gated by policy and tests
- No autonomous publishing without an approval specification

---

## Development Workflow

### Specification Workflow
1. Intent expressed in natural language
2. Specification created or updated in `specs/`
3. Ambiguities resolved or explicitly marked
4. Specification reviewed and ratified

### Planning Workflow
1. Approved spec is translated into an implementation plan
2. Contracts, schemas, and tests are derived
3. Complexity gates are evaluated

### Execution Workflow
1. Tasks generated from the plan
2. Tests written and confirmed failing
3. Implementation generated to satisfy tests
4. CI validates specification alignment

Agents must **explain their plan** before generating code.

---

## Quality Gates

All changes must pass:
- Specification alignment checks
- Contract validation
- Test suite execution
- CI pipeline verification

Failure at any gate blocks progression.

---

## Governance

This constitution supersedes:
- Individual agent preferences
- Generated plans
- Implementation convenience

Rules:
- All agents must verify compliance before acting
- Violations require updating specifications or requesting amendments
- Constitutional changes require:
  - Written rationale
  - Explicit approval
  - Backward compatibility assessment

Runtime behavior guidance must reference this constitution and the active specifications.

---

**Version**: 1.0.0  
**Ratified**: 2026-02-04  
**Last Amended**: 2026-02-04
