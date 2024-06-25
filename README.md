# download-old-bitnami-helm-charts

Add bitnami repo

```
helm repo add bitnami-full-index https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami

```
Download and extract the helm chart
```
helm fetch bitnami-full-index/postgresql --version 10.16.2 --untar
```

If you are using sub-helm charts, update the repository url.

```diff
  - name: postgresql
    version: 10.16.2
-   repository: https://charts.bitnami.com/bitnami
+   repository: https://raw.githubusercontent.com/bitnami/charts/archive-full-index/bitnami
    condition: postgresql.enabled
```
