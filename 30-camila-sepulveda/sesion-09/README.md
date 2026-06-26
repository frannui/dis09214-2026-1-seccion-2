# sesión 09 - 08/05
sesión 9

# Aclaraciones:
## p5
para poner códigos de p5 se inicia con tres comillas y se termina con tres ej: ´´´x´´´
un bloque de oración= ´´´código p5´´´
se usa entre medio de una oración ´código p5´
angleMode(DEGREES): configura el modo de trabajar con ángulos y no con radial

# pilares:
descomposición, reconocimiento de patrones, abstracción, algoritmos.
## Descomposición:
dividir para conquistar un problema complejo y grande, se rompe en partes pequeñas y
manejables. se hace de a poco en procesos para llevarlo de manera más liviana, se
descompone en diseño A, B, C y códigos en las funciones propias, no solo se pone todo en
draw, si no se ponen diferentes títulos para ordenar. En el código se utilizan las funciones
propias como dibujarIconos() y otra calcularDiferencia(),.

## reconocimiento de patrones:
si algo se repite o sigue una lógica constante se puede optimizar, dentro del diseño y
código. Dentro del código se utiliza Bucles (for). Si hay un patrón, el código lo repite por
con solo tres líneas.

## Abstracción:
lo importante vs el detalle, filtrar la información que es innecesaria, solo definir las
características que definen el problema y crear una representación simbólica, se usa a
través de variables, map y mouseX
## Algoritmos:
serie de reglas ordenadas para resolver el problema. Es el plan de acción que debe seguir
el sistema, receta de paso a paso. Se traduce en el diagrama de flujo y condicionales
(if/else), mapa lógico que conecta todas las partes anteriores.

# Tipos de interacción:
Interacción discreta: evento específico, donde un sistema funciona con un click como un
interruptor de encendido y apagado, como mousePressed o if(mouselsPressed.

interacción continua: cuando un sistema reacciona constantemente a un movimiento, o
estado de un usuario sin necesidad de hacer un clic, como por ejemplo con mousePressed()
o con un if(mouseIsPressed).
# Funciones propias:
Crear nuestras propias funciones, para dar modularidad al codigo, para desglosar de más a
menos, puedo mencionar esa función como carpeta, que haga elementos con esa función a
través de capas con elementos específicos que cumplan cierta acción.
function nombre de la función(){ // va debajo del draw. ej: function Dibujarfiguras() {
stroke
fill
etc
}