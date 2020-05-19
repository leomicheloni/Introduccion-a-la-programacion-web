## Día 2 - Elementos HTML

Cada cosa que vemos en una Web (página, sitio, aplicación, etc.) es en algún punto un elemento declarado.
[Existe muchos elementos HTML definidos ](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

Vamos a hablar de los más básicos (y también más utilizados) pero no son los únicos y vale la pena aprender otros, si bien con los que se detalla a continuación podemos hacer prácticamente cualquier cosa.

### Elementos

 ``` html
 <html>
 ```
 Es el elemento raíz, solo puede existir uno, todo el *html* es hijo de él.

  ``` html
 <head>
 ```
Contiene elementos accesorios del contenido, por ejemplo archivos *css*, *js* o *meta-información* de la página. Es información que solo le interesa el navegador.

´´´ html
body
´´´
Este elemento es el que encierra el contenido que se visualiza, solo puede haber uno.

### Dentro del body

``` html
<p>
```
Párrafo de texto, puede contener otros tags si son para texto, como por ejemplo ``` <i> ``` para mostrar contenido en itálica.

``` html
<hr>
```
Es una línea horizontal, no tiene cierre porque ocupa siempre una línea completa

``` html
<a>
```
El anchor representa un enlace (link) a otra página o una sección dentro de la página actual

``` html
<img>
```
Permite agregar imágenes

``` html
<table>
```
Tablas, para contenido del tipo grilla

``` html
<div>
```

Permite declarar una sección lógica de varías líneas, no altera el texto ni permite hacer nada, solo es para agrupar texto o elementos.

``` html
<h1>
```
Es un texto del tipo encabezado, un título.

``` html
<ul>
 <li>
```
Listas desordenadas

``` html
<br>
```
Salto de línea

``` html
<span>
```

Como el div pero inline

[Ejemplo de elementos HTML](code/index2.html)


### Atributos

Los elementos pueden tener atributos, es decir, características como puede ser un nombre o un color.
Suelen ser todos opcionales.
Todos pueden tener id, que debe ser único en todo el documento.
Todos pueden tener style.
Todos pueden tener class.
Eventualmente diferentes elementos tendrán diferentes atributos, conocer esto básicos debería ser suficiente.

``` html
<div style="background-color: red">
```

[Ejemplo de estilos inline usando atributos](code/index3.html)


