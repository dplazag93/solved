# Test 2

El fragmento de código de nuestro fichero `test.js` nos devuelve un output no 
deseado. Queremos imprimir un valor incremental a cada segundo pero lo que 
nos devuelve el código es el mismo valor en cada iteración. 

1. Sin necesidad de ejecutar el código, ¿sabrías decirnos qué valor imprimiría
 por consola el script? ¿Cuál es el motivo?

**RESPUESTA:**
Se mostraría el valor final del bucle, en este caso 5, repetido tantas veces como itere el mismo.
Es un problema causado porque el setTimeout duerme el hilo principal, asi que cuando se lance el console log, el bucle ya habrá finalizado dando lugar a que i = 5 y 
lanzandose las 5 veces correspondientes.
 
2. Sabiendo que el output que buscamos es el que encuentras bajo estas líneas… 
¿Cómo solucionarías el fragmento de código para que el output sea el deseado?

```
    > 0
    > 1
    > 2
    > 3
    > 4
```
**RESPUESTA:**
Utilizando let en lugar de var.

for (let i = 0; i < 5; i++) {
    setTimeout(function () {
        console.log(i);
    }, 1000)
}