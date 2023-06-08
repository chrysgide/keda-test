# Keda

Keda and Tests

A [taskfile](https://taskfile.dev/) runner is configured to run local development steps:

```shell
❯ task -l
task: Available tasks for this project:
* clean:            remove kind cluster
* full-test:        full test, create cluster, install, test, delete cluster
* keda:             install keda
* kind:             setup a kind cluster for testing, using version 1.23
* nginx:            install nginx, for testing keda
* prometheus:       install prometheus for testing
* test:             test keda autoscaling; this should scale down to 1 pod
```

## cision - install keda

keda can be installed with standard policies as a kustomize resource

```yaml
resources:
  - https://github.com/Cision-DevOps/keda/deploy/base?ref=XXX
```

##  charts

update helm chart by version

```sh
git remote add keda https://github.com/kedacore/charts
git fetch keda
git checkout tags/v2.8.1 -- charts
```
