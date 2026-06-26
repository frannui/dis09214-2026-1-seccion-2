# sesión 10 - 12/06  
# Diseño responsivo (windowResized)  

## ¿cómo crear un sketch que se adapte a diferentes tamaños de pantalla?  

**paso 1**  
crear canvas con dimensiones dinámicas: para esto usaremos windowWidth, WindowHeight) estas variables leen el ancho y alto disponibles en la ventana del navegador  

**paso 2**  

crear un evento windowResized()  
si el usuario estira o encoge el navegador, el lienzo se adapta al tamaño de la ventana en tiempo real  

**paso 3**  

usar valores relativos  

Ahora p5 actualiza estas variables width y height automáticamente con el tamaño actual del lienzo. hay que pensar los valores en relación proporcional a esas variables, usaremos fracciones y proporciones (ej: (width / 2, height /2) centro de lienzo), (ej: a un cuarto del lienzo en eje x (width * 0,25) ).  

**paso 4**  

incluir un factor de referencia  

Creamos una variable global (referencia) y la asignamos para que calcule el mínimo. observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.  

**paso 5**  

consejo para proyectos complejos  

En lugar de hacer matemáticas complejas con cada figura, usamos translate() para mover el punto de origen. siempre utilizando push() y pop() para cada figura o elemento.  

## Agregar imágenes loadimage()  

**paso 1** : subir imagen jpg o png a p5, en sketch files, idealmente hacer carpetas y poner nombres cortos a las imágenes y en minusculas  
1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.

2. Hacer clic en el icono de + o el menú desplegable junto a
Files.

3. Seleccionar Upload file (Subir archivo).

4. Arrastrar la imagen o buscarla en el computador.

5. Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

**paso 2** : declarar y precargar la imagen function preload()  
crear variable global al inicio del código para guardar la imagen  
usamos la función function preload() y dentro de esta cargamos la imagen con loadImage ()  

**paso 3** : dibujar y dimensionar en el draw, se dibuja usando la funcion image(). esta funcion requiere minimo 3 argumentos, pero acepta hasta 5  
```image(nombreVariableImagen, x, y, ancho, alto);```

## ejemplos avanzados de distorsión de imagen  

### loadPixels() entrar en los pixeles  

Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la Memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.

loadPixels() crea un "puente" temporal para que puedas analizar la información de forma masiva y fluida.  

get(x, y) — Lectura (El "Ojo")  
• Función: Va a la coordenada exacta (x, y) y extrae el color de ese píxel.  
• Resultado: Te devuelve un objeto de color o un arreglo con los cuatro canales esenciales: [Rojo, Verde, Azul, Alfa] (valores de 0 a 255).  
• Uso extra: Si lo usas sin coordenadas (imagen.get()), sirve para clonar o hacer una copia de respaldo completa del lienzo.  
set(x, y, nuevoColor) — Escritura (El "Pincel")
• Función: Va a la coordenada (x, y) e inyecta un color nuevo, reemplazando por completo el color que existía ahí.  
• Resultado: Modifica el mapa de píxeles en la memoria interna, preparando el nuevo aspecto de la imagen.  
updatePixels() — La Actualización
• Función: Toma todos los cambios que realizaste con set() y los sube de golpe a la pantalla.  
• ¿Por qué es MUY necesario? set() no dibuja inmediatamente; solo guarda los cambios en un borrador secreto. updatePixels() es el comando que efectivamente "pública" y renderiza el resultado final en el lienzo para que el usuario pueda verlo.  


