# sesión 09 - 05/06  

# ESTADOS Y CÁMARA  

Cómo crear un sketch con estados diferentes  

**Paso 01**  

CREAR Y DEFINIR VARIABLE ESTADOS   
1.  Al principio de tu código (fuera de las funciones), debes crear una variable que guarde en qué pantalla nos encontramos. Empezará en 0.
 
```let estado = 0;       // 0 = Inicio, 1 = Experiencia, 2 = Final```  

**Paso 02**  

CONFIGURAR EL LIENZO (function setup)   
2.  Creamos el lienzo de fondo donde va a ocurrir toda la magia.  

```function setup()```  

**Paso 03**  

CREAR LA ESTRUCTURA  DEL ESTADO (function draw)   
3.  Aquí usamos un ```switch``` Dependiendo del valor de la variable estado, el programa dibujará una cosa u otra.  

**Paso 04**  

ROGRAMAR VISUALMENTE CADA ESTADO (funciones propias)   
4. Ahora creamos las funciones que inventamos en el paso anterior. Cada una tendrá un diseño y un color diferente para que se note el cambio.  

```function pantallaInicio() {```  

**Paso 05**  

A LÓGICA DEL CAMBIO Y EL REINICIO  
5.  Para pasar de un estado a otro y lograr que vuelva al comienzo, usamos la función ```mousePressed()``` Cada vez que hagas un clic, la variable aumentará. Si llega a 3 (después del estado 2), volverá a 0.  

### Se puede cambiar de distintas formas de un estado a otro  

- Interacción con el teclado.
- Botones reales en la pantalla.
- Zonas de click (Botones dibujados).
- Interacciones automáticas por tiempo.

 ## CÁMARA WEB  

1. Se debe crear la variable para la captura y declarar una variable global que guardará el flujo de video de la cámara web.
2. Se debe inicializar la cámara en ```function setup()``` utilizando un comando especial ```createCapture(VIDEO)```, también se define el tamaño con ```captura.size```y es muy importante agregar el ```captura.hide();``` para que esconda el video que html pone abajo de manera default.

3. Dibujar la cámara en el ```function draw()``` usamos la ```función image()```. p5.js toma cada cuadro de la cámara y lo dibuja en el lienzo en tiempo real.

![Gato](https://i.pinimg.com/736x/90/ce/b7/90ceb75734753ebbd77da84148182967.jpg)
