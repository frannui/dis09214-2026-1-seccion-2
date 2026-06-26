# Sonido en pj5*


Paso 1 - Subir el archivo a la biblioteca del codigo ( mp3 - .wav ) se recomienda poner nombres breves y sin mayúsculas ni espacios. 


Paso 2 - Declarar y precargar el archivo. - Creamos una variable global al inicio del codigo, luego usamos la función funtion preloand() 


Paso 3 - le damos play al sonido en el function setup


## Control de sonido - 

nombreVariable.play() Comienza el audio


nombreVariable.loop() Comienza el audio el repeticion


nombre.Variable.stop() Detiene el audio 


nombre.Variable.pause() Pausa el audio


javascript ´´´

let miSonido;
let tam1, tam2; 

let botonX = 200;
let botonY = 400; 
let botonRadio = 100; 

let boton2X = 600; 
let boton2Y = 500;
let boton2Radio = 100; 

function preload() {
  miSonido = loadSound('gil.mp3'); 
}

function setup() {
  createCanvas(800, 800);
  frameRate(5);
} 

function draw() {
  background(97, 38, 25);

  tam1 = random(10, 220);
  tam2 = random(20, 100);
  tam3 = random(20, 350);

  noStroke();
  fill(64, 26, 19, 40);
  circle(100, 100, tam3); 
  circle(150, 600, tam3); 
  circle(700, 550, tam3); 
  circle(400, 300, tam3); 
  circle(700, 200, tam3); 
  circle(550, 700, tam3); 

   noStroke();
  fill(66, 12, 12, 40);
  circle(200, 200, tam3); 
  circle(250, 650, tam3); 
  circle(600, 550, tam3); 
  circle(440, 100, tam3); 
  circle(600, 270, tam3); 
  circle(500, 600, tam3); 


  noStroke();
  fill(209, 2, 2, 90);
  circle(botonX, botonY, tam1); 

  noStroke();
  fill(209, 2, 2, 90);
  circle(boton2X, boton2Y, tam1);
  
  textAlign(CENTER);
  textSize(50);
  fill(255);
  text("Quiero amar sin pensar \n sin pensar en que me harán", 400, 400);
}

function mousePressed() {
  // detectar clic en el primer círculo (PLAY)
  let d1 = dist(mouseX, mouseY, botonX, botonY); 
  if (d1 < botonRadio) {
    // verifica si NO está sonando
    if (!miSonido.isPlaying()) { 
      miSonido.play();
    }
  }
  
  // detectar clic en el segundo círculo (PAUSE)
  let d2 = dist(mouseX, mouseY, boton2X, boton2Y);
  if (d2 < boton2Radio) {
    // verifica si ESTÁ sonando
    if (miSonido.isPlaying()) { 
      miSonido.pause(); 
    }
  }
}
´´´
https://editor.p5js.org/janisepulveda/sketches/AjFMyVSlB 


### sintesis de audio 

*Oscilador*  (p5.Oscillator): Motor que genera el sonido. Formas de onda que cambian el timbre del sonido:
1. Sine = (onda senoidal ó sinusoidal: un sonido suave, como una flauta).
2. Triangle = (onda triangular: sonido intermedio).
3. Sawtooth = (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los 80).
4. Square = (onda cuadrada: sonido retro, tipo videojuego de 8 bits).


*Frecuencia*  (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor
frecuencia, el sonido es más agudo.


*Amplitud*  (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el
volumen.




