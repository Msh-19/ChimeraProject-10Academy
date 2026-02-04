# Feature Specification: [FEATURE NAME]

**Feature Branch**: `[###-feature-name]`  
**Created**: [YYYY-MM-DD]  
**Status**: Draft  
**Input**: User description: "$ARGUMENTS"

---

## User Scenarios & Testing *(MANDATORY)*

<!--
IMPORTANT:
- User stories MUST be prioritized as independent user journeys.
- Each story must be independently developable, testable, deployable, and demo-able.
- Implementing any single P1 story must result in a viable MVP.
- Priorities: P1 (critical), P2 (important), P3 (nice-to-have).
-->

### User Story 1 — [Brief Title] (Priority: P1)

[Describe this user journey in clear, plain language.]

**Why this priority**:  
[Explain the value delivered and why this story is critical.]

**Independent Test**:  
[Describe how this story can be fully tested on its own and what value it proves.]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]  
2. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

### User Story 2 — [Brief Title] (Priority: P2)

[Describe this user journey in plain language.]

**Why this priority**:  
[Explain the value and why it has this priority level.]

**Independent Test**:  
[Describe how this can be tested independently.]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

### User Story 3 — [Brief Title] (Priority: P3)

[Describe this user journey in plain language.]

**Why this priority**:  
[Explain the value and why it has this priority level.]

**Independent Test**:  
[Describe how this can be tested independently.]

**Acceptance Scenarios**:

1. **Given** [initial state], **When** [action], **Then** [expected outcome]

---

> Add additional user stories as needed.  
> Every story MUST have a priority and an independent test definition.

---

## Edge Cases

<!--
ACTION REQUIRED:
Replace the placeholders below with real edge cases derived from the feature context.
-->

- What happens when [boundary condition is exceeded]?
- How does the system behave when [external dependency fails]?
- What occurs if [invalid or unexpected input] is provided?

---

## Requirements *(MANDATORY)*

<!--
ACTION REQUIRED:
Replace all placeholder requirements with explicit, testable statements.
-->

### Functional Requirements

- **FR-001**: System MUST [specific, testable capability]
- **FR-002**: System MUST [specific validation or rule]
- **FR-003**: Users MUST be able to [key interaction]
- **FR-004**: System MUST [data persistence or processing requirement]
- **FR-005**: System MUST [observable behavior or side effect]

#### Handling Ambiguity (REQUIRED)

Use `[NEEDS CLARIFICATION]` for any unknowns. Do NOT guess.

- **FR-006**: System MUST authenticate users via  
  `[NEEDS CLARIFICATION: auth method not specified — email/password, SSO, OAuth?]`
- **FR-007**: System MUST retain user data for  
  `[NEEDS CLARIFICATION: retention period not specified]`

---

### Key Entities *(Include only if the feature involves data)*

- **[Entity 1]**:  
  [What it represents, key attributes, and constraints — no implementation details]

- **[Entity 2]**:  
  [What it represents and its relationship to other entities]

---

## Success Criteria *(MANDATORY)*

<!--
ACTION REQUIRED:
Success criteria MUST be measurable, technology-agnostic, and verifiable.
-->

### Measurable Outcomes

- **SC-001**: [User outcome metric — e.g., task completion time, success rate]
- **SC-002**: [System performance metric — e.g., throughput, latency]
- **SC-003**: [Quality or reliability metric — e.g., error rate, retries]
- **SC-004**: [Business or operational metric — e.g., cost reduction, adoption]

---

## Specification Status

- **Ready for Planning**: ☐ YES ☐ NO  
- **Blocking Clarifications**: [List FR/SC IDs or NONE]  
- **Reviewed By**: [Agent / Human]  
- **Last Review Date**: [YYYY-MM-DD]
