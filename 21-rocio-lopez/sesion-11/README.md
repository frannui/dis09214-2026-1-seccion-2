# sesión 06 - 14/04
## diseño responsivo (windowResized) 

Como crear un sketch que se adapte a la pantalla - 
Crea un canva con dimensiones dinamicas. -
 Se utiliza variable integradas (windowWidth, windowHeight) - Crea un evento windowResized()
usar valores relativos - todos los valores relativos de posición y tamaño actual del lienzo. - Usaremos fracciones y proporciones:  centro del lienzo(width / 2, height / 2)  - A un cuadro de la pantalla en eje x: width * 0.25)
Incluir valor de referencia. - creamos variable global referencial y asignamos que calcule el mínimo. observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea mas pequeño. 
usar push y pop - En lugar de hacer matemáticas  complejas en cada rect o ellipse, usamos translate para mov er el origen del mundo y siempre utilizando push y pop para cada figur


### imagenes

1. Subir la imagen 
2. Declarar y pre cargar la imagen
3. Dimensionar en el draw
4. image(nombreVariableImagen, x, y, ancho, alto);

javascript ´´´

let fotos = []; //creamos un Array vacío
let index = 0; // creamos variable para guardar la posición actual en el array

// Creamos también las variables para las imágenes individuales
let foto0, foto1, foto2, foto3, foto4, foto5, foto6;

function preload() {
foto0 = loadImage("easy1.jpg");
foto1 = loadImage("easy2.jpg");
foto2 = loadImage("easy3.jpg");
foto3 = loadImage("easy5.jpg");
foto4 = loadImage("easy6.jpg");
foto5 = loadImage("easy7.jpg");
foto6 = loadImage("easy4.jpg");
}

function setup() {
  createCanvas(600, 600);

  // Llenamos el array global que declaramos arriba (sin usar "let" aquí)
  fotos = [foto0, foto1, foto2, foto3];
}

function draw() {
  background(220);

  

function mousePressed() {
  index = index + 1;
}
  if (index >= fotos.length) {
    index = 0;
}
}
´´´

