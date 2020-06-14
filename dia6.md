## Bucles

Un bucle es un bloque de código que se repite una cantidad de veces dada. La cantidad de veces está determinada por el cumplimiento de una condición.

Existen diferentes bulces, en este caso vamos a centrarnos en el más conocido y clásico que existe en la mayoría de los lenguajes de programción y Javascript no es la excepción.


### Bucle for

El bucle for tiene la siguiente forma

``` javascript

for( params ){
    // código que se va a repetir
}

```

la estructura es simple, la complejidad está en los parámtetros, que son así:

``` javascript
for( declaración  ; condición a cumplir ; invocación ){
    // bloque a repetir
}
```

Como vemos el *for* recibe un parámetro en 3 partes separadas por *;* (los nombres los puse yo)

 - declaración: se puede incluir la declaración de una variable, esta parte se ejecuta solo una vez antes de iniciar el primer ciclo.
 - condición a cumplir: es una condición (similiar a un if) que se evalúan en cada ciclo y mientras sea verdad el *for* continúa.
 - invocación: un bloque de código que se ejecuta en cada ciclo.

Entonces, lo más típico es usar el for de la siguiente manera:

``` javascript
for(let i = 0 ; i<10 ; i = i+1){
    // bloque a repetir
}
```
> La expresión *i = i + 1* significa que el nuevo valor de *i* será el anterior + 1.

En este caso, en la parte de declaración se declara la variable *i*. En la condición dice que mientras *i* sea menor que 10 el bucle debe continuar, y por último en cada ciclo se ejecuta la expresión *i = i + 1* es decir, se incrementa el valor de *i*, lo que ocurre es que este bloque se ejecuta 10 veces, ya que declaramos *i* con valor *0*, lo incrementamos *1* en cada ciclo mientras sea menor que 10, es decir, *i* irá tomando los valores desde el *0* hasta el *9*.
> Lo más "normal" es escribir la expresión *i = i + 1* como *i++* que es equivalente pero más corto.

Entonces, si ejecutamos el siguiente código

``` javascript
for(let i = 0; i < 10 ; i++){
    console.log("El valor de i es: " + i);
}
```

Veremos que se escriben los valores del 0 al 9 en la consola del navegador. Listo! hicimos nuestro primer bucle.

### Otros ejemplos

Veamos algunos ejemplos de cosas que podemos hacer con un bucle *for*

#### Sumar todos los números del 1 al 100

Un ejemplo (aunque poco útil) es calcular la suma de todos los números del 1 al 100, para practicar, sería más o menos así:

``` javascript
let acumulador = 0;
for(let i = 1; i <101 ; i++){
    acumulador = acumulador + i;
}

console.log("La suma de los números del 1 al 100 es: " + acumulador);
```
Lo que hacemos el un bucle del 1 al 100 (declaramos *i* con valor 1, la condición dice que el bucle se ejecute mientras *i* sea menor que 101 y le sumamos 1 a *i* en cada iteración) y dentro del bucle tomamos el valor actual de *i* y se lo sumamos al valor actual de la variable *acumulador*.


### Sumar los números pares del 1 al 100

``` javascript
let acumulador = 0;
for(let i = 0; i <101 ; i = i + 2){
    acumulador = acumulador + i;
}

console.log("La suma de los números pares del 1 al 100 es: " + acumulador);
```
Este ejemplo es muy similar al anterior pero cambiamos la última parte del *for* en lugar de sumar 1 a *i* en cada iteración le sumamos dos y comenzamos a contar desde 0, entonces *i* tomará los valores: 0, 2, 4, etc.

[Ejemplo](code/index8.html)