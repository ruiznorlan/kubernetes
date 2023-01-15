# PODS

Los Pods son las unidades de computación desplegables más pequeñas que se pueden crear y gestionar en Kubernetes.

----

## ¿Qué és un Pod?

Un Pod es un grupo de uno o más contenedores (como contenedores Docker), con almacenamiento/red compartidos, y unas especificaciones de cómo ejecutar los contenedores. Los contenidos de un Pod son siempre coubicados, coprogramados y ejecutados en un contexto compartido. Un Pod modela un "host lógico" específico de la aplicación: contiene uno o más contenedores de aplicaciones relativamente entrelazados. Antes de la llegada de los contenedores, ejecutarse en la misma máquina física o virtual significaba ser ejecutado en el mismo host lógico.

[Fuente: Documentación](https://kubernetes.io/es/docs/concepts/workloads/pods/pod/)

----


### Imperativo

```bash
kubectl run nginx1 --image=nginx
```

### Declarativo

```bash
kubectl apply -f 01-primer-pod.yaml
```
