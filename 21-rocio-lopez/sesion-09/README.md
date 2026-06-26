# 29 de mayo 


**Algoritmos** - instrucciones paso a paso: lógicas, definidas, ordenadas y finitas. 

**Estructura:** Input (Entrada) - Proces (Algoritmo) - Output (terminado) 

**Diagrama de flujo:** representación gráfica o el paso a paso de un proceso de programación. Se utiliza como herramienta de seguimiento 


## Array - listas 

Conocidos como arreglos, contenedor con compartiemientos enumerados bajo un mismo nombre. Son Útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.  

Sintaxis: let nombreArray = {e0 , e1 , e2, e3 , e4, e5]:  Ejemplo: let Colores = “red” , “orange , “yellow” ,  “green” , “blue”]:  - background(Colores[1]): 

´´´ javascript 
let Colores = ["red" , "orange" , "yellow" , "green" , "blue" , "purple"];
let index = 0; 
               
function setup() {
createCanvas(400, 400); 
frameRate(10); 
}


function draw() {
  background(Colores[index]); //En corchetes el color que quiero llamar
  index = index + 1; //aumenta en 1
  
  if (index >= Colores.length) { //Si el index (el numero que corre) es mayor a 0 o igual a los colores. lenght (es la cantidad de elementos que tiene mi array, en este caso 6) vuelve a ser 0 
  index = 0; //El index vuelve a cero por que el color vuelve a ser rojo 
  }
}
´´´


Para el diametro 


´´´ javascript 

let Diametro = [0,10, 50, 100, 150, 200, 250, 300, 350, 400]; // Array con numeros
let index = 0; // creamos e incializamos variable para guardar la posición del Array

function setup() {
  createCanvas(400, 400);
  background(0, 200, 150);
  frameRate(10);
  
}

function draw() {
  
  fill(252,30,200,50);
  ellipse (200,200, Diametro[index]);
  index = index + 1;
  print(index);
  
  if(index>= Diametro.length){
    index=0;
  }
}

function mousePressed(){
  background(0, 200, 150);
}


´´´

a la franja horizontal 

´´´ javascript 

let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];

function setup() {
  createCanvas(850, 600);
}

function draw() {
  background(220);

  // Creamos, definimos e inicializamos una variable para determinar la altura de cada franja de color

  let alturaFranja = height / Colores.length; //colores.lenght en este caso es = a 6

  //Repite el loop mientras "i" sea menor que el total de elementos en el array colores, aumentando "i" de 1 en 1 - esto es lo que se llama recorrer un Array

  for (let i = 0; i < Colores.length; i++) {
    fill(Colores[i]); // Cambia el color de relleno por cada elemento
    noStroke();
    rect(0, i * alturaFranja, width, alturaFranja); // Dibuja un rectángulo en una posición x,y calculada por el índice i y la alturaFranja
  }
}
´´´


Para el diametro 


´´´ javascript 

let Diametro = [0,10, 50, 100, 150, 200, 250, 300, 350, 400]; // Array con numeros
let index = 0; // creamos e incializamos variable para guardar la posición del Array

function setup() {
  createCanvas(400, 400);
  background(0, 200, 150);
  frameRate(10);
  
}

function draw() {
  
  fill(252,30,200,50);
  ellipse (200,200, Diametro[index]);
  index = index + 1;
  print(index);
  
  if(index>= Diametro.length){
    index=0;
  }
}

function mousePressed(){
  background(0, 200, 150);
}


´´´

a la franja horizontal 

´´´ javascript 

let Colores = ["red", "orange", "yellow", "green", "blue", "purple"];

function setup() {
  createCanvas(850, 600);
}

function draw() {
  background(220);

  // Creamos, definimos e inicializamos una variable para determinar la altura de cada franja de color

  let alturaFranja = height / Colores.length; //colores.lenght en este caso es = a 6

  //Repite el loop mientras "i" sea menor que el total de elementos en el array colores, aumentando "i" de 1 en 1 - esto es lo que se llama recorrer un Array

  for (let i = 0; i < Colores.length; i++) { //cuanfo i sea menor que 6, i va ir incrementando de uno en uno. 
    fill(Colores[i]); // Cambia el color de relleno por cada elemento
    noStroke();
    rect(0, i * alturaFranja, width, alturaFranja); // Dibuja un rectángulo en una posición x,y calculada por el índice i y la alturaFranja
  }
}

´´´

### CLASS 

Es un molde o plantilla abstracta que define la estructura, datos y los comportamientos que tendrá un tipo de objetos específico. - La sintaxis básica de una clase en JavaScript se estructura siempre en tres partes dentro de un bloque de llaves. - no es el objeto real en sí, sino las instrucciones empaquetadas para fabricar infinitas copias independientes basadas en ese mismo modelo utilizando la palabra clave new



La palabra clave class + nombre que le quiera dar.
El método constructor (donde se definen las propiedades del objeto usando .this)
      3.  Las funciones personalizadas que definen lo que hace el objeto.


´´´ javascript 

function setup() {
  createCanvas(500, 500);
  cuadrado1 = new cuadrado();
  cuadrado2 = new cuadrado();
  cuadrado3 = new cuadrado();
}

function draw() {
  background(129, 167, 242);

  cuadrado1.move();
  cuadrado1.show();
  cuadrado2.move();
  cuadrado2.show();
  cuadrado3.move();
  cuadrado3.show();
}

class cuadrado {
  constructor() {
    this.x = 150;
    this.y = 150;
  }

  move() {
    this.x = this.x + random(-5, 5);
    this.y = this.y + random(-5, 5);
  }
  show() {
    stroke(179, 255, 127);
    strokeWeight(4);
    noFill();
    rect(this.x, this.y, 100, 100);
  }
} 

´´´
#### Array + class 

´´´ jjavascript 
let Cuadrados = []; // Creamos un array llamado cuadrados, vacio 

function setup() {
  createCanvas(500, 500); //canvas de 500x500
  frameRate(20); //velocidad
  for (let i = 0; i < 100; i++) { //crea una variable que es igual a 0, cuando i sea mayo que 10 va ir creciendo uno a uno hasta llegar a 10
    Cuadrados[i] = new cuadrado(); //llama a array cuadrados, con eso crea un new cuadrado.
  }
}

function draw() {
  background(255);

  //loop de inicio: se ejecuta 10 veces al arrancar el programa
  for (let i = 0; i < Cuadrados.length; i++) { //fabricamos un objeto real usando el molde de la clase y lo guardamos en la psición i 
    Cuadrados[i].show(); //le dice al cuadrado actual que se dibuje en la pantalla
    Cuadrados[i].move(); //le dice al cuasrado que cambiesu posición 
  }
}
//molde
class cuadrado { //El contructor define las propiedades iniciales del cuadrado cuando nace
  constructor() {
    this.x = 250;
    this.y = 250;
  }

  move() {
    this.x = this.x + random(-5, 5); //todos nacen exactamente en el dentro horizonal 500/2
    this.y = this.y + random(-5, 5); //todos nacen exactamente en el centro vertical 55/2 
  }
  //metodo para renderizar el dibujo
  show() {
    stroke(random(255), random(255), random(255)); //colores de relleno de linea
    strokeWeight(5); //valor de linea
    noFill(); //sin relleno
    rect(this.x, this.y, 20, 20); //variable de posición + tamaño 
  }
}

´´´
