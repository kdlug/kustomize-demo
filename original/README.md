# Original

http-echo application with configmap which passes text to the application

## How to deploy?

```bash
$ cd original
$ kubectl apply -f .
```

# How to test?

Forward port 8080

```bash
$ kubectl get svc
echo  ClusterIP   10.96.142.241   <none>        8080/TCP   41h

$ kubectl port-forward service/echo 8080:8080
```

Open in a browser http://localhost:8080/. You should see a ECHO_TEXT configured in configmap.yaml (ECHO_TEXT: Demo).

## Cleanup

```bash
kubectl delete -f .
```
