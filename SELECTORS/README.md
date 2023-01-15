# SELECTORS

Al contrario que los nombres y UIDs, las etiquetas no garantizan la unicidad. En general, se espera que muchos objetos compartan la(s) misma(s) etiqueta(s).

A través del selector de etiqueta, el cliente/usuario puede identificar un conjunto de objetos. El selector de etiqueta es la primitiva principal de agrupación en Kubernetes.

La API actualmente soporta dos tipos de selectores: basados en igualdad y basados en conjunto. Un selector de etiqueta puede componerse de múltiples requisitos separados por coma. En el caso de múltiples requisitos, todos ellos deben ser satisfechos de forma que las comas actúan como operadores AND (&&) lógicos.

La semántica de selectores vacíos o no espefificados es dependiente del contexto, y los tipos de la API que utilizan los selectores deberían documentar su propia validación y significado.

[Fuente: Documentación](https://kubernetes.io/es/docs/concepts/overview/working-with-objects/labels/#selectores-de-etiquetas)

----

## Comandos Útiles

Aplicar todos los YAML

```bash
kubectl apply -f .
```

Mostrar todos los PODS que incluyan la etiqueta (se puede usar el '==' o '=')

```bash
kubectl get pods --show-labels -l estado=desarrollo
```

Se pueden realizar búsquedas de tipo AND

```bash
kubectl get pods --show-labels -l estado==desarrollo,responsable=juan
```

Se pueden realizar búsquedas que sean diferentes a lo indicado (con el símbolo '!=')

```bash
kubectl get pods --show-labels -l responsable!=juan
```

```bash
kubectl get pods --show-labels -l estado!=testing
```

Se pueden realizar búsquedas en una lista (por ejemplo, buscar los que en el estado tengan 'desarrollo' y 'testing')

```bash
kubectl get pods --show-labels -l 'estado in(desarrollo,testing)'
```

Se pueden realizar búsquedas que no estén en una lista (por ejemplo, buscar los que en el estado no tengan 'desarrollo' y 'testing')

```bash
kubectl get pods --show-labels -l 'estado notin(desarrollo,testing)'
```

Además cualquier comando puede aceptar selectores, por ejemplo, si se quisiera eliminar los PODS que tengan la etiqueta de estado=desarrollo

```bash
kubectl delete pods -l estado=desarrollo
```