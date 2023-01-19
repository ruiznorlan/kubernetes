# DEPLOYMENTS

Un controlador de Deployment proporciona actualizaciones declarativas para los Pods y los ReplicaSets.

Cuando describes el estado deseado en un objeto Deployment, el controlador del Deployment se encarga de cambiar el estado actual al estado deseado de forma controlada. Puedes definir Deployments para crear nuevos ReplicaSets, o eliminar Deployments existentes y adoptar todos sus recursos con nuevos Deployments.

[Fuente: Documentación](https://kubernetes.io/es/docs/concepts/workloads/controllers/deployment/)

----

## Comandos Útiles

Aplicar todos los YAML

```bash
kubectl apply -f .
```

Ver los Deployments

```bash
kubectl get deploy
```

Editar un Deployment

```bash
kubectl edit deploy nginx-d
```

Escalar un Deployment

```bash
kubectl scale deploy -l estado=1 --replicas=10
```
