# OpenShift Pipelines Architecture

Architecture Decision Records (ADRs) and documentation for OpenShift Pipelines.

## What belongs here?

This repository documents **product-level decisions** for OpenShift Pipelines - the Red Hat distribution of Tekton.

For Tekton feature proposals and API changes, see [Tekton Enhancement Proposals (TEPs)](https://github.com/tektoncd/community/tree/main/teps).

### In scope for this repo

- OpenShift integration (SCC, Routes, OAuth, Console plugin, OperatorHub)
- Support policy and lifecycle decisions
- Component inclusion/exclusion decisions
- Downstream-only patches and their rationale
- Release process and versioning
- Internal tooling and CI/CD decisions
- Security and compliance requirements (FIPS, CVE response)
- Konflux integration specifics

### Out of scope (use TEPs instead)

- Tekton API changes (Pipeline, Task, TaskRun, etc.)
- Tekton Operator behavior (TektonConfig, addon management)
- New Tekton features
- Tekton Results, Chains, Hub, Dashboard features
- Anything that benefits the broader Tekton community

See [docs/scope.md](docs/scope.md) for detailed guidance.

## Structure

```
ADR/           # Architecture Decision Records
docs/          # Additional documentation
```

## Quick links

- [ADR Template](ADR/0000-adr-template.md)
- [Contributing Guide](CONTRIBUTING.md)
- [Scope Definition](docs/scope.md)

## Related

- [Tekton Enhancement Proposals](https://github.com/tektoncd/community/tree/main/teps)
- [konflux-ci/architecture](https://github.com/konflux-ci/architecture) (inspiration for this repo)
