# Helm Charts Repository

This repository hosts packaged **Helm charts** published via GitHub Pages.

The charts in this repository are intended to be consumed by CI/CD pipelines or installed directly using Helm.



## 📦 Available Charts

| Chart | Description |
|------|-------------|
| flask-counter | Helm chart for deploying the Flask Counter application |



## ➕ Add the Helm Repository

```bash
helm repo add gal-halevi-helm https://gal-halevi.github.io/helm-charts
helm repo update
```

Verify the repository was added:

```bash
helm search repo gal-halevi-helm
```



## 🚀 Install / Upgrade a Chart

Example installation:

```bash
helm upgrade --install counter-app gal-halevi-helm/flask-counter \
  --version <chart-version> \
  --set image.repository=<docker-image-repo> \
  --set image.tag=<image-tag>
```

Chart versions are published as immutable artifacts and should be pinned when used in CI/CD pipelines.



## 🔗 Related Projects

- Source application and CI/CD pipeline:
  https://github.com/gal-halevi/devops-experts-project
