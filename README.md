# Kubernetes Kustomize Playground

Kustomize introduces a template-free way to customize application configuration that simplifies the use of off-the-shelf applications and is built into Kubernetes.

```bash
kubectl kustomize overlays/dev

kubectl apply -k overlays/dev 
kubectl get pods
kubectl delete -k overlays/dev 

kubectl apply -k overlays/prod
kubectl get pods
kubectl delete -k overlays/prod
```

Then visit `http://localhost:30000`.

## How

Files in `base` contain the standard YAML and get overwritten from `overlays`:

```
├───base
│       deployment.yaml
│       kustomization.yaml
│       service.yaml
│
└───overlays
    ├───dev
    │       application.properties
    │       kustomization.yaml
    │       replicas.yaml
    │
    └───prod
            application.properties
            kustomization.yaml
            replicas.yaml
```

## Resources

* https://kubernetes.io/docs/tasks/manage-kubernetes-objects/kustomization/
* https://www.youtube.com/watch?v=spCdNeNCuFU
* https://github.com/devopsjourney1/mykustomapp/tree/master