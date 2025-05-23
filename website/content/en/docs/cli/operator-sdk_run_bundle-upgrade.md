---
title: "operator-sdk run bundle-upgrade"
---
## operator-sdk run bundle-upgrade

Upgrade an Operator previously installed in the bundle format with OLM

### Synopsis

The single argument to this command is a bundle image, with the full registry path specified.
If using a docker.io image, you must specify docker.io(/&lt;namespace&gt;)?/&lt;bundle-image-name&gt;:&lt;tag&gt;.
If the bundle image provided is a SQLite index, it must be pullable by the cluster as SQLite images are pulled from the cluster.
If the bundle image provided is a File-Based Catalog (FBC) index, it will be pulled on the local machine.

```
operator-sdk run bundle-upgrade <bundle-image> [flags]
```

### Options

```
      --ca-secret-name string                     Name of a generic secret containing a PEM root certificate file required to pull bundle images. This secret *must* be in the namespace that this command is configured to run in, and the file *must* be encoded under the key "cert.pem"
  -h, --help                                      help for bundle-upgrade
      --image-pull-policy string                  image pull policy for the registry pod (default "Always")
      --kubeconfig string                         Path to the kubeconfig file to use for CLI requests.
  -n, --namespace string                          If present, namespace scope for this CLI request
      --pull-secret-name string                   Name of image pull secret ("type: kubernetes.io/dockerconfigjson") required to pull bundle images. This secret *must* be both in the namespace and an imagePullSecret of the service account that this command is configured to run in
      --security-context-config SecurityContext   specifies the security context to use for the catalog pod. allowed: 'restricted', 'legacy'. (default legacy)
      --service-account string                    Service account name to bind registry objects to. If unset, the default service account is used. This value does not override the operator's service account
      --skip-tls                                  skip authentication of image registry TLS certificate when pulling a bundle image in-cluster
      --skip-tls-verify                           skip TLS certificate verification for container image registries while pulling bundles
      --timeout duration                          Duration to wait for the command to complete before failing (default 2m0s)
      --use-http                                  use plain HTTP for container image registries while pulling bundles
```

### Options inherited from parent commands

```
      --plugins strings   plugin keys to be used for this subcommand execution
      --verbose           Enable verbose logging
```

### SEE ALSO

* [operator-sdk run](../operator-sdk_run)	 - Run an Operator in a variety of environments

