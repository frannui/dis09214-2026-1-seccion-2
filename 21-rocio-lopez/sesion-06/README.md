# 4 PILARES FUNDAMENTALES 

1. Descomposición
2. Reconocimiento de patrones
3. Abstracción
4. Algoritmos

   1. *Descomposición* - Consiste en tomar un problema grande y complejo y romperlo en partes más pequeñas y
manejables. - Se traduce en el uso de Funciones Propias. En lugar de un draw() gigante,
tienes una función dibujarIconos() y otra calcularDiferencia()


   2. *Reconocimiento de patrones* - Observar tendencias o regularidades dentro de un problema. Si algo se repite o sigue una
lógica constante, podemos automatizarlo. - Se traduce en el uso de Bucles ***FOR** - Si hay un patrón, el código lo repite por
ti con solo tres líneas.

  3. *Abstración* - Es filtrar la información innecesaria y quedarse solo con las características que definen el
problema. Es crear una representación simbólica de la realidad. - Se traduce en el uso de variables y la función map() - Una posición de
mouse (mouseX) se "abstrae" para convertirse en un valor.

  4.*Algoritmos* - Es el diseño de una serie de reglas ordenadas para resolver el problema. Es el plan de acción que debe seguir el sistema. - Se traduce en el Diagrama de Flujo y en las Condicionales if/else. Es el mapa lógico que conecta todas las partes anteriores.


## FUNCIONES PROPIAS 

**FUNCIÓN** FUNCTION(); 

function Nombredelafunción() { }

```javascript

let x = 0;
let y = 0;
let speedX = 3;
let speedY = 6;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0);
  
  // Llamamos a nuestros módulos (funciones)
  dibujarObjetos();
  moverObjetos();
  comprobarBordes();
}

// --- MÓDULOS o FUNCIONES PROPIAS ---

function dibujarObjetos() {
  noStroke();
  fill(255, 0,0);
  ellipse(x, 200, 50, 50);

  fill(24, 113, 237);
  ellipse(200, y, 50, 50);
}


function moverObjetos() {
  x += speedX; // Esto es lo mismo que x = x + speedx
  y += speedY;
}


function comprobarBordes() {
   
   if (x > width || x < 0) {
    speedX *= -1;
  }
  // Rebote vertical
  if (y > height || y < 0) {
    speedY *= -1;
  }

}
