## Estilos

Es posible definir el estilo (combinación de colores, tipos de letra, tamaño, bordes, etc. de los elementos) directo sobre el elemento o *inline* mediante el atributo *style*

También es posible declarar estos estilos por fuera de los elementos para poder re-utizarlos.

La aproximación más simple es agregar una sección *style* en el *head* de la página.

``` html
<html>
    <head>
        <style>
        </style>
    </head>
    <body>
    </body>
</html>
```

Para definir un estilo basta con encerrar sus valores entre llaves

``` css 
{
    backgroud-color: blue;
    border: 1 1 1 1;
}
```

Para indicar sobre qué elemento queremos aplicar el estilo (o los estilos) utilizamos *selectores*

### Selectores

Un selector no es más que un texto que indica cómo hará el navegador para encontrar aquellos elementos sobre los que tiene que aplicar un estilo.

El más simple es por tipo, es decir, que simplemente utilizamos el nombre del tag

``` css 
div {
    backgroud-color: blue;
    border: 1 1 1 1;
}
```

### 

CSS significa cascade stylesheet, hojas de estilo en cascada.

Esto es porque existe un jerarquía en cómo se aplican los estilos.
Es decir, en función del tipo de selector uno tendrá mayor prioridad que otro y prevalecerá su estilo.

- Tipos de tags: el tipo de elemento.
- Clases: no es más que un nombre para agrupar estilos y hacer referencia.
- ID de elementos: atributo *id* de cualquier elemento HTML.
- Inline: definir el estilo dentro de un atributo *style*

Esto nos permite definir estilos a alto nivel que aplicarán a toda la página o aplicación, por ejemplo el tipo de fuente, y luego ir definiendo un color para todos botones del tipo "aceptar", etc. De esta manera aumenta la reutilización y es más simple hacer cambios.

Es posible combinar todo o que varios selectores afecten a uno o más elementos.

### Más de selectores

Los selectores aplican a un elemento y el estilo tiene impacto en sus hijos (hijos a nivel jerarquía en el HTML).
Se pueden encadenar selectores para hacer una discriminación más precisa (es el recomendable por un tema de velocidad también)


Algunos ejemplos de selectores:

- div => aplica a todos los elementos del tipo div
- table>tr => aplica a los *tr* hijos directos de un table
- table tr => aplica a todos los *tr* que tengan un table por ancenstro
- .clase1 => aplica a todos los elementos con la clase "clase1" (nótese el . delante del nombre)
- div.clase1 => aplica a todos los elementos del tipo div que además tenga una clase llamada "clase1"
- table>tr.clase1 => aplica a los *tr* que son hijos directos de un *table* y tienen una clase "clase1"

> Los estilos *inline* tiene siempre prevalencia sobre los demás

[Ejemplo de estilos dentro del html](code/index4.html)

[Ejemplo de estilos fuera del html](code/index5.html)