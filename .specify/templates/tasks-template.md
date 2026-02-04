---
description: "Task list template for feature implementation"
---

# Tasks: [FEATURE NAME]

**Input**: Design documents from `/specs/[###-feature-name]/`  
**Prerequisites**: `plan.md` (required), `spec.md` (required for user stories), `research.md`, `data-model.md`, `contracts/`

**Tests**: The examples below include test tasks. Tests are **OPTIONAL** — only include them if explicitly requested in the feature specification.

**Organization**: Tasks are grouped by **user story** to enable independent implementation and testing of each story.

---

## Format

`[ID] [P?] [Story] Description`

- **[P]**: Can run in parallel (different files, no dependencies)
- **[Story]**: Which user story this task belongs to (e.g., US1, US2, US3)
- Descriptions MUST include **exact file paths**

---

## Path Conventions

- **Single project**: `src/`, `tests/` at repository root
- **Web app**: `backend/src/`, `frontend/src/`
- **Mobile**: `api/src/`, `ios/src/` or `android/src/`
- Paths below assume **single project** — adjust based on `plan.md`

<!--
============================================================================
IMPORTANT: SAMPLE TASKS ONLY

The `/speckit.tasks` command MUST replace these with real tasks derived from:
- User stories from `spec.md` (with priorities P1, P2, P3…)
- Feature requirements from `plan.md`
- Entities from `data-model.md`
- Endpoints / interfaces from `contracts/`

Tasks MUST be grouped by user story so each story can be:
- Implemented independently
- Tested independently
- Delivered as an MVP increment

DO NOT keep these sample tasks in the generated `tasks.md` file.
============================================================================
-->

---

## Phase 1: Setup (Shared Infrastructure)

**Purpose**: Project initialization and baseline structure

- [ ] T001 Create project structure per implementation plan
- [ ] T002 Initialize [language] project with [framework] dependencies
- [ ] T003 [P] Configure linting and formatting tools

---

## Phase 2: Foundational (Blocking Prerequisites)

**Purpose**: Core infrastructure that MUST be complete before ANY user story work

**⚠️ CRITICAL**: No user story implementation may begin until this phase is complete

Examples (adjust to your project):

- [ ] T004 Set up database schema and migrations framework
- [ ] T005 [P] Implement authentication / authorization framework
- [ ] T006 [P] Set up API routing and middleware structure
- [ ] T007 Create base models/entities shared by all stories
- [ ] T008 Configure error handling and logging infrastructure
- [ ] T009 Set up environment configuration management

**Checkpoint**: Foundation ready — user stories may now proceed in parallel

---

## Phase 3: User Story 1 — [Title] (Priority: P1) 🎯 MVP

**Goal**: [What this story delivers]

**Independent Test**: [How to verify this story works on its own]

### Tests for User Story 1 (OPTIONAL — only if requested) ⚠️

> Tests MUST be written first and MUST fail before implementation.

- [ ] T010 [P] [US1] Contract test for [endpoint] in `tests/contract/test_[name].py`
- [ ] T011 [P] [US1] Integration test for [journey] in `tests/integration/test_[name].py`

### Implementation — User Story 1

- [ ] T012 [P] [US1] Create `[Entity1]` model in `src/models/[entity1].py`
- [ ] T013 [P] [US1] Create `[Entity2]` model in `src/models/[entity2].py`
- [ ] T014 [US1] Implement `[Service]` in `src/services/[service].py` (depends on T012, T013)
- [ ] T015 [US1] Implement `[endpoint/feature]` in `src/[location]/[file].py`
- [ ] T016 [US1] Add validation and error handling
- [ ] T017 [US1] Add logging for User Story 1 operations

**Checkpoint**: User Story 1 is fully functional and independently testable

---

## Phase 4: User Story 2 — [Title] (Priority: P2)

**Goal**: [What this story delivers]

**Independent Test**: [How to verify this story works on its own]

### Tests for User Story 2 (OPTIONAL) ⚠️

- [ ] T018 [P] [US2] Contract test in `tests/contract/test_[name].py`
- [ ] T019 [P] [US2] Integration test in `tests/integration/test_[name].py`

### Implementation — User Story 2

- [ ] T020 [P] [US2] Create `[Entity]` model in `src/models/[entity].py`
- [ ] T021 [US2] Implement `[Service]` in `src/services/[service].py`
- [ ] T022 [US2] Implement `[endpoint/feature]` in `src/[location]/[file].py`
- [ ] T023 [US2] Integrate with User Story 1 components (if needed)

**Checkpoint**: User Stories 1 and 2 work independently

---

## Phase 5: User Story 3 — [Title] (Priority: P3)

**Goal**: [What this story delivers]

**Independent Test**: [How to verify this story works on its own]

### Tests for User Story 3 (OPTIONAL) ⚠️

- [ ] T024 [P] [US3] Contract test in `tests/contract/test_[name].py`
- [ ] T025 [P] [US3] Integration test in `tests/integration/test_[name].py`

### Implementation — User Story 3

- [ ] T026 [P] [US3] Create `[Entity]` model in `src/models/[entity].py`
- [ ] T027 [US3] Implement `[Service]` in `src/services/[service].py`
- [ ] T028 [US3] Implement `[endpoint/feature]` in `src/[location]/[file].py`

**Checkpoint**: All user stories are independently functional

---

## Phase N: Polish & Cross-Cutting Concerns

**Purpose**: Improvements spanning multiple stories

- [ ] TXXX [P] Documentation updates
- [ ] TXXX Code cleanup and refactoring
- [ ] TXXX Performance optimization
- [ ] TXXX [P] Additional unit tests in `tests/unit/` (if requested)
- [ ] TXXX Security hardening
- [ ] TXXX Validate `quickstart.md`

---

## Dependencies & Execution Order

### Phase Dependencies

- **Phase 1 (Setup)**: No dependencies
- **Phase 2 (Foundational)**: Depends on Phase 1 — BLOCKS all stories
- **Phase 3+ (User Stories)**: Depend on Phase 2
- **Final Phase (Polish)**: Depends on desired stories being complete

### User Story Dependencies

- **US1 (P1)**: No dependencies after Foundation
- **US2 (P2)**: May integrate with US1 but must remain independently testable
- **US3 (P3)**: May integrate with US1/US2 but must remain independently testable

### Within Each User Story

- Tests (if included) → MUST fail first
- Models → Services → Endpoints
- Core logic before integration
- Story must pass independent validation before moving on

---

## Parallel Opportunities

- All `[P]` tasks can run in parallel
- Different user stories can be worked on concurrently
- Models within the same story can be parallelized
- Tests within the same story can be parallelized

---

## Parallel Example — User Story 1

```bash
# Tests (if requested)
Contract test for endpoint
Integration test for user journey

# Models
Create Entity1 model
Create Entity2 model
```

### Implementation Strategy
#### MVP-First

- Phase 1 — Setup

- Phase 2 — Foundational (BLOCKING)

- Phase 3 — User Story 1

- STOP & VALIDATE

- Deploy / demo MVP

### Incremental Delivery

- Add one user story at a time

- Validate independently

- Deploy independently

- Never break previous stories

### Parallel Team Strategy

- Team completes Setup + Foundation together

- After Foundation:

   - Dev A → US1

    - Dev B → US2

  - Dev C → US3

### Notes

- [P] = safe parallel execution

- [US#] = explicit story ownership

- Avoid vague tasks

- Avoid cross-story file conflicts

- Commit frequently

- Validate at every checkpoint