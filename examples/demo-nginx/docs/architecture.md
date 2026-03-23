# Architecture

`demo-nginx` ships nginx as container images deployed by Kubernetes manifest in `k8s/demo-workload.yaml`.

- Service: `demo-nginx`
- Namespace: `backstage-demo`
- Label selector: `app=demo-nginx`
