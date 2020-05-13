# k8smonitoring
Grafana and prometheus deployment files.

To setup Grafana and prometheus, run the following:

kubectl create -f clusterRole-prometheus.yml

kubectl create -f config-map.yml

kubectl create -f prometheus-deployment.yml 

kubectl create -f grafana-datasource-config.yml

kubectl create -f grafana-deployment.yml

Log in to prometheus on port 9090 ( you migth want to avoid exposing prometheus as it doesn't come with any authentication mechanism )

Log in to grafana on port 3000

Change the datasource url to your prometheus domain or IP address and port 9090

To deploy kube state metrics

kubectl create -f clusterRole-metrics.yml 

kubectl create -f service-account.yml

kubectl create -f metrics-deployment.yml 

