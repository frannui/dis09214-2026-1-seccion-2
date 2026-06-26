# sesión 05/06

Como crear un estado 

*Paso1 - crear y definir una variable estado, se declara en funtion. 

*Paso2 configurar el lienzo - crear el lienzo de base donde ocurrirá todo. 

*Paso 3 Crear la variable estado - function draw - se crea un switch dependiendo del valor de la variable estado, el programa dibujara una u otra cosa. 

*Paso 4 - programar visualmente cada estado. - Funciones propias 

*Paso 5 - La lógica de cambio y reinicio. - Para pasar de un estado a otro y lograr que vuelva al comienzo, se usa la función mousepressed() Cada vez haga clic, la variable aumentará. Si llega a 3 (Después del estado 2) volverá a 0. 

inicia en el espacio 0 - importante en el examen utilizar tamaño de texto según la adaptabilidad del tamaño del canvas  

EJEMPLO 

´´´javascript 

let estado = 0;

function setup() {
  createCanvas(400, 400);
  textAlign(CENTER, CENTER);
}

function draw() {
  background(220);

  switch (estado) {
    case 0:
      pantallaInicio();
      break;
    case 1:
      pantallaExperiencia();
      break;
    case 2:
      pantallaFinal();
      break;
  }
}

function pantallaInicio() {
  background(135, 206, 250);
  fill(0);
  textSize(24);
  text("ESTADO 0: INICIO", width / 2, height / 2 - 20);
  textSize(16);
  text("Haz clic para continuar", width / 2, height / 2 + 20);
}

function pantallaExperiencia() {
  background(144, 238, 144);
  fill(0);
  textSize(20);
  text("ESTADO 1: EXPERIENCIA", width / 2, height / 2 - 20);
  
  // Interactividad extra en este estado
  fill(255, 100, 100);
  ellipse(mouseX, mouseY, 30, 30);
  
  fill(0);
  textSize(14);
  text("Mueve el mouse. Haz clic para avanzar.", width / 2, height / 2 + 40);
}

function pantallaFinal() {
  background(255, 182, 193);
  fill(0);
  textSize(24);
  text("ESTADO 2: FINAL", width / 2, height / 2 - 20);
  textSize(16);
                                                                                                                                                                                                                                                                                [[[ t[ext("Haz clic para volver al inicio 🔄", width / 2, height / 2 + 20);
}


function mousePressed() {
  estado = estado + 1;
  
  if (estado > 2) {
    estado = 0;
  }
}
´´´

 Teclado - EJ: keyPressed()
Botones reales - EJ: Crear variable ( let botonSiguente. ) dentro de function setup ( botonSiguente = createButton('Siguiente Pantalla'); -  (botonSiguiente.position(150, 350);) // Posición en la pantalla -  Cuando se haga clic en ÉSTE botón, se ejecuta la función cambiarEstado (botonSiguiente.mousePressed(cambiarEstado);) 
Zona de clic - Botones de clic. - prefieres dibujar tus propios botones con rect(), puedes evaluar si el mouse estaba dentro de esa caja al hacer clic. - EJ:  text("BOTÓN", width / 2, height / 5.2); 
Interacciones automáticas - Por tiempo, temporizado. Ideal para pantalla de introducción. - Declara estado.  let tiempoTranscurrido = millis() - tiempoInicioEstado;

capture video 
1. Crear la variable para la captura, declarar una variable global que guardará el flujo de video de tu cámara web.

2. Inicializar la cámara en el function setup() utilizamos el comando especial createCapture(VIDEO) esto le pedirá permiso al navegador para encender la cámara del computador. También definimos tamaño con captura.size(x,y); y es muy importante agregar captura.hide(); para que esconda el video que HTML pone abajo por default.
3. Dibujar la cámara en el function draw() usamos la función image(). p5.js toma cada cuadro (frame) de la cámara y lo dibuja en el lienzo en tiempo real 
´´´ javascript 

let captura;

function setup() {
  createCanvas(640, 480);
  
  // Capturamos la cámara del computador
  captura = createCapture(VIDEO); 
  captura.size(500, 480); //define tamaño de la captura de video
  captura.hide(); // Esconde el duplicado de HTML
  textAlign(CENTER);
}

function draw() {
  background(0);
  
  // Dibujamos la captura en la posición (0,0)
  image(captura, 0, 0, width, height);
}
 

´´´ 
EFECTOS

  //filter(THRESHOLD, umbralT);
  //filter(INVERT);
  //filter(GRAY);
  //filter(POSTERIZE,umbralP);
  //filter(BLUR,4);// cambiar valores

CAPTURA ESPEJO EN PIXELES 

´´´javascript 

let captura;

function setup() {
  createCanvas(640, 480);
  
  // Inicializamos la cámara web
  captura = createCapture(VIDEO);
  captura.size(640, 480);
  captura.hide(); // Ocultamos el video original de HTML
  
  noStroke(); // Quitamos los bordes de los círculos 
}

function draw() {
  background(15, 15, 25); // Un fondo azul oscuro 

  // Cargamos los pixeles del video de la cámara en la memoria
  captura.loadPixels();

  // Usamos el mouse para definir el tamaño del "pixel" (mínimo 6px, máximo 50px)
  let tamañoPixel = floor(map(mouseX, 0, width, 50, 6, true));

  // Recorremos la pantalla saltando de "tamañoPixel" en "tamañoPixel"
  for (let y = 0; y < captura.height; y = y + tamañoPixel) { 
    for (let x = 0; x < captura.width; x += tamañoPixel) {
      
      // Calculamos la posición del pixel actual en el arreglo de pixeles de p5
      let indice = (x + y * captura.width) * 4;
      
      // Extraemos los componentes de color de ese pixel exacto
      let r = captura.pixels[indice];
      let g = captura.pixels[indice + 1];// aumentar valor
      let b = captura.pixels[indice + 2];

      // Pintamos nuestro propio círculo con el color del pixel de la cámara
      fill(r, g, b);
      
      // El tamaño de cada círculo reacciona al brillo del pixel
      let brillo = (r + g + b) / 3;
      let tamañoCirculo = map(brillo, 0, 255, 0, tamañoPixel);
      
      // Dibujamos el círculo en la coordenada correspondiente
      ellipse(x, y, tamañoCirculo, tamañoCirculo);
    }
  }
}
´´´









