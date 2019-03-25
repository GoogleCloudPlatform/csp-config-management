# CSP Config Management Examples #

This repository contains example configurations for Cloud Services Platform (CSP) Config Management.

To use these examples, install the CSP Config Management operator on your Kubernetes cluster and and create a custom resource that points at one of the included examples by setting the 'policyDir' field to the directory of the desired example (e.g. 'foo-corp').

This example command will configure your cluster to use the "foo-corp" example contained in this repository:

```
apiVersion: addons.sigs.k8s.io/v1alpha1
kind: ConfigManagement
metadata:
  name: config-management
spec:
  git:
    syncRepo: git@github.com:GoogleCloudPlatform/csp-examples.git
    syncWait: 5
    secretType: ssh
    policyDir: foo-corp
```

For a more complete experience, you can fork this repository, which will allow you to make changes and experiment by adding configurations of your own to the examples contained here. When forking the repository, you will need to change your cluster configuration to point to the URL of your forked repository.

For more information on CSP Config Management, please reference the [Google Cloud Platform documentation](https://cloud.google.com/csp-config-management/docs/). 
