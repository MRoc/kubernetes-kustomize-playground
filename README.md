# kubernetes-kustomize-playground

```bash
kubectl apply -k overlays/dev 
kubectl get pods
kubectl delete -k overlays/dev 

kubectl apply -k overlays/prod
kubectl get pods
kubectl delete -k overlays/prod
```

Then visit `http://localhost:30000`.