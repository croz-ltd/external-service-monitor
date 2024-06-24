# external-service-monitor
A Helm Chart that configures ServiceMonitor to bring metrics from a service outside of a K8s/OpenShift cluster

Table of available parameters:

| Parameter                          | Description                                                                                               | Default Value         |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------|
| `targetService.ip`                 | The IP address of the target service                                                                      | `11.11.11.2`          |
| `targetService.hostname`           | The hostname of the target service                                                                        | `target.service.com`  |
| `targetService.port`               | The port number to connect to the target service                                                          | `443`                 |
| `targetService.scheme`             | The scheme to use for connecting to the target service (e.g., http, https)                                | `https`               |
| `targetService.insecureSkipVerify` | A boolean flag indicating whether to skip verification of the server's certificate (insecure connections) | `false`               |
| `scrape[0].interval`               | The interval at which Prometheus will scrape metrics from the target service                              | `13s`                 |
| `scrape[0].path`                   | The path on the target service where Prometheus can scrape metrics                                        | `/metrics`            |
