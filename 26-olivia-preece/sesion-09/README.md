# sesión 09 - 29/05

## INSTRUCCIONES DEL EXAMEN

1. Perfeccionar su entrega solemne 2
2. Debe tener 3 pantallas: inicio - instrucciones - interacción
3. Debe tener un RESET o forma de volver a comenzar
4. Hacer un diagama de flujo de su algoritmo- código (diseño de sistema)
5. Adaptar su sketch en p5.js para que sea windowResized canvas (windowWidth, windowHeight)

### Nuevos requisitos mínimos del código  
* Array con 1 class
* incluir perisféricos (web cam, sonidos, interacción con el teclado)
* Debe tener 3 estados y un RESET

### Repo examen el mismo que antes  
### Misma pauta  
### Entrega antes del viernes 26 de Junio en la carpeta de entrega clase 

29 mayo  
## DIAGRAMA DE FLUJO  
ALGORTIMO es una secuencia de instrucciones paso a paso, lógicas, definidas, ordenadas y finitas.  
Características  
* Presición: Cada paso debe estar clarísimo  
* Orden: Los pasos llevan una secuencia lógica
* Finitud: Tiene que terminar en algún momento, no puede ser infinito
* Definición: Si sigues el mismo algoritmo dos veces con los mismos datos, deberías obetener siempre el mismo resultado

Input(Entrada) -> Proceso -> Output(Salida)

### Diagrama de flujo:  
Representacion de un algoritmo o de los pasos de un proceso. En programación funciona como una herramienta de planificacion

(Primero inicio que parte por ejemplo con function setup (inicio siempre con ovalo), luego crear leinzo de... y luego configurar ángulos en grados. Luego llega inicio del function draw, que dice pintar fondo de color x, definir grosor de línea en x, y dibujar círculos por ejemplo base)

## ARRAYS (listas)  
Contenedor con compartimientos enumerados donde se pueden guardar múltiples elementos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arreglos (Array) son muy útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.  (Se empieza a contar desde el 0 no 1)
EJEMPLO: Imagina un tren con vagones, el tren en si es el array, pero cada vagón es un elemento, y cada elemento puede contener lo que quieras: números enteros, variables, etc)  
* Sintaxis: let nombreArray = [e0, e1, e2, e3, e4, e5]; (vamos a hacer una variable, luego el nombre del Array y luego elementos)  (el let es parecido al cons pero mejor usar let)
* Ejemplo: let colores = ["red", "orange", "yellow", "green", "blue"];
* Como uso los elementos: Primero uso el nombre del Array y el elemento -> nombreArray[n° elemento]
* Ejemplo: background(coolores[1]); Esto pintará el fondo de mi lienzo en color anaranjado.

## Class  
Una clasee o (class) es un molde o plantilla abstracta que define la estructura, los datos (propiedades) y los comportamientos (métodos) que tendrá un tipo de objeto específico.  
* Ejemplo: Imaginala como el plano de diseño de una casa o un cortador de galletas: no es el obejto real en sí, sino las instrucciones empaquetadas para fabircar infinitas copias independientes basadas en ese mismo modelo, utilizando la palabra clave new
La sintaxis básica de una clase en JavaScript se estrcutura siempre en tres partes dentro de un bloque de llaves:
1. La palabra clave calss + nombre que le quieras dar
2. El método constructor (donde se definen las propiedades del objeto usado.this).
3. La funciones personalizadas que definen lo que hace el obejto.


### DATO

para hacer que la pantalla de p5.js se achioque o agrande y el lienzo o diseño se adapte se hace con function windowResized() {
  resizeCanvas(windowWidth, windowHeight);


