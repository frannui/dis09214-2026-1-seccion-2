# sesión 10 - 05/06

# ESTADOS Y CÁMARA WEB

## ESTADOS 
### ¿Cómo crear un sketch con estados diferentes?

Paso 1  
### crear y definir variable estados  
1. Al inicio de tu código (fuera de las funciones) debes crear una variables que guarde en que pantalla nos encontramos. Variable estado();

Paso 2.  
### Configurar el lienzo (function setup)  
2. Creamos el lienzo de fondo donde va a ocurrir toda la magia. 

Paso 3  
### Crear la estructura del estado (function draw) 
3. Aqui usamos un switch. Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.

Paso 4  
### Programar visualmente cada estado (funcions propias)

Paso 5  
### La logica del cambio y el reinicio  
5. Para pasar de un estado a otro y lograr qe vuelva al inicio, usamos por ejemplo la función mousePressed() Cada vez que hagas clic, la variable aumentará. Si llegas a 3 (despues del estado 2) volveRá a 0.

#### Hay muchas formas de cambiar de un estado a otro

### 1. Interacción con el teclado  
1.1 por barra espaciadora o enter  
1.2 por teclas específicas (ej: números). Puedes hacer que la tecla 1 te lleve al inicio, la 2 a la experiencia y la 3 al final.

### 2. Botones reales en la pantalla  
2. en lugar de jacer clic en cualquier parte de la pantalla, puedes crear un botón real HTML usando la librería de p5.js. Esto es mucho más profesional para menús.

### 3. Zonas de Clic (botones dibujados con rect o ellipse)
3. si no quieres usar botones de HTML y prefieres dibujar tus propios botones con rect(); puedes evaluar si el mouse estaba dentro de esa caja al hacer clic

### 4. Interacciones automáticas (Por tiempo)  
4. Por Tiempo (Temporizador); Ideal para una pantalla de introducción (Splash Screen) que dura 3 segudos y pasa sola al menú.

## CÁMARA WEB  
createCapture(VIDEO);
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.
2. Inicializar la cámara en el function setup(); utilizamos el comando especial createCapture(VIDEO) esto le perdirá permiso al navegador para encender la cámara del computador. También definiremos tamaño con captura.size(x,y) y es muy importante qgregar captura.hide(); para que esconda el video HTML pone abajo por default.
3. Dibujar la cámara en el function draw() usamos la funcion image(). P5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real


