# cilium-vsphere-fullstack
Cilium Fullstack Integration with Kubernetes on vSphere

May 2021

- kubectl create -f cilium-hubble-helm.yaml
- helm repo add haproxytech https://haproxytech.github.io/helm-charts
- helm repo update
- kubectl create ns ingress-controller
- helm install kubernetes-ingress haproxytech/kubernetes-ingress --set controller.service.nodePorts.http=37093 --set controller.service.nodePorts.https=30794 --set controller.service.nodePorts.stat=30795 -n ingress-controller
- kubectl create -f cilium-grafana-pv.yaml
- kubectl create -f cilium-prometheus-pv.yaml
- kubectl create -f cilium-grafana.yaml
- kubectl create -f cilium-grafana-ingress.yaml
- kubectl create -f cilium-prometheus-ingress.yaml


