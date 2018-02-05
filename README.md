## Deployment

To create / update this instance, do the following:

1. Run:
    ```bash
    gcloud config configurations create 31232132132
    gcloud config set core/project 32321321312
    gcloud config set core/account 32131232131
    gcloud config set compute/zone 321321312
    ```
    After this step, `gcloud config configurations describe 65654654654` should print:
    ```yaml
    is_active: true
    name: 654654654654
    properties:
    compute:
        zone: 5654645654654
    core:
        account: 543534543
        project: 654654654
    ```
1. `gcloud container clusters get-credentials 543543543543534543`<br>
    After this, `kubectl` should be configured to hit the demo cluster.
1. Walk through the [Sourcegraph Data Center installation instructions](https://about.sourcegraph.com/docs/server/datacenter). Use the `storage-class.yaml` in this directory when creating the storage class.
1. Afterward, you'll need to manually expose the sourcegraph-frontend service's NodePort port in the [GCP Firewall rules settings](https://example.com). (Alternatively, you can change the type of the sourcegraph-frontend service from "NodePort" to "LoadBalancer" and an external IP will be automatically allocated and visible via `kubectl get svc sourcegraph-frontend`.
