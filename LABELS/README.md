# LABELS

Las etiquetas son pares de clave/valor que se asocian a los objetos, como los pods. El propósito de las etiquetas es permitir identificar atributos de los objetos que son relevantes y significativos para los usuarios, pero que no tienen significado para el sistema principal. Se puede usar las etiquetas para organizar y seleccionar subconjuntos de objetos. Las etiquetas se pueden asociar a los objetos a la hora de crearlos y posteriormente modificarlas o añadir nuevas. Cada objeto puede tener un conjunto de etiquetas clave/valor definidas, donde cada clave debe ser única para un mismo objeto.

```json
"metadata": {
  "labels": {
    "key1" : "value1",
    "key2" : "value2"
  }
}
```

Las etiquetas permiten consultar y monitorizar los objetos de forma más eficiente y son ideales para su uso en UIs y CLIs. El resto de información no identificada debe ser registrada usando anotaciones.

Ejemplos de etiquetas:

* "release" : "stable", "release" : "canary"
* "environment" : "dev", "environment" : "qa", "environment" : "production"
* "tier" : "frontend", "tier" : "backend", "tier" : "cache"
* "partition" : "customerA", "partition" : "customerB"
* "track" : "daily", "track" : "weekly"

Estos son sólo algunos ejemplos de etiquetas de uso común; eres libre de establecer tus propias normas. Ten en cuenta que la clave de cada etiqueta debe ser única dentro de cada objeto.

[Fuente: Documentación](https://kubernetes.io/es/docs/concepts/overview/working-with-objects/labels/)

----

## Comandos Útiles

Crear una etiqueta

```bash
kubectl label pod tomcat responsable=juan
```

Mostrar las etiquetas

```bash
kubectl get pods --show-labels
```

Modificar una etiqueta

```bash
kubectl label --overwrite pod/tomcat responsable=pedro
```

Eliminar una etiqueta
```bash
kubectl label pod/tomcat responsable-
```
