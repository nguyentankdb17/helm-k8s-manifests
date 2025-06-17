# Prometheus in Kubernetes Cluster
## 📁 Folder Structure

```bash
.
└── alert-rules.yml       # Contains own alert rules for Prometheus
```
## Steps
- Install Prometheus in K8s cluster via helm
```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
kubectl create namespace monitoring
helm install my-prometheus prometheus-community/kube-prometheus-stack -n monitoring
```
- To apply the rule, run kubectl command:  
```
kubectl apply -f alert-rules.yml
```  
Note that the release metadata in config file must match with the ruleSelector in Prometheus. You can check via command:   
 `kubectl -n monitoring get prometheus -o yaml | grep -A 5 ruleSelector`
