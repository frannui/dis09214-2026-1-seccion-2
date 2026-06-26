# sesión 10 - 12/06 Apuntes
---
#### DIseño Responsivo  
El diseño responsivo consiste en adaptar el contenido para que se vea correctamente en distintos tamaños de pantalla. En lugar de utilizar coordenadas fijas, se calcula una escala según el tamaño de la ventana y se aplican transformaciones para mantener las proporciones del proyecto. Además, cuando la ventana cambia de tamaño se utiliza windowResized() junto con *resizeCanvas()* para actualizar el lienzo automáticamente.  

#### Uso de translate(), push() y pop()  
En proyectos grandes es recomendable no realizar cálculos complejos para posicionar cada figura. En su lugar se utiliza *translate()* para mover el origen del sistema de coordenadas y dibujar los elementos desde esa nueva posición.

Las funciones *push()* y *pop()* permiten guardar y restaurar el estado del lienzo. De esta forma, cualquier transformación como *translate(), rotate() o scale()* afecta únicamente al elemento que se está dibujando y no al resto del programa.  

#### Trabajar con imágenes  
Antes de utilizar una imagen en p5.js, es necesario subir el archivo al editor.  
**Se recomienda:**  
1. Crear una carpeta llamada assets.
2. Utilizar nombres cortos.
3. Escribir los nombres en minúsculas.
4. Evitar espacios en los nombres de los archivos.

#### Paso 2: Declarar y precargar la imagen  
Primero se crea una variable global que almacenará la imagen.  
Luego, dentro de preload(), se utiliza loadImage() para cargarla antes de que comience el programa. Esto asegura que la imagen esté disponible cuando se ejecute draw().  

#### Paso 3: Dibujar la imagen  
Las imágenes se muestran utilizando la función image().  
Los primeros tres parámetros son obligatorios (imagen, posición X y posición Y), mientras que el ancho y alto son opcionales si se desea modificar el tamaño de la imagen.  

#### Manipulación de píxeles
**loadPixels()**: loadPixels() carga todos los píxeles del lienzo o de una imagen en la memoria para poder acceder a ellos individualmente. Esto permite analizar o modificar la imagen píxel por píxel en tiempo real.

**get(x, y)**: La función get() lee el color del píxel ubicado en una coordenada específica.  
Devuelve un arreglo con cuatro valores:
Rojo (R), Verde (G), Azul (B), Alfa (A)  

***Cada valor va desde 0 hasta 255. También puede utilizarse sin coordenadas para copiar una imagen completa.***

**set(x, y, color)**: set() modifica el color de un píxel específico, reemplazando el color original por uno nuevo.
Los cambios quedan almacenados temporalmente hasta que se actualice la imagen.

**updatePixels()**: Después de modificar los píxeles con set(), es necesario llamar a updatePixels().
Esta función actualiza la pantalla y hace visibles todos los cambios realizados. Sin ella, las modificaciones permanecen solamente en la memoria y no se muestran al usuario.  

#### Distorsión de imágenes  
Una vez cargados los píxeles, es posible crear diferentes efectos visuales modificando su posición o sus colores.  
Algunos ejemplos mostrados en la presentación son:  
1.Cambiar la imagen para que solo conserve el canal rojo.  
2.Crear un efecto de estiramiento similar al "efecto Aladino".  
3.Generar una distorsión basada en una onda seno para deformar la imagen.  
4.Pattern Generator  
***La presentación también muestra ejemplos de interfaces generadoras de patrones (Pattern Generator), donde es posible crear composiciones visuales mediante programación utilizando parámetros que modifican las formas en tiempo real.***  

#### Recursos adicionales  
Como material complementario, la presentación recomienda consultar una lista de reproducción de tutoriales sobre imágenes en p5.js para profundizar en el uso de *loadImage()*, manipulación de píxeles y otros efectos visuales.
