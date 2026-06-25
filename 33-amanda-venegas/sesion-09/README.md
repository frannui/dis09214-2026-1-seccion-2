# 🌸 # sesión 9 - DISEÑO RESPONSIVO  (windowResized)🌸 

¿CÓMO CREAR UN SKETCH QUE SE ADAPTE A DIFERENTES TAMAÑOS DE PANTALLA?

Paso 1 Crear un canvas con dimensiones dinámicas 

Para esto usaremos las variables integradas en el sistema: (windowWidth, windowHeight) estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.

<img width="605" height="116" alt="image" src="https://github.com/user-attachments/assets/b10f4103-fec7-43d4-957a-b9f7e800872a" />

Paso 2 Crear un evento windowResized()

Si el usuario estira o encoge la ventana del navegador, el lienzo se adaptará al tamaño de la ventana en tiempo real.

<img width="595" height="123" alt="image" src="https://github.com/user-attachments/assets/3631bb39-8be8-4e76-8d29-515326d735cf" />

Paso 3 Usar valores relativos 

Ahora p5.js actualiza estas variables width y
height automáticamente con el tamaño actual
del lienzo.

Entonces ahora todos los valores de posición y
tamaño que ocupemos los tenemos que pensar
en relación proporcional a esas variables.

Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)

Paso 4 Incluir un factor de referencia 
Referencia = min(width,height)

Creamos una variable global (referencia) y la asignamos para que calcule el mínimo.

Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.

Paso 5 Usar translate  push and pop

En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para "mover el origen del mundo”.

Y siempre utilizando push() y pop() para cada figura o elemento.

---

## Agregar imagenes 

1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.

2. Hacer clic en el icono de + o el menú desplegable junto a Files.

3. Seleccionar Upload file (Subir archivo).

4. Arrastrar la imagen o buscarla en el computador.

5. Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

Paso 2 

1. Creamos una variable global al inicio del código para guardar la imagen.

2. Usamos la función dentro de function preload() y cargamos la imagen con loadImage()

Paso 3 

La imagen se dibuja usando la función image()

Esta función requiere mínimo 3 argumentos, pero acepta 5 si queremos controlar su tamaño de forma responsiva.

SINTAXIS:
image(nombreVariableImagen, x, y, ancho, alto);


## EJEMPLOS AVANZADOS DE DISTORSIÓN DE IMAGEN

#### loadPixels()

Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la
memoria de acceso rápido (RAM). Se comunica directamente con la
tarjeta gráfica píxel por píxel en tiempo real.

loadPixels() crea un "puente" temporal para que puedas analizar la
información de forma masiva y fluida.

Modificar los pixeles 

get(x, y) — Lectura (El "Ojo")
 Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.
 
 Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).

Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una
copia de respaldo completa del lienzo.
set(x, y, nuevoColor) — Escritura (El "Pincel")

 Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por
completo el color que existía ahí.

Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo
aspecto de la imagen. updatePixels() — La Actualización

Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la
pantalla.

¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios
en un borrador secreto. updatePixels() es el comando que efectivamente "publica" y
renderiza el resultado final en el lienzo para que el usuario pueda verlo.
 

P
