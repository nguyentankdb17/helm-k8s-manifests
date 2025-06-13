# My own helm charts for microservices webapp
#### Original repository: https://github.com/GoogleCloudPlatform/microservices-demo   
You can deploy your own helm charts following these steps:
- Step 1: Create a Kubernetes cluster (I created on Google Kubernetes Engine).
- Step 2: Connect to that cluster, define number of control plane nodes and worker nodes (If you use public cloud services such as GKE or EKS, you only need to care about worker nodes).
- Step 3: Install Helm via [this](https://helm.sh/docs/intro/install/).
- Step 4: Write your own helm charts for each services.
- Step 5 (optional): Install `helmfile` and write a `helmfile.yaml` to run multiple helm charts simultaneously.
- Step 6: Access the external IP of the frontend pod and see the result.
   
  ![](https://github.com/GoogleCloudPlatform/microservices-demo/blob/main/docs/img/online-boutique-frontend-1.png)
