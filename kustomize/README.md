# Kustomize

kustomized http-echo application 

## How to deploy?

```bash
$ cd kustomize/overlays/dev
$ kubectl apply -k .
```

Template

```bash
# kustomize/overlays/dev
$ kubectl kustomize  .
```

## How to test?

Forward port 8080

```bash
$ kubectl get svc
kustom-echo-v1   ClusterIP   10.96.142.241   <none>        8080/TCP   41h

$ kubectl port-forward service/kustom-echo-v1 8080:8080
```

Open in a browser http://localhost:8080/. You should see a ECHO_TEXT configured in configmap.yaml (ECHO_TEXT: Dev)

## Cleanup

```bash
kubectl delete -k .
```
