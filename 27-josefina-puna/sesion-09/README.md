# sesión 06 - 14/04  
# Clase 9: Estados y Cámara web.  

## ¿Cómo se crea un sketch con estados diferentes?  
### Paso 1: Crear y definir variable estados.  
Al principio del código (fuera de las funciones), se debe crear una variable que guarde en qué pantalla nos encontramos. Empieza en 0.  
**Sintaxis:**  let estado = 0;       // 0 = Inicio, 1 = Experiencia, 2 = Final  

### Paso 2: Configurar el lienzo (function setup)  
Se crea el lienzo de fondo donde va a ocurrio toda la magia.  

### Paso 3: Crear la estructura del estado (function draw)  
Se usa un switch. Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra. 

### Paso 4: Programar visualmente cada estado (funciones propias)  
Se crean las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.  

### Paso 5: La lógica del cambio y el reinicio  
Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función mousePressed().  
Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.  

## Distintas formas de cambiar de un estado a otro  
### Interacción con el Teclado  
1. Por barra espaciadora o Enter.  
2. Por teclas específicas (ej. Números).  

### Botones Reales en la Pantalla  
En lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de HTML usando la librería de p5.js. Esto es mucho más profesional para menús.  

### Zonas de Clic (Botones dibujados con rect o ellipse)  
Si no se quiere usar botones de HTML y se prefiere dibujar botones propios con rect(), se puede evaluar si el mouse estaba dentro de esa caja al hacer clic.  

### Interacciones Automáticas (Por Tiempo)  
**Por Tiempo (Temporizador):** Ideal para una pantalla de introducción (Splash Screen) que dura 3 segundos y pasa sola al menú.  

## Interacción con el mundo físico  
### Cámara web  
*createCapture(VIDEO);*  
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.  
2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar  captura.hide(); para que esconda el video que HTML pone abajo por default.  
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.  
