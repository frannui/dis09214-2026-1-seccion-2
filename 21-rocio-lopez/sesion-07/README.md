#sesión 7 15/04  

LOOPS WHILE AND FOR 


##LOOP 

Proceso que se repite indefinidamente - Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida. (RAE) 


Es una estructura de control que permite ejecutar un bloque de instrucciones de manera repetida mientras se cumpla una condición específica o hasta que se alcance un estado determinado. 

###WHILE 


los bucles while son útiles para repetir instrucciones mientras una condición sea verdadera. 
EJEMPLO: 


Mientras (x sea menor o igual que el alto de mi lienzo) { x incrementará 1 cada vez } 

While (x <= height) {x=x+1 }

```javascript

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  
  let x=0 
  
  while(x < width) {
    fill(233, 127, 168);  
    ellipse(x, 200, 50);
    x=x+30;
  }
} 

´´´

while rejilla 

```javascript

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(245, 73, 39);
  
  let y = 0; 
  
  while (y <= 400); 
  stroke(255); 
  strokeWeight(5);
  line(0, y, 400, y); 
  y= y + 25;
}

  let x = 0 
  while (x <= 400) { 
  stroke(255); 
  strokeWeight(5); 
  line(x, 0, x, 400); 
    x = x + 25
  }
  }


´´´

WHILE EN CIRCUNFERENCIA. 
```javascript
function setup() {
  createCanvas(400, 400);
  noFill(); //sin color de relleno en las figuras 
  strokeWeight(2); 
}

function draw() {
  background(0); //fondo negro 
  
  let diametro = 400; //creo variable de diametro y le asigno valor de 400 
  
    //loop Mientras el valor de mi variable diámetro sea mayor que 0

    
  while (diámetro > 0) {
  // asigna un color al borde alterado por mi variable diámetro
    stroke(diametro, 100, 255 - diámetro / 2); 
    
  // crea un circulo en coordenada x, coordenada y, diámetro  
    circle(width / 2, height / 2, diametro);
    
  //creamos la variable opArt que será un map de mouseX
    let opArt = map(mouseX, 0, width, 5, 50); 
    diametro = diametro - opArt; 
  }
  
}
´´´

#### FOR 4 elementos  


Una forma de repetir un bloque de código cuando se conoce el número
de iteraciones. Los bucles FOR son útiles para repetir instrucciones un
número determinado de veces.


for (inicialización variable; condición booleana; actualización){ Lo que queremos que pase cuando la condición sea verdadera }


for (let x=0 ; x <= width; x=x+1) {ellipse (x , 200, random(300))}


```javascript


for (let x = 0; x < width; x = x + 30) {
    fill(233, 127, 168);
    ellipse(x, 200, 50);
  }
}


´´´

LOOP DENTRO DE UN LOOP 
 

para no crear dos condicionales y hacerlas en un mismo loop 


 for (let x = 0; x <= width; x = x + 25) { //loop madre
    for (let y = 0; y <= height; y = y + 25) { //loop hijo 
      fill(0, 0, 255);
      ellipse(x, y, 15);  
    }
  }
}





######FRAME    COUNT  


Variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El
valor de frame Count es 0 dentro de *setup* Se incrementa en 1 cada vez que finaliza la ejecución del código en draw. 

```javascript

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0);
  
   print(frameCount);
  
  if ((frameCount <= 180)) {
    background(130, 237, 75);
    textSize(50);
    textAlign(CENTER, CENTER);
    text("olisime", 200, 200);
  }
  else {
    background(237,75,211); 
    textSize(100);
    textAlign(CENTER, CENTER);
    text("CHAO", 200, 200);
  }
  
  if(mouseIsPressed){
    frameCount = 0;
  }
}

´´´

PARA AGREGAR SEGUNDA LINEA DE TEXTO AGREGAR  "+"\n 



 if ((frameCount <= 180)) {
    background(130, 237, 75);
    textSize(80);
    textAlign(CENTER, CENTER);
    text("olisime"+"\n monite", 200, 200);** 

 



