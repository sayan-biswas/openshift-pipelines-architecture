# Contributing to OpenShift Pipelines Architecture

## Before you file an ADR

Ask yourself: **Does this belong upstream?**

If your proposal affects Tekton APIs, behavior, or features that other Tekton users would benefit from, file a [TEP](https://github.com/tektoncd/community/tree/main/teps) instead.

This repo is for **OpenShift Pipelines product decisions** only. See [docs/scope.md](docs/scope.md) for details.

## When to file an ADR

- OpenShift-specific integration decisions
- Support policy or lifecycle changes
- Decisions about what components to include/exclude
- Downstream patch rationale
- Release or versioning process changes
- Security/compliance requirements

## Process

### 1. Create your ADR

Copy the template:

```bash
cp ADR/0000-adr-template.md ADR/00XX-my-decision.md
```

Use the next available number. Fill in all sections.

### 2. Open a Pull Request

- Title: `ADR: <brief description>`
- Fill in the PR template
- Request review from maintainers

### 3. Discussion period

- ADRs are discussed in PR comments
- Significant ADRs may be announced in team meetings
- Address all feedback

### 4. Acceptance

- Maintainers approve or request changes
- Once merged, the ADR is considered accepted
- Update status to "Accepted" or "Implemented" as appropriate

## Style guidelines

- Keep it concise - ADRs should be readable in a few minutes
- Focus on **why**, not just what
- Be honest about trade-offs in Consequences
- Link to relevant TEPs, issues, or external docs

## Questions?

Open an issue if you're unsure whether something belongs here or upstream.
