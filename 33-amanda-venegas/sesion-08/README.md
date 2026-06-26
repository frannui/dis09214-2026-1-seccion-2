# 🌸 # sesión 8 - Estados y cámara web 🌸  

PASO 1 CREAR Y DEFINIR VARIABLE ESTADOS

1. Al principio de tu código (fuera de las funciones), debes crear una
variable que guarde en qué pantalla nos encontramos. Empezará en 0.

<img width="791" height="113" alt="image" src="https://github.com/user-attachments/assets/0e4b06ee-8603-410c-8a93-a96ce400e01d" />

Paso 2 configurar el lienzo (funtion setup) 

2. Creamos el lienzo de fondo donde va a ocurrir toda la magia.

Paso 3 

3. Aquí usamos un switch Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.

<img width="346" height="387" alt="image" src="https://github.com/user-attachments/assets/a40d3041-0791-4b9e-835d-f2bd92fda8e6" />

Paso 4 Programar visualmente cada estado (funciones propias)

4. Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.
   
<img width="515" height="419" alt="image" src="https://github.com/user-attachments/assets/f16f3d39-6dd6-4139-bcb9-0666078892a1" />

Paso 5  La logica del cmbio y el reinicio

5. Para pasar de un estado a otro y lograr que vuelva al comienzo,
usamos la función mousePressed() Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.

HAY MUCHAS FORMAS DIFERENTES DE CAMBIAR DE UN ESTADO A OTRO

1.Interración con el teclado 

la barra espaciador o enter , o alguna tecla especifica 

2 . Botones reales en la pantalla

 En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de
HTML usando la librería de p5.js. Esto es mucho más profesional para menús.

3 . Zona de clic

 Si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(),
 puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.

4. Interacciones automáticas

Por Tiempo (Temporizador): Ideal para una pantalla de introducción (Splash Screen) que
dura 3 segundos y pasa sola al menú.

## Camara web 

1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
   
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.

   EJEMPLOS DE PROFE

https://editor.p5js.org/PoliMujica/sketches/Xdk0YBVbQ
https://editor.p5js.org/PoliMujica/sketches/sK_BYepGn
https://editor.p5js.org/PoliMujica/sketches/OVsazOghk
https://editor.p5js.org/PoliMujica/sketches/cYCPjuXft
https://editor.p5js.org/PoliMujica/sketches/L9QBzREF3
   

