This repository contains example configurations for Cloud Services Platform Config Management.

To use these examples, install the CSP Config Management operator on your Kubernetes cluster and and create a custom resource that points at one of the included examples by setting the 'policyDir' field to the directory of the desired example (e.g. 'foo-corp').

This example command will configure your cluster to use the "foo-corp" example contained in this repository:

```
apiVersion: addons.sigs.k8s.io/v1alpha1
kind: Nomos
metadata:
  name: nomos
  namespace: nomos-system
spec:
  git:
    syncRepo: git@github.com:GoogleCloudPlatform/csp-examples.git
    syncWait: 5
    secretType: ssh
    policyDir: foo-corp
```
