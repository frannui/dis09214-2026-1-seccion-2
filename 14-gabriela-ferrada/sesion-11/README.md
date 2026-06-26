# sesión 11 - 12/06

### Examen

- Podemos NO colocar figuras geométricas , no son requisito
- Diseñar o dibujar algo afuera , como en ilustrator y colocarlo en el p5js
- El diagrama de flujo no puede ser con IA
- Si nuestro proyecto no requiere instrucciones, no es obligatorio colocar, quizá queremos que sea intuitivo

-------------------------------------------
## Diseño responsivo (windowResized)
¿Cómo creamos un sketch que se adapte a diferentes tamaños de pantalla?

💙 **PASO 1**
-----> Creamos un canvas con dimensiones dinamicas, Para esto usamos las variables integradas en el sistema: **(windowWidth, windowHeight)**, estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.

<img width="550" height="102" alt="Captura de pantalla 2026-06-26 012344" src="https://github.com/user-attachments/assets/6fb43fa1-3370-4029-8dde-182d71311bcd" />

🤎 **Paso 2**
-----> Creamos un evento, **windowResized** , Si el usuario estira o encoge la ventana del navegador, el lienzo se adaptará al tamaño de la ventana en tiempo real.<img 

                                                                                                                                                                     
 <img width="506" height="90" alt="Captura de pantalla 2026-06-26 012531" src="https://github.com/user-attachments/assets/fce31ef6-9686-4b49-90f9-6b027c2f3a54" />
                                                                                                                                                            

💚 **Paso 3**
-----> Usamos valores relativos, Ahora p5.js actualiza estas variables width y height automáticamente con el tamaño actual del lienzo.

⭐ Entonces ahora todos los valores de posición y tamaño que ocupemos los tenemos que pensar en relación proporcional a esas variables.

Usaremos fracciones y proporciones:
Ej: Centro del lienzo: (width / 2 , height / 2)
Ej: A un cuarto de la pantalla en eje x: ( width * 0.25)

❤️ **Paso 4**
-----> Incluimos un factor de referencia **( referencia = min(widht,height) )** , Creamos una variable global (referencia) y la asignamos para que calcule el mínimo.

⭐ Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.

🩷 **Paso 5**
-----> **Usamos translate - push y pop** , En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para "mover el origen del mundo”.

⭐ Y SIEMPRE utilizando push() y pop() para cada figura o elemento.

[Ejemplo profe](https://editor.p5js.org/PoliMujica/sketches/8gsrkntPw](https://editor.p5js.org/PoliMujica/sketches/qDjCOtTlB) 

## DESAFIO EN CLASES! : Hacer la bandera chilena en diseño responsivo 
[Desafio gaby p5js](https://editor.p5js.org/gabyferradaexe/sketches/TnCJGx100)

-------------------------------------------------------
## Agregar imagenes ( loadImage() )

💜 **Paso 1** 
-----> Subir la imagen a p5js
**a)** Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de
archivos laterales.

**b)** Hacer clic en el icono de + o el menú desplegable junto a
Files.

**c)** Seleccionar Upload file (Subir archivo).

**d)** Arrastrar la imagen o buscarla en el computador.

**e)** Recomendación profe: Usar nombres de archivo cortos, en minúsculas y sin espacios , ademas tambien hacer una carpeta llamada ASSETS, para subir las imagenes ahí.

💛 **Paso 2** 
-----> Declaramos y precargamos la imagen **( function preload() )**

⭐ Creamos una variable global al inicio del código para guardar la imagen.
⭐ Usamos la función dentro de function preload() y cargamos la imagen con loadImage()

<img width="396" height="147" alt="Captura de pantalla 2026-06-26 014119" src="https://github.com/user-attachments/assets/7209d34d-a3d1-4973-8d93-562b9977bcbd" />


💙 **Paso 3** 
-----> Dibujamos y dimensionamos en el draw();

⭐ La imagen se dibuja usando la función image() . Esta función requiere **mínimo 3 argumentos, pero acepta 5** si queremos controlar su tamaño de forma responsiva.

**SINTAXIS:**
image(nombreVariableImagen, x, y, ancho, alto);

<img width="382" height="328" alt="Captura de pantalla 2026-06-26 014342" src="https://github.com/user-attachments/assets/83a00c8e-e4ba-4082-803b-8847e25f282e" />

--------------------------------
#### Ejemplos profe

[EJ distorsion de imagen color rojo](https://editor.p5js.org/PoliMujica/sketches/6S1tglHiR)

[EJ distorsion imagen onda seno](https://editor.p5js.org/PoliMujica/sketches/6S1tglHiR)

[EJ distorsion de pixeles efetco aladino](https://editor.p5js.org/PoliMujica/sketches/jaEqYvHew)





