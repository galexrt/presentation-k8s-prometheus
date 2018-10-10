# no-operator

Install and run Prometheus + Alertmanager without the use of [coreos/prometheus-operator](https://github.com/coreos/prometheus-operator) but using `helm` to render and then manually apply the manifests.

## Credits

The `prometheus/` and `prometheus-blackbox-exporter/` directories are originally from the [GitHub helm/charts](https://github.com/helm/charts) repository but have gotten some slight modifications from me.
I will probably return some of my modifications back to the repo when I have the time.

## Helm

```
export YOUR_NAMESPACE=my-monitoring-test
mkdir -p ./prometheus-rendered/ ./prometheus-blackbox-exporter
helm template --namespace ${YOUR_NAMESPACE} --name example --output-dir ./prometheus-rendered/ -f ./prometheus-values.yaml ./prometheus/
helm template --namespace ${YOUR_NAMESPACE} --name example --output-dir ./prometheus-rendered/ -f ./prometheus-blackbox-exporter-values.yaml ./prometheus-blackbox-exporter/
```
