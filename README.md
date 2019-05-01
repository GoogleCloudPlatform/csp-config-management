# Anthos Config Management

## Examples

This repository contains example repos for [Anthos Config Management][1].

To use these examples, install the Anthos Config Management operator on your
Kubernetes cluster and and create a custom resource that points at one of the
included examples by setting the `policyDir` field to the directory of the
desired example (e.g. `foo-corp`).

This example command will configure your cluster to use the `foo-corp` example
contained in this repository:

```yaml
apiVersion: addons.sigs.k8s.io/v1alpha1
kind: ConfigManagement
metadata:
  name: config-management
spec:
  git:
    syncRepo: git@github.com:GoogleCloudPlatform/csp-config-management.git
    syncBranch: "0.1.0"
    syncWait: 5
    secretType: ssh
    policyDir: foo-corp
```

For a more complete experience, you can fork this repository, which will allow
you to make changes and experiment by adding configurations of your own to the
examples contained here. When forking the repository, you will need to change
your cluster configuration to point to the URL of your forked repository.

For more information on Anthos Config Management, please reference the
[Google Cloud Platform documentation][2].

## How-to Guides

*   [Validate Configs in CI/CD](docs/how-to-validate-ci-cd.md)

[1]: https://cloud.google.com/anthos-config-management/
[2]: https://cloud.google.com/anthos-config-management/docs
