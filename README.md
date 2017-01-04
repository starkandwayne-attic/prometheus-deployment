Prometheus Deployment Template
======================================

This repository acts as an upstream repository of YAML templates for use in deploying one or more [Prometheus][prometheus] clusters via the [Genesis][genesis] utility.

Creating a new Prometheus Deployment
======================================

To create a new [Genesis][genesis]-based deployment of Prometheus, run

```
genesis new deployment --template prometheus
```

This will create a new repo called `prometheus-deployments` for you, and pull in the `github.com/starkandwayne/prometheus-deployment` repo as the `upstream` remote, copying the contents of `global/*` into the new `prometheus-deployments` repository.

This allows you to easily diverge from the upstream templates to suit your environment, yet still be able to pull in changes from upstream down the road.

BOSH-Lite Sites
======================================

The `bosh-lite` template will set you up with a structure suitable for deploying Prometheus on a BOSH-Lite.

```
genesis new site --template bosh-lite <name>
```

Amazon EC2 (AWS) Sites
======================================

The `aws` template will set you up with a structure suitable for deploying Prometheus to Amazon Web Service's EC2/VPC infrastructure.

```
genesis new site --template aws <name>
```

Google Cloud Platform (Google) Sites
======================================

The `google` template will set you up with a structure suitable for deploying Prometheus to Google Cloud Plaftorm infrastructure.

```
genesis new site --template google <name>
```

vCloud Director (vCloud) Sites
======================================

The `vcloud` template will set you up with a structure suitable for deploying Prometheus on a vCloud Director infrastructure.

```
genesis new site --template vcloud <name>
```

vSphere Sites
======================================

The `vsphere` template will set you up with a structure suitable for deploying Prometheus on a VMWare vSphere ESXi cluster.

```
genesis new site --template vsphere <name>
```

Notes
======================================

For more information, check out the [Genesis][genesis] repo, or `genesis help`. You can download the Genesis program from [Github][genesis]

[genesis]: https://github.com/starkandwayne/genesis
[prometheus]: https://prometheus.io/
