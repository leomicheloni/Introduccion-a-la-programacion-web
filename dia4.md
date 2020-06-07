## Lógica de la aplicación: Javascript
Vamos a trabajar en la lógica de la aplicación, la que nos permitirá agregar comportamiento a nuestra aplicación y le dará vida.

### ¿Qué es un programa?
Es un conjunto de instrucciones que le dicen al navegador qué hacer, por ejemplo, *sumar 10 veces un número*
Javascript es un lenguaje de programación, no es más que un lenguaje especial para indicar estar instrucciones de un modo que el navegador puede entenderlo.

Entonces escribimos nuestra lógica en Javascript para que el navegador la ejecute.

### ¿Y cómo hacemos para escribir la lógica?
La parte de Javascript (lo que sería el código fuente de la aplicación) se coloca en el *head* que es la sección de HTML que es para que solo procese el navegador, al usuario no le interesa lo que ponemos allí sino el resultado que mostraremos luego de algún modo.

### Nuestro primer código Javasript: El console.log
Es una función, ahora no vamos a ver en profundidad qué significa esto ni todas sus variantes, de momento solo vamos a utilizarla para poder ver el resultado de nuestras pruebas.
No nos vamos a detener ahora en comprender cómo funciona *console.log*

``` javascript
console.log(123);
```

> En javascript cada línea es una instrucción y termina con ; (esto no es siempre así pero en este curso usaremos esta forma)

Podemos ver el resultado en la consola del navegador (F12 en Firefox, Edge y Chrome en Windows)

### Las variables
Una variable es una forma de decir al navegador que recuerde un valor para luego usarlo, un lugar temporal.
Por ejemplo, queremos que recuerde mi nombre para usarlo luego, y se lo decimos.

``` javascript
let nombre = "Leonardo";
```

Como vemos arriba, la forma de hacerlo es utilizar la instrucción *let* luego el nombre que queremos que tenga la variable (un nombre para hacer referencia a la variable luego, es recomendable que tenga sentido con el valor que guarda) el digno *=* y luego el valor, en este caso entre comillas porque es un texto.

Una vez que definimos nuestra variable Javascript la va a recordar y podremos usarla en nuestro código, por ejemplo, imprimirla en la consola.

``` javascript
console.log(nombre);
```

### Tipos de datos

Al igual que para nosotros para Javascript los datos también tienen tipos, por ejemplo, no es lo mismo un número que un texto.
Inicialmete hablaremos de dos tipos, numéricos, textos (o cadenas de textos o strings) y booleanos (verdero / falso)

Javascript no dispone de una forma de indicar los tipos,sino que los infiere, es decir que determina a partir de lo nosotros escribimos de qué tipo debería ser la variable, además luego podemos cambiar el tipo del mismo modo.

``` javascript
var nombre = "Leonardo";
```

Por ejemplo si nota que escribimos algo entre comillas decidirá que es un string, si no que es un número

``` javascript
var valor = 12;
``` 

### Sumar tipos

En Javascript es posible sumar peras con manzanas, o mejor dicho, números con strings, al detectar el signo + Javascript intentará interpretar ambos valores como el mismo tipo y mostrar un resultado (el modo en que lo hace no siempre es claro y no es conveniente dejar que Javascript decida cómo hacerlo)
Ejemplos

``` javascript
let number1  = 2;
let number2 = 1;
let result = number1 + number2;
console.log(result);
```

``` javascript
let message  = "hoy es día ";
let day = "martes";
let text = message + day;
console.log(text);
```

``` javascript
let message  = "hoy es día ";
let day = 1;
let text = message + day;
console.log(text);
```

### Asignaciones
Se pueden asignar variables a otras, o sumar variables con literales (valores escritos directamente)

[Ejemplo](code/index5.html)


