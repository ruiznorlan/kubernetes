# Kubernetes (K8s)

<img src="https://github.com/kubernetes/kubernetes/raw/master/logo/logo.png" width="100">

----

## Descripción

Repositorio con ejemplos sobre los componentes de K8S

----

## Importante
En los ejemplos de cada componente se mostrará como crearlos de forma imperativa o declarativa.

### Declarativo vs Imperativo: Definiciones

Algo que es declarativo hace una declaración del resultado final, indicando la intención pero no el proceso para lograrlo. En Kubernetes, esto dice "Debe haber un ReplicaSet con tres pods".

Un imperativo actúa como un comando. Mientras que un declarativo es pasivo, los imperativos son activos e inmediatos: "Crear un ReplicaSet con tres Pods".

El ecosistema de Kubernetes proporciona mecanismos para interactuar con su clúster en cualquiera de estas formas. Los enfoques imperativos son atendidos por comandos CLI y archivos YAML individuales. La configuración declarativa se facilita utilizando directorios de archivos que se combinan en la representación final del recurso.
