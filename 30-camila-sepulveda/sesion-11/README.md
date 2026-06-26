# sesión 11 - 22/05
# Estados y camara web:
## como crear un sketch y definir variable estados:
Al principio del código, fuera de las funciones, se debe crear una variable global, que guarde
en qué pantalla nos encontramos. Empezará en 0.
Ejemplo:
let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final
luego se crea el lienzo, en function setup, para continuar en el function draw se crea la
estructura del estado, se usa el switch, dependiendo del valor de la variable estado, el
programa dibujara una cosa u otra.
Ahora se crea las funciones que se inventó en el paso
anterior. Cada una tendrá un diseño y un color diferente
para que se perciba un cambio.

se usa switch (estado)
case 0 :
pantallaDeInicio();
break
case 1 :
el siguiente paso es programar visualmente cada estado, que son funciones propias, para
luego hacer la lógica de cambio y reiniciar, para pasar de un estado a otro y lograr que

vuelva al comienzo, usando la función mousePressed(), cada vez que se haga clic la
variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.
## Interacción con el teclado:
se puede usar con barra espaciadora se puede hacer con teclas específicas por ejemplo se
puede hacer con tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final. Ademas se
puede realizar con botones reales en la pantalla, por ejemplo en lugar de hacer clic en
cualquier parte de la pantalla, se puede crear un botón real de HTML usando la librería de
p5.js, esto es mucho más profesional para menús.
## Zona de clic:
Son Botones dibujados con rect o ellipse.
Si no se usa los botones de HTML y prefieres se puede evaluar si el mouse
estaba dentro de esa caja al hacer clic.
## Interacciónes Automaticas por tiempo:
Por medio del tiempo, de un temporizador, es Ideal para una
pantalla de introducción (Splash Screen) que
dura 3 segundos y pasa sola al menú.
# Interacción con el mundo fisico
## Camara web:
createCapture(VIDEO):
Se crea una variable para la captura, declarando una
variable global que guardará el flujo de video de
la cámara web.
Luego inicializar la cámara en el function setup()
utilizamos el comando especial
createCapture(VIDEO) esto pedirá permiso
al navegador para encender la cámara del
computador. También se define el tamaño con
captura.size(x,y); y es muy importante
agregar captura.hide(); para que esconda el
video que HTML pone abajo por default.
Por ultimo Dibujar la cámara en el function draw()
usando la función image(). p5.js toma cada cuadro
(frame) de la cámara y lo dibuja en el lienzo en
tiempo real.

# Diseño Responsivo ( windowResized)
al modificar el tamaño de la pantalla o dispositivo, no se modifique el diseño sí no que se
adapta y no se estropee.

Se debe crear un canvas con dimensiones dinámicas:
para eso se usa las variables windowWidth y windowHeight
Luego se crea un evento windowResized
Para después usar valores relativos, con esto p5 actualiza las variables wiidth y height
automáticamente con el tamaño actual del lienzo.
entonces todos los valores de posición y tamaño se deben pensar en relación proporcional
a esas variables.
El siguiente paso es incluir factor de referencia que es min(width, height). Esto observa el
ancho y alto de la ventana, los compara y se queda solo con el que sea más pequeño en
ese momento.
Por otro lado se puede usar el translate, push y pop.
en lugar de hacer matemáticas complejas en cada rect o ellipse usamos translate para
mover el origen del mundo.
y siempre se utiliza push y pop para cada elemento.

# agregar imagen loadImage()
Primero se sube la imagen en sketch files, se recomienda si son más de una imagen
guardarla en carpetas y se recomienda no usar espacio en los nombre asignado al archivo.
el paso dos se debe declarar y precargar la imagen, creando una variable global para
guardar la imagen, por medio de un let, para luego usar la function preload, donde se carga
la imagen con el loadimage, para que pueda cargar la imagen dentro del canvas.
elemplo:
let miImagen;
function preload() {
miImagen= LoadImage(‘holaImg’)
para continuar La imagen se dibuja usando la función image()
Esta función requiere mínimo 3 argumentos, pero

acepta 5 si queremos controlar su tamaño de
forma responsiva.
Sintaxis: image(nombreVariableImagen, x, y, ancho, alto);
## Ejemplo avanzado de distrorcion de imagen:
loadPixels() :
Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la
memoria de acceso rápido (RAM). Se comunica directamente con la
tarjeta gráfica píxel por píxel en tiempo real.
loadPixels() crea un &quot;puente&quot; temporal para que puedas analizar la
información de forma masiva y fluida.
Para modificar los pixeles, pasa por un proceso de lectura = get(x,y), escritura =
set(x,y,nuevoColor) y la actualización = updatePixels().

sesión 12

# Sonido
## loadSound();
El primer paso para realizar es hacer clic en la flecha pequeña que está hacia la derecha (&gt;)
ubicada en la esquina superior izquierda del editor (debajo del botón de
Play). Esto abrirá el menú de archivos laterales. Luego se debe hacer clic en el icono de + o
el menú desplegable junto a Files, para luego seleccionar Upload file para poder subir un
archivo de nombre corto y sin espacios, que se debe Arrastrar en un archivo de sonido.,
mp3 o .wav y guardarlo en una carpeta llamada assets.
El paso número dos es declarar y precargar el sonido en function preload().
Para aquello se crea una variable global al inicio del código para guardar el sonido,
utilizando la función function preload() se inicia la variable y se carga el sonido con
loadSound().
Para activar el sonido Le damos play al sonido en el function setup con:
nombreVariable.play();
Con esta instrucción de que el sonido va a comenzar
cuando le demos play a nuestro sketch, donde se puede activar idealmente con
mousePressed()
### Métodos de control del sonido

nombreVariable.play() : Reproduce el sonido una vez.
nombreVariable.loop() : Reproduce el sonido en bucle infinito.
nombreVariable.stop() : Detiene el sonido por completo.
nombreVariable.pause() : Pausa el sonido en el segundo actual.
nombreVariable.setVolume(valor) : Modifica el volumen.
Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).
nombreVariable.rate(valor) : Modifica la velocidad de
reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más
grave) y 2.0 es el doble (suena más agudo).
### Métodos de consulta o estados del sonido
nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y
false si no.
nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().
nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en
loop().
nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción
(ej: 12.45).
nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej:
180.0).
nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un
número entre 0.0
y 1.0).
nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para
normal, 2.0 para el
doble).
Por otro lado también se puede trabajar con sintetizadores como para el sonido, para eso se
necesitan componentes básicos de un sintetizador, como el oscilador de p5.Ocillator que es
un motor que genera el sonido.Tiene distintas &quot;formas
de onda&quot; que cambian el timbre del sonido:
como la onda &#39;sine&#39; que tiene un sonido suave, como una flauta, &#39;triangle&#39; que tiene un
sonido intermedio, &#39;sawtooth&#39; donde su sonido es brillante y rasposo, como de sintetizador
de los 80, &#39;square&#39; su sonido ess retro, tipo videojuego de 8 bits, La Frecuencia que controla
qué tan rápido vibra la onda. Matemáticamente, a mayor
frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz
(Hz) y por ultimo la amplitud, que controla la altura de la onda, lo que percibimos como el
volumen. Va de 0.0 (silencio) a 1.0 (máximo).