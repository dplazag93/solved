# Test 1

Para responder a este test encontrarás un archivo llamado `test.js` en esta 
misma carpeta donde hay un pequeño fragmento de código que deberás analizar 
y responder a las siguientes cuestiones. 

1. En el fragmento de código de nuestro archivo (`test.js`) podemos encontrar
 hasta 3 variables. ¿Podrías decirnos cuál sería el valor de todas ellas al 
 finalizar la ejecución del script?
**RESPUESTA:**

- rgb:
    red: "#FF0000",
    green: "#00FF00",
    blue: "#0000FF"
    white: "#FFFFFF",
    black: "#000000"


- wb:
    white: "#FFFFFF",
    black: "#000000"


- colors: 
    red: "#FF0000",
    green: "#00FF00",
    blue: "#0000FF"
    white: "#FFFFFF",
    black: "#000000"


2. Modifica el código para que las variables `rgb` y `wb` mantengan sus valores 
iniciales y `colors` tenga los valores de ambas al finalizar la ejecución del 
script.
**RESPUESTA:**

        var rgb = {
            red: "#FF0000",
            green: "#00FF00",
            blue: "#0000FF"
        };

        var wb = {
            white: "#FFFFFF",
            black: "#000000"
        };
        var colors={};
        colors = Object.assign(colors, rgb);
        colors = Object.assign(colors, wb);


3. Además, tenemos un bug localizado en dispositivos con Internet Explorer… 
El código de nuestro script no funciona y necesitamos que se ejecute también 
en este navegador. ¿Sabrías identificar cuál es el problema? ¿Qué solución nos
 propones?


**RESPUESTA:**
El problema radica en que Internet Explorer no soporta la funcion assign.
Propongo utilizar la función extend de jQuery, que sí está soportada por IE.

    var rgb = {
        red: "#FF0000",
        green: "#00FF00",
        blue: "#0000FF"
    };

    var wb = {
        white: "#FFFFFF",
        black: "#000000"
    };
    var colors = $.extend(rgb, wb);

**PS**: No es estrictamente necesario tener Internet Explorer para poder identificar y/o resolver el bug. 
