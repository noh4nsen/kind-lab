# Argo CD Configuration

This chart is configuring chart with parameters for a simple lab, this setup should not be used in production.

```bash
helm dependency update ./argocd/
helm upgrade argocd ./argocd/ --namespace argocd

#To retrieve initial password
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```