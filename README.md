### tempo 

download chart:
> helm repo add grafana https://grafana.github.io/helm-charts
> helm repo update

install command:
> helm -n tempo-test install tempo grafana/tempo-distributed -f custom.yaml

### otel-collector

download chart:
>  helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts 
> helm repo update  

download all the chart and values.yaml:
> helm pull open-telemetry/opentelemetry-collector --untar 

* feature: 
    * now enable the kubeletstats in otel-collector
    * get the metrics from the nodes/pods/containers

* command:
helm install otel-collector ./opentelemetry-collector \
  -f ./opentelemetry-collector/values.yaml \
  -n observability --create-namespace


### prometheus

command: 
> helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
> helm repo update

