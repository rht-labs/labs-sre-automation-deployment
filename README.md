# labs-sre-automation-deployment
Labs SRE Automation Deployment Manifests

This repository both bootstraps and manages the deployment lifecycle of Labs SRE Automation across multiple versions. It contains a manifest which controls the release version of all individual components of Labs Automation. It is meant to be used with Argo CD.

Bootstrapping
To create an instance of Labs Automation in a cluster of your choice, ensure you're on the branch/commit-id of your choice and you have working oc/kubectl session towards the target cluster, then apply the bootstrap Kustomize using the following command:

```
kustomize build bootstrap/ | oc apply -f -
```

NOTE: Running kustomize build bootstrap/ alone will print manifests that can be reviewed before actually applying it to the cluster.

