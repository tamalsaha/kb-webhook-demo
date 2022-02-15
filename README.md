# kb-webhook-demo

ref: https://kubebuilder.io/migration/multi-group.html

```
# create kubebuilder project
$ kubebuilder init --domain x-helm.dev --skip-go-version-check

# convert project to multi group layout
$ kubebuilder edit --multigroup=true

# add first api group
$ kubebuilder create api --group module --version v1alpha1 --kind Workflow

# generate webhook
$ kubebuilder create webhook --group module --version v1alpha1 --kind Workflow --defaulting --programmatic-validation
```
