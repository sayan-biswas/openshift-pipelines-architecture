# Scope: OSP ADRs vs Upstream TEPs

This document defines what belongs in OpenShift Pipelines Architecture vs upstream Tekton Enhancement Proposals.

## Guiding principle

> If it benefits the broader Tekton community, it belongs upstream.
> If it's specific to how Red Hat builds, ships, or supports the product, it belongs here.

## What goes in upstream TEPs

[Tekton Enhancement Proposals](https://github.com/tektoncd/community/tree/main/teps) cover:

- **Core APIs**: Pipeline, Task, TaskRun, PipelineRun, etc.
- **Tekton Operator**: TektonConfig, addon management, installation behavior
- **Tekton components**: Results, Chains, Hub, Dashboard features
- **Resolvers**: Git, Bundle, Cluster, Hub resolvers
- **Cross-ecosystem standards**: Result naming, annotations, labels
- **New features**: Anything that changes how Tekton works

## What goes in OSP ADRs

OpenShift Pipelines ADRs cover **product-level decisions**:

### OpenShift Integration
- Security Context Constraints (SCC) configuration
- Route exposure and TLS
- OAuth proxy integration
- OpenShift Console plugin
- OperatorHub packaging and metadata

### Support Policy
- Supported OpenShift versions
- Component lifecycle and deprecation
- Breaking change policy
- Upgrade path requirements

### Component Decisions
- What upstream components to include
- What to exclude and why
- Version pinning rationale
- Downstream-only additions

### Downstream Patches
- Patches not yet upstream
- Rationale for temporary divergence
- Timeline for upstreaming

### Release Process
- Versioning scheme
- Branching strategy
- Backport policy
- Release cadence

### Internal Tooling
- CI/CD infrastructure decisions
- Testing strategy
- Build process

### Security & Compliance
- FIPS requirements
- CVE response process
- Security scanning requirements

### Konflux Integration
- Konflux-specific configuration
- Integration with Konflux services

### Quality Engineering
- Test strategy and architecture
- QE tooling decisions
- Test coverage requirements
- E2E and integration test approach

## Gray areas

When in doubt:

1. **Start upstream** - propose a TEP or bring it up in [Tekton working groups](https://github.com/tektoncd/community/blob/main/working-groups.md)
2. **Reference, don't duplicate** - if a TEP exists, link to it
3. **Ask** - open an issue here if unsure

## Examples

| Decision | Where? | Why? |
|----------|--------|------|
| Add new Pipeline API field | TEP | Core API change |
| Configure default SCC for pipelines | OSP ADR | OpenShift-specific |
| New Tekton Results feature | TEP | Benefits all users |
| Which OCP versions to support | OSP ADR | Product policy |
| Change TektonConfig behavior | TEP | Operator is upstream |
| Downstream-only CVE patch | OSP ADR | Product-specific |
