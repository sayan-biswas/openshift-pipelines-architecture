# 0003. OpenShift Builds Integration in OpenShift Pipelines

Date: 2026-08-25

## Status

Proposed

<!-- Status lifecycle:
- Proposed: Under discussion, not yet accepted
- Accepted: Approved, ready for implementation
- Implemented: Done and reflected in the product
- Superseded: Replaced by a newer ADR (link to it)
- Rejected: Not accepted (stays in repo for reference)
-->

## Context

OpenShift Builds will cease to exist as separate product and will made available to user through OpenShift Pipelines.
This integration will install OpenShift Builds operator along with OpenShift Pipelines Operator from the user installs OpenShift Pipelines from software catalog.

### Constraints

- This will only install the Builds Operator and user would need to create a OpenShiftBuilds CR to install the Build controllers.
- The operator will be installed in openshift-operators namespace
- The controllers will be installed in openshift-builds namespace
- OpenShift Builds will have separate set or roles and role bindings
- Existing forms for Builds in OpenShift UI should work as it is.

### Proposal

`operators.coreos.com/v1alpha1`, Cluster Service Version defines deployments as a list, which allows to specify multiple deployments.

```yaml
# Cluster Service Version (Builds deployment added)
spec:
  install:
   spec:
     deployments:
      - name: tekton-operator
   ...
	 - name: tekton-operator-webhook
   ...
	 - name: openshift-builds-operator
   ...
```

Create Kustomize component `builds` under [Operator Config for OpenShift](https://github.com/tektoncd/operator/tree/main/config/openshift). The component will hold all the manifest required to deploy OpenShift Builds operator.
Include the manifest under [OperatorHub release manifests](https://github.com/tektoncd/operator/blob/main/operatorhub/openshift/manifests/fetch-strategy-release-manifest/kustomization.yaml)

User creates the following CR to install Shipwright Builds controllers and Shared resources daemonset.
```yaml
apiVersion: operator.openshift.io/v1alpha1
kind: OpenShiftBuild
metadata:
  name: cluster
spec:
  sharedResource:
    state: Enabled
  shipwright:
    build:
      state: Enabled
```

## Decision

TBD

## Consequences

OpenShift Builds operator will be deployed along with OpenShift Pipelines Operator. After that user can optionally create `OpenShiftBuilds` CR to install Shipwright Builds and Shared Resources

### Benefits

- OpenShift Builds will integrate with OpenShift Pipelines

### Drawbacks

- Existing OpenShift Builds users should manually switch by uninstalling existing builds operator and creating the `OpenShiftBuilds` custom resource.

### Follow-up actions

- Migration path from existing installing process to this proposed installation process
- OpenShift Builds docs to exists as standalone or merged with OpenShift Pipelines
- The OpenShift UI forms for Shipwright exists under `Builds` section under OpenShift Console. It should be changed to dynamic console plugin and brought under OpenShift Pipelines. 
