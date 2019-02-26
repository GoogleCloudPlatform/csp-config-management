# foo-corp Example #

This example repository for the fictional 'foo-corp' highlights various features of **Cloud Services Platform (CSP) Config Management**.

This repo is discussed in detail in the [CSP Config Management Quickstart](https://cloud.google.com/csp-config-management/docs/quickstart). For details on how to install CSP Config Management and direct your Kubernetes cluster to read from this repository, please reference
 the instructions in the quickstart guide.
 
 This repo contains example configurations for each of the top-level directories defined by the CSP Config Management file system, including:
 - **system/** - This directory contains configs for the Nomos Operator, as well as Syncs.
 - **clusters/** - This directory contains configs that apply to entire clusters, rather than to Namespaces, such as ClusterRoles. By default, any config in the clusters/ directory applies to every cluster enrolled in CSP Config Management. You can limit which clusters a config can affect by using a ClusterSelector.
 - **clusterregistry/** - An optional directory that contains configs for ClusterSelectors, which allow you to address a configuraiton to a specific set of clusters using labels. These ClusterSelectors are referenced in configs found in the clusters/ and namespaces/ directories.
 - **namespaces/** - This directory contains configs for Namespaces and Namespace-scoped objects, such as Rolebindings. It is the only directory in the repo that can contain subdirectories, and the structure within namespaces/ is the mechanism that drives Namespace inheritance. If a directory has subdirectories (such as the 'namespaces/online/' directory, any configuration placed in the directory will be inherited by all subdirectories. Any directory that has no subdirectories (such as the 'namespaces/audit/' directory) is treated as a Namespace and must include a namespace Config.
 
 For more information on how configurations can be used to manage multiple Kubernetes clusters, see the [Creating configs](https://cloud.google.com/csp-config-management/docs/configs) section of the CSP Config Management documentation. 
