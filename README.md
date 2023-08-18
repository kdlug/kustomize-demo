# Kustomize demo

Kustomize simple demo based on http-echo server.

## Check your version of kubectl

```bash
kubectl version
```

- If you have 1.21 or above of kubectl you will have access to kubectl kustomize which is the recommended method. If you aren't on version 1.21 or above, upgrade kubectl.

- You could also download/use the 'kutomize' binary seperatly but the cmds are different.

## Useful commands

```bash
# View templates
kubectl kustomize .
kubectl kustomize kustomize/overlays/dev/

# Apply templates
kubectl apply -k .
kubectl apply -k kustomize/overlays/dev/

# Delete
kubectl delete -k .
kubectl delete -k kustomize/overlays/dev/

# Port forward
kubectl port-forward service/<service-name> 8080:8080
```

## Resources

- [kustomize reference](https://github.com/kubernetes-sigs/kustomize/blob/master/README.md)
- [kubectl-kustomize Docker image](https://github.com/line/kubectl-kustomize)
