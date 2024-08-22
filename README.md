# gcp-kubernetes
Running Kubernetes on GCP

![wallpaper.jpg](wallpaper.jpg)

## Instructions

Install the GCP SDK:

```bash
curl https://sdk.cloud.google.com | bash
```

Initialize the cloud environment:

```bash
gcloud init
```

Create a project:

```bash
gcloud config set project kuber
```

Enable required services:

```bash
gcloud services enable container.googleapis.com
gcloud services enable deploymentmanager.googleapis.com
```

Deploy the Kubernetes cluster to GCP:

```bash
gcloud deployment-manager deployments create kubernetes-cluster --config cluster.yaml
```

Verify the status of the cluster:

```
gcloud container clusters describe kuber --zone us-central1-a
```