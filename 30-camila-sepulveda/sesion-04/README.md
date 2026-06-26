# sesión 04 - 23/03

P5 Js
Creado por Lauren McCarthy, es una herramienta online muy amigable para aprender a
programar y hacer arte. Es una biblioteca de JavaScript libre y de código abierto, construida
para una comunidad inclusiva y solidaria.
**Algoritmo:** secuencia de instrucciones paso a paso, con lógicas, definidas, ordenadas y
finitas que permiten solucionar un problema o hacer una tarea específica.
**Orden:** Los pasos llevan una secuencia lógica.
**Finitud:** Tiene que terminar en algún momento; no puede ser infinito.
**Definición:** Si sigues el mismo algoritmo dos veces con los mismos datos,
Siempre deberías obtener el mismo resultado.
**Estructura:**
**Entrada (Entrada):** Es la información o los ingredientes que necesitas para empezar.
Ej: ingredientes y utensilios para la preparación de una comida
Proceso o algoritmo: Los pasos lógicos que transforman esa entrada.
Ej: lista de instrucciones para hacer la comida
**Output (Salida):** El resultado final de la solución al problema.
Ej: resultado final de una comida
**Diagrama de flujo:**
Representación gráfica de un algoritmo o de los pasos de un proceso, es como una
herramienta de planificación para visualizar la lógica de un programa antes de escribir una
línea de código.
Se utilizan componentes Estándar (Simbología), para que cualquier programador pueda
entenderlo.
Lenguajes de programación:
Existen entre 700 y 900 lenguajes de programación que se utilizan actualmente en la
industria, la academia y el desarrollo de software profesional.
JavaScript y Python son los más reconocidos.

P5.js:
Es un lenguaje de programación, principalmente de la biblioteca de JavaScript, usando toda
la potencia y la sintaxis, pero te regala un &quot;vocabulario&quot; especializado para dibujar, animar y
crear cosas visuales de forma mucho más sencilla.
Funciones maestras:
setup(): Se ejecuta una sola vez al principio (para crear el lienzo), su propósito es configurar
el entorno inicial, definiendo el tamaño del lienzo (Creative Canvas), cargas de imágenes o
sonidos, establece configuraciones que no cambiarán (como el color de fondo inicial).

draw(): Se ejecuta en un bucle infinito (normalmente 60 veces por segundo), lo que permite
crear animaciones, su propósito es crear movimiento y responder a la interacción en tiempo
real. Además, donde se dibujan las formas que cambian de posición según lo que se
solicita, detectar dónde está el ratón o cambios de colores gradualmente.
CreativeCanvas:
createCanvas([ancho], [altura], [renderizador], [canvas]); Ej: createCanvas(100, 100);
createCanvas (ancho, altura); Nos sirve para crear el lienzo (lienzo) y determinar su tamaño
en píxeles, solo se pone una vez y siempre dentro de la configuración();
[renderer] : Define el motor de renderizado. P2D (por defecto): Es el modo &quot;2D&quot;. Está
activado de forma automática y está optimizado para formas básicas, texto e imágenes
planas. WEBGL: Activa el modo 3D. Utiliza la tarjeta gráfica (GPU) de tu ordenador. Es
indispensable para usar funciones como box(), sphere(), luces o texturas complejas.
[canvas] Parámetro &quot;oculto&quot; y menos utilizado, pero útil si eres desarrollador web. Por
defecto, p5.js crea un elemento nuevo y lo inyecta en HTML.
Además es un sistema de coordenadas (x,y) como un plano cartesiano, pero hay que tener
en cuenta que el punto(0,0) no está en el centro, sino en la esquina superior izquierda.
Antecedentes:
fondo(v1, v2, v3, [a]); Ej: fondo(250, 150, 228,150);
Sirve para designar el color del lienzo (lienzo).
Se puede poner en el setup(); o en el draw(), pero se obtienen diferentes resultados y
funciona con los valores de RGB.
[a] : Parámetro para el canal alfa, sirve para dar semitransparente al color del fondo. (0-255)
Donde 1 será muy transparente y 255 muy poco transparente, pero también se pueden usar
con otros parámetros.
Antecedentes: en escala de grises, el negro es 0 y el blanco es 255. En RGB está
compuesto de tres números (255,0,0);(rojo,verde,azul).
Para mencionar colores a través de texto siempre se pone entre comillas (´blue&#39;) y para
poder hacer transparencia son 4 números, background(0, 0, 255, 50); (R,G,B y el cuarto
número es el canal &quot;Alpha&quot;).
Espacio de color RGB:
R: Rojo [0 - 255] G: Verde [0 - 255] B: Azul [0 - 255] Es igual colorMode(RGB);
Espacio de color HSV /HSB:
• H: Tono [0 - 360o] • S: Saturación [0 - 100%] • B: Brillo [0 - 100%] Es igual colorMode
(HSB);
Espacio de color HSL:
H: Tono [0 - 360o] S: Saturación [0 - 100%] L: Ligereza [0 - 100%] Es igual colorMode(HSL);

Figuras geométricas:
•punto(x, y); Dibuja un solo píxel en las coordenadas dadas.
•línea(x1, y1, x2, y2); Dibuja una línea desde un punto inicial hasta un punto final.
•rect(x, y, ancho, alto); Dibuja un rectángulo. Por defecto, x y define la esquina superior
izquierda.

•elipse(x, y, ancho, alto); Dibuja un óvalo o círculo. A diferencia del rectángulo, x y define el
centro de la figura. •circle(x, y, diámetro); Una versión simplificada de la elipse cuando
quieres un círculo perfecto.
•cuadrado(x, y, lado); Un rectángulo donde todos los lados son iguales.
•triángulo(x1, y1, x2, y2, x3, y3); Necesitas darle las coordenadas de sus tres esquinas.
•cuádruple(x1, y1, x2, y2, x3, y3, x4, y4); Un cuadrilátero. Sirve para hacer formas
irregulares de cuatro lados.
Peso del golpe();
Establece el tamaño del borde de las figuras o el ancho de la línea o punto. Siempre se
pone arriba de Stroke(); que establece el color que se utiliza para dibujar puntos, líneas y
contornos de figuras.
Ej: peso de carrera(25); carrera (245, 0, 0);
NoCroke();
Se usa para que mi figura no tenga borde.
StrokeCap();
Define la forma de la línea o borde de nuestras figuras se puede dividir en las siguientes
constantes. Round, square y project, donde el round viene por defecto.
StrokeCap(cap); Ej: strokeCap(SQUARE);
llenar();
Establece el color de relleno para las figuras.
relleno (v1, v2, v3, [alfa]); Ej: relleno(252, 159, 216);
Figuras geométricas avanzadas:
Arco();
Activar el modo ángulos en el SETUP(); : angleMode(DEGREES); sirve para hacer arcos o
medio círculo. X y son las coordenadas del centro del círculo que contiene este arco, w y h
son la anchura y alto del círculo que contiene este arco, start y stop, es donde comienza y
termina el ángulo de este arco.
arco(x, y, w, h, inicio, parada) Ej: arco(250, 250, 100, 100, 270, 90).
El arco necesita grados para poder dar la dirección del arco, en ese caso se utiliza: 0°, 90°,
180°, 270°, etc, pero siguiendo la sintaxis de, arc(x, y, w, h, start, stop).