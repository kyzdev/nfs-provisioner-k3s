# traefik-k3s

A kubectl YAML to deploy a NFS Provisioner on Kubernetes

This YAML use Kustomize to decline different <env> in overlays directory.
Please tune your <env> directory, or create new one base on the common files in "base" directory. 

## Post-Installation

You can tune the prod or dev Kustomize Overlay with :

## Installation

The namespace used for this deployment is "nfs".

```bash
# <env> must match your environment overlay
git clone https://github.com/kyzdev/nfs-k3s.git
cd nfs-k3s
kubectl apply -k overlays/<env>
```
## Uninstallation

```bash
# <env> must match your environment overlay
kubectl delete -k overlays/<env>
```

## Credits

https://blog.exxactcorp.com/deploying-dynamic-nfs-provisioning-in-kubernetes/
https://quay.io/repository/kubernetes_incubator/nfs-provisioner