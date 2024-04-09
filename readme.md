# Helm Chart for adding Horizontal Pod Autoscaler in a Deployment

## Description
This Helm chart deploys an application with Horizontal Pod Autoscaler (HPA) support in Kubernetes.

## Prerequisites
- Kubernetes cluster
- Helm 3.x installed

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/NashTech-Labs/TEMPLATE-FOR-HPA-HELM.git
   cd hpa-helm-chart
   ```
2. Customize the values in ```values.yaml``` as needed.

3. Install the Helm chart:
   ```
   helm install my-hpa-release .
   ```
4. Verify the deployment and HPA:
   ```
   kubectl get deployment
   kubectl get hpa
   ```

## Configurations

You can customize the deployment and HPA configurations by modifying the values in values.yaml.

`replicaCount:` Number of replicas for the deployment.

`image.repository and image.tag:` Docker image and tag for the application container.

`containerPort:` Port exposed by the application container.

`hpa.minReplicas and hpa.maxReplicas:` Minimum and maximum number of replicas for HPA.

`hpa.targetCPUUtilizationPercentage:` Target CPU utilization percentage for HPA scaling.

