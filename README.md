# kubernetes-prometheus-demo

The example files are using [coreos/prometheus-operator](https://github.com/coreos/prometheus-operator) to run
Prometheus and Alertmanager.
[kubernetes/kube-state-metrics](https://github.com/kubernetes/kube-state-metrics) and
[prometheus/node_exporter](https://github.com/prometheus/node_exporter) are used as "example" applications from
which to get metrics from.

## File Structure

* `alerting/` - Example Prometheus alert rule.
    * `deadman-switch.yaml` - Dead Man Switch rule for Promteheus (PrometheusRule object).
    * `rules.yaml` - Rules taken from [kube-prometheus](https://github.com/coreos/prometheus-operator/tree/master/contrib/kube-prometheus).
* `kube-state-metrics/` - Kubernetes manifests for [kubernetes/kube-state-metrics](https://github.com/kubernetes/kube-state-metrics).
* `node-exporter/` - Kubernetes manifests for [prometheus/node_exporter](https://github.com/prometheus/node_exporter).
* `prometheus/` - Kubernetes manifests for [coreos/prometheus-operator](https://github.com/coreos/prometheus-operator), Prometheus and Alertmanager instances.
    * `alertmanager/` - Alertmanager manifests.
    * `prometheus/` - Prometheus manifests.
    * `prometheus-operator/` - Prometheus operator manifests.
