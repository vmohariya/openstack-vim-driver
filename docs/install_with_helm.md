# Install to Kubernetes

The following guide details how to install the VIM driver into a Kubernetes environment with helm.

## Install Helm Chart

Download and install the chart using the helm CLI:

```
helm install os-vim-driver-<version>.tgz --name os-vim-driver
```

The above installation will expect Kafka to be running in the same Kubernetes namespace with name `foundation-kafka`, which is the default installed by Stratoss&trade; Lifecycle Manager. If different, override the Kafka address:

```
helm install os-vim-driver-<version>.tgz --name os-vim-driver --set app.config.override.messaging.connection_address=myhost:myport
```