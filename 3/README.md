# Test 3

En este caso, tenemos un código usando el objeto `Promise` (Promesa). Las *promises* 
(promesas) nos permiten manejar situaciones asíncronas en nuestras ejecuciones, 
pero tenemos un pequeño problema… No es una solución totalmente cross-browser. 
Sabemos que no funciona en Internet Explorer así que nos gustaría saber cómo 
modificarías nuestro código (`test.js`) para que funcione correctamente.

**RESPUESTA:**
Internet Explorer no soporta por si mismo las promesas, por lo que habría que recurrir a una librería de terceros para hacerlo funcionar.
En caso de no querer tener una deuda tecnológica, bastaría con evaluar si el navegador es Internet Explorer y en caso de serlo, notificar al usuario de que debe usar otro
tipo de navegador como Chrome o Firefox, bloqueando su entrada a la web.