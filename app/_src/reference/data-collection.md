---
title: Kuma data collection
---

{{site.mesh_product_name}} can collect information about your deployment to continuously improve the product and gather anonymous feedback. The collected data is sent to Kong servers securely for storage and aggregation.

You can enable data collection when installing the control plane in Kubernetes, of before running `kuma-cp` in Universal mode.

## Enabling data collection

1.  Set the following environment variable:

    ```
    KUMA_REPORTS_ENABLED=true
    ```

1.  Specify the environment variable when you install the control plane. See the [configuration docs](/docs/{{ page.release }}/documentation/configuration/) for details.

Or you can set the `reports.enabled` field to `true` in the config YAML file.

## What data is collected

| Data field | Definition                                                                                                               | 
|---|--------------------------------------------------------------------------------------------------------------------------|
| version  | The installed version of {{site.mesh_product_name}} you're running                                                       | 
| product  | Static value "{{site.mesh_product_name}}"                                                                                | 
| unique_id  | Control plane hostname + randon UUID, generated each time control plane instance is restarted                            | 
| backend  | Where your config is stored. One of in memory, etcd, Postgres                                                            | 
| mode    | One of zone or global                                                                                                    |
| hostname | The hostname of each {{site.mesh_product_name}} control plane you deploy                                                 |
| signal | One of `start` or `ping`. `start` sent when control plane starts, then `ping` once per hour                              | 
| cluster_id | Unique identifier for entire {{site.mesh_product_name}} cluster. Value is the same for all control planes in the cluster |
| dps_total | The total number of data plane proxies across all meshes                                                                 | 
| meshes_total | The total number of meshes deployed                                                                                      | 
| zones_total | The total number of zones deployed                                                                                       | 
| internal_services | Tne total number of services running inside your meshes                                                                  | 
| external_services | The total number of external services configured for your meshes                                                         |
| services_ total | The total number of services in your mesh network                                                                        | 
