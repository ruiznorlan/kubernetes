# ANNOTATIONS

Puedes usar las anotaciones de Kubernetes para adjuntar metadatos arbitrarios a los objetos, de tal forma que clientes como herramientas y librerías puedan obtener fácilmente dichos metadatos.

```json
"metadata": {
  "annotations": {
    "key1" : "value1",
    "key2" : "value2"
  }
}
```

[Fuente: Documentación](https://kubernetes.io/es/docs/concepts/overview/working-with-objects/annotations/)

----

## Comandos Útiles

Aplicar el YAML

```bash
kubectl apply -f tomcat4.yaml
```

Describir un componente, dentro de la descripción se encontrarán las anotaciones

```bash
kubectl describe pod tomcat4
```
