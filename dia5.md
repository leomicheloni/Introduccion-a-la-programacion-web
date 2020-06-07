## Condiciones

Las condiciones son el corazón de una aplicación, permiten ejecutar una u otra parte de nuestro código si es que se cumple un criterio o condición.
Por ejemplo, un usuario de nuestra aplicación ingresa su edad, y nuestro código tiene una condición de solo dejarlo ingresar si su edad es mayor o igual a 18 años.
La instrucción para todas las condiciones en Javascript es la palabra clave *if* (en muuuchos lenguajes se usa la misma) y tiene esta forma.

``` javascript
if(condición){
    // se ejecuta este código si al condición se cumple (el resultado de su evaluación es verdadero)
}else{
    // este bloque se ejecuta si el if no se cumple, es decir, la condición no se satisface
}

```

### La condición

Para escribir nuestra condición simplemente tener que utilizar una expresión que puede ser verdadera, lo más común es que se trate de una comparación, por ejemplo:

``` javascript

let edad = 19;

if(edad > 17){
    console.log("Bienvenido!");
}else{
    console.log("Lo sentimos, solo las personas con 18 o más años pueden ingresar");
}
```

En este ejemplo luego del *if* ponemos entre paréntesis (del mismo modo que a *console.log* le indicamos qué queremos mostrar usando paréntesis) cuál es la condición que se debe cumplir. Y no es más que una simple comparación *edad > 17*.
Es posible utilizar cualquier expresión dentro de los paréntesis que se pueda evaluar, por ejemplo:

``` javascript
let nombre = "Leonardo";
if(nombre == "Leonardo"){
    console.log("Hola yo!");
}
```
En este ejemplo vemos dos cosas interesantes:
Primero, para comparar dos textos (o strings) utilizamos *==* el doble signo *=* ya que cuando usamos solo uno Javascript entiende que lo que queremos es asignar, no comparar. 
Segundo, no usamos *else* en este ejemplo, el *else* es opcional y en este caso no queremos hacer nada si la condición no se cumple, es por eso que lo hemos omitido.

``` javascript
let nombre = "Santiago";
if(nombre != "Leonardo"){
    console.log("Usted no es yo");
}

```

En este ejemplo usamos los signos *!=* que significa *distinto que* es decir, al reemplazar el primer *=* por un *!* estamos invirtiendo o *negando* la condición, es decir, el *if* se ejecutará siempre que la condición no sea verdadera.

``` javascript
let edad = 20;
let nombre = "Leonardo";
if(nombre != "Leonardo" & edad > 17){
    console.log("Usted no cumple con las condiciones para ser aceptado");
}else{
    console.log("Un gusto conocerlo");
}
```

Y en este ejemplo la condición tiene dos partes, primero *nombre != "Leonardo"* y luego *edad > 17* al unir las dos condiciones con el signo *&* estamos diciendo que ambas deben cumplirse simultáneamente para que el *if* se evalue como cierto.
Esto se conoce como un *AND* lógico, es decir, se tiene que cumplir una y la otra.

``` javascript
let nombre = "Gabriel";
if(nombre == "Leonardo" | nombre == "Gabriel"){
    console.log("Bienvenido");
}
```

Y en este ejemplo uniendo las dos condiciones *nombre == "Leonardo"* y *nombre == "Gabriel"* con el signo *|* estamos indicando que cualquiera de los dos criterios que se cumplan harán verdadera la condición.
Esto se conoce como un *OR* lógico, se puede cumplir una o la otra o ambas para que la condición sea cierta.

Podemos encadenar todas las condiciones que queramos, también comparar variables contra variables.

### Tipos de variables
Hemos visto que al declarar una variable también le asignamos su valor.

``` javascript
let nombre = "Augusto";
```

En este caso estamos declarando su nombre, su valor y también su tipo, es decir, esta variable ahora tiene dentro una cadena de texto (un string). Entonces decimos que es una variable del tipo *string*.

``` javascript
let cantidad = 12;
```

Del mismo modo al declarar esta variable con el valor *12* la estamos declarando con el tipo *number*.

``` javascript
let esReal = true;
```
Y en éste será del tipo *boolean*, porque decimos que vale *true* y el tipo *boolean* solo puede ser *true* o *false*

### Importancia de los tipos en las comparaciones

Cuando usamos *if* estamos comparando valores (como literales o como variable) y Javascript evalúa condiciones, si son iguales, mayores, etc.
En el caso que lo que comparemos sea de distinto tipo (comparar un *string* con un *number* por ejemplo) en ese momento Javascript intentará hacerlo y no nos advertirá que estamos intentanto comprar tipos diferentes, sino que intentará ver cómo puede compararlos aplicando sus criterios.

``` javascript
let valor = "12";
if(valor == 12){
    console.log("es verdad");
}
```
En este ejemplo la condición será verdadera, porque si bien *valor* es *string* y el literal es un *number* Javascript entiende que puede *convertir* el *string* en *number* (porque nota que queremos comparar con un *number*) entonces intenta hacerlo y luego compara, por lo tanto la comparación es verdadera.
Hay muchos ejemplo de esto, de conversiones de tipos que Javascript hace automáticamente al comparar y que a veces son difíciles de anticipar hasta qué punto dos valores que no son iguales serán interpretados como iguales.

### Comparaciones estrictas

La forma de comprar dos valores y asegurarnos que Javascript no intentará hacer ningún tipo de conversión es utilizar *===* o *!==*

``` javascript
let valor = "12";
if(valor === 12){
    console.log("es verdad");
}
```

[Ejemplo](code\index7.html)
