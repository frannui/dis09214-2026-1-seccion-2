# sesión 09 - 05/04  
# Estados y camaras web 

## ¿como crear un sketch con diferentes variables?  

**paso 1** crear y definir variables de estado  
al principio de tu código (fuera de las funciones), debes crear una
variable que guarde en qué pantalla nos encontramos. Empezará en 0.  
```let estado = 0; // 0 = Inicio, 1 = Experiencia, 2 = Final```

**paso 2** configurar el lienzo (function setup)  


**paso 3** crear la estructura del estado  
aquí usamos un switch dependiendo del valor de la variable estado, el programa dibujara una cosa u otra  

break (detener) el switch  

**paso 4** programar visualmente cada estado (funciones propias)  

**paso 5** para pasar de un estado a otro y lograr que vuelva al comienzo usamos la función mousePressed cada vez que hagas clic, la variable aumentará, si llega a 3 (después del estado 2), volverá a 0  

## interacción con el teclado  
1. por barra espaciadora o enter  
2. por teclas específicas (ej: tecla 1, 2, 3)  

## botones reales en la pantalla  
en lugar de hacer clic en cualquier parte de la pantalla, puedes crear un botón real de html usando la librería de p5, esto es mucho más profesional para menús   

## zonas de clic (botones dibujados con rect o ellipse)  

Si no quieres usar botones html y prefieres dibujar el tuyo con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic.  

## interacción automática (por tiempo)  
por tiempo (temporizador): ideal para una pantalla de introducción (splash screen) que dura 3 segundos y pasa sola al menú  

# Interacción con el mundo físico  

## camara web  
createCapture(VIDEO);  

1. Crear la variable para la captura, declarar una variable global que guardará el flujo de vídeo de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial
createCapture(VIDEO) esto le pedirá permiso
al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.

3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real.  


