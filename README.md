# Anthos Config Management

This repository contains example repos for [Anthos Config Management][1].

To use these examples, install the Anthos Config Management operator on your
Kubernetes cluster and and create a custom resource that points at one of the
included examples by setting the `policyDir` field to the directory of the
desired example (e.g. `foo-corp`).

For a more complete experience, you can fork this repository, which will allow
you to make changes and experiment by adding configurations of your own to the
examples contained here. When forking the repository, you will need to change
your cluster configuration to point to the URL of your forked repository.

For more information on Anthos Config Management, please reference the
[Google Cloud Platform documentation][2].

## Examples

### [Foo-Corp](foo-corp/)

A single cluster example showing several features of Anthos Config Management
working together

### [Hello, Namespace!](hello-namespace/)

A simple example to generalize how to define and enforce configuration

### [Locality-Specific Policy](locality-specific-policy/)

Configure policy to apply only to resources in specific regions

[1]: https://cloud.google.com/anthos-config-management/
[2]: https://cloud.google.com/anthos-config-management/docs/overview
