# ADR-XXXX: [Title of the Decision]

**Status**: Proposed | Accepted | Deprecated | Implemented | Rejected | Superseded by ADR-XXXX  
**Priority**: Critical | High | Medium | Low
**Date**: YYYY-MM-DD  
**Authors**: [@github-author]  
**Reviewers**: [@github-reviewer1, @github-reviewer2]  
**Tags**: `#architecture` `#tekton` `#operator` *(optional)*

<!-- Status lifecycle:
- Proposed: Under discussion, not yet accepted
- Accepted: Approved, ready for implementation
- Implemented: Done and reflected in the product
- Deprecated: Not required anymore
- Superseded: Replaced by a newer ADR (link to it)
- Rejected: Not accepted (stays in repo for reference)
-->

## Context

*What’s the business requirement that led to this decision? 
(Any confidential information should be marked `Confidential`)*

- Existing problem
- Constraints (technical, organizational, etc.)
- Business goals or use cases driving this change 
- Systems, teams, or processes impacted

## Decision

*Describe the architectural or design decision that is being made in few lines.*
- Chosen option: `[Option A]` over `[Option B]`

### Architectural Overview

*Briefly describe the high level architecture here.*

- Overview of the chosen solution
- Architecture diagrams if any
- Design patterns used

### Implementation Details

*Briefly describe the high level implementation details here.*

- Explains how the proposed solution will be implemented (high level)
- API specs if any
- Affected components/systems: component-A, component-B

## Scope

*Clearly define the boundaries of this architectural decision here.*

* **In-Scope:**
    * [What this decision explicitly solves or covers]
* **Out-of-Scope:**
    * [Related items that are intentionally left out of this enhancement phase]

## Acceptance Criteria

*Add all the criteria to consider this decision as `Accepted`.*

The decision is considered accepted when:
- [ ] Problem, scope, and non-goals are clear
- [ ] Alternatives were considered and compared
- [ ] Chosen option's trade-offs (not just benefits) are documented
- [ ] Backward compatibility / migration path addressed
- [ ] Security/RBAC impact assessed
- [ ] Observability and rollback plan defined
- [ ] Required reviewers approved 
- [ ] Open concerns resolved or tracked
- [ ] Decision is specific enough to implement without further design work
- [ ] Documented in internal knowledge base

## Considered Options

*Compare all the options considered mentioning the advantages and disadvantages in this section.*

| Option     | Pros                      | Cons                          |
|------------|---------------------------|-------------------------------|
| Option A   | [Advantage 1, 2]          | [Disadvantage 1, 2]           |
| Option B   | [Aligns with X, reusable] | [Requires migration, efforts] |
| Do Nothing | No effort required        | Does not address [key issue]  |

## Decision Drivers

*List out the factors to consider this decision here.*

Key factors influencing this decision:
- Security and compliance
- Scalability or performance needs
- Team expertise and maintainability
- Complexity or efforts required

## Consequences

*List out the Short-term and long-term effects here.*

- Positive outcomes:
    - [Improved reliability/performance]
    - [Better user experience]
- Risks:
    - [Security concerns]
    - [Development overhead]
    - [Challenges]
- Technical debt or follow-up ADRs required

## References

*Define all the references, docs, JIRAs, ADRs, etc. here.*

- [ADR-0000: Referenced ADR](./0000-adr-template.md)
- [Performance improvement strategies](https://example.com/docs/sample)
- [JIRA: High level outcome](https://redhat.atlassian.net/browse/SRVKP)
- [Any other references](https://example.com/docs/sample)

## Change Log

*Maintain a history of status change and reviews here.*

| Date       | Author         | Change Summary                 |
|------------|----------------|--------------------------------|
| YYYY-MM-DD | @github-handle | Created initial ADR            |
| YYYY-MM-DD | @github-handle | Updated with reviewer feedback |
| YYYY-MM-DD | @github-handle | Status changed to Implemented  |

---

## Metadata

*Update this metadata as and when the ARD is updated.*

```yaml
id: ADR-XXXX
title: "[Title of the Decision]"
status: Accepted
priority: High
date: YYYY-MM-DD
tags:
  - operator
  - architecture
  - tekton
```