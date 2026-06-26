# EXAMEN
# Manspreading

**Autor:** Amanda Venegas

## Información del proyecto

**Nombre del proyecto:** Manspreading

**Autor:** Amanda Venegas

---

# Descripción objetiva

## ¿Qué es el proyecto?

*Manspreading* es un proyecto interactivo desarrollado en p5.js que busca representar de forma visual el fenómeno del manspreading y evidenciar cómo este comportamiento puede afectar el espacio de otras personas en el transporte público.

## ¿Qué se ve en pantalla?

El proyecto presenta tres pantallas: una pantalla de inicio, una pantalla de instrucciones y una pantalla de interacción.

En la escena principal se observa el interior de un vagón de metro con un hombre y una mujer sentados uno al lado del otro. A medida que el usuario interactúa mediante clics, el personaje masculino comienza a ocupar cada vez más espacio con la apertura de sus piernas.

## ¿Qué elementos visuales aparecen?

* Fondo del metro.
* Personaje masculino.
* Personaje femenino.
* Ícono de enojo.
* Botón de reinicio.
* Texto con título e instrucciones.
* Partículas y cambios de color como respuesta a la interacción.

---

# Descripción conceptual

La idea central del proyecto es representar visualmente cómo una acción cotidiana, como el manspreading, puede afectar el espacio compartido y generar incomodidad en otras personas.

El sistema utiliza la interacción del usuario para exagerar progresivamente el comportamiento del personaje masculino, haciendo visible una situación que normalmente puede pasar desapercibida.

### Regla de oro del sistema

**A mayor cantidad de clics, mayor es el espacio que ocupa el personaje masculino y mayor es la incomodidad que experimenta la mujer.**

### Relación con la problemática de género

El proyecto representa cómo ciertas conductas cotidianas pueden reflejar desigualdades en el uso del espacio público. El manspreading muestra una ocupación desproporcionada del espacio compartido, obligando a la mujer a desplazarse y manifestando visualmente la incomodidad que esto genera.

---

# Input / Output y sistema

## Input

* Clic del mouse.
* Botón de reinicio.

## Proceso

Cada clic modifica distintas variables del programa.

El personaje masculino aumenta gradualmente el tamaño de su cuerpo y separa más sus piernas. Cuando se alcanza el máximo de interacción, la mujer se desplaza, aparece un ícono de enojo, se generan partículas y comienza a reproducirse un sonido.

## Output

* Crecimiento del personaje masculino.
* Cambio de color del fondo.
* Desplazamiento de la mujer.
* Aparición del ícono de enojo.
* Sistema de partículas.
* Reproducción de sonido.
* Posibilidad de reiniciar la interacción.

---

# Pensamiento computacional

El funcionamiento del proyecto se basa en la interacción del usuario mediante clics. Cada clic produce cambios dentro de la escena, haciendo que el personaje masculino ocupe cada vez más espacio y que la mujer reaccione alejándose.

A medida que aumenta la cantidad de clics, también cambian otros elementos del sistema, como el color del fondo, la aparición del ícono de enojo, las partículas y el sonido. Todos estos cambios siguen reglas definidas en el programa y ocurren en momentos específicos de la interacción.

La experiencia está organizada en tres estados: una pantalla de inicio, una pantalla de instrucciones y una pantalla de interacción. Además, el usuario puede volver al estado inicial utilizando el botón de reinicio.


---

# Referentes

## Referentes visuales

* Interior del Metro de Santiago como escenario cotidiano del transporte público.
* Señaléticas e ilustraciones de campañas sobre el uso responsable del espacio público.

<img width="451" height="640" alt="image" src="https://github.com/user-attachments/assets/26182615-0403-4dac-8791-052bee865f94" />
Universitat Oberta de Catalunya. (2023, 22 de marzo). Mansplaining, manspreading y gaslighting. UOC News. https://www.uoc.edu/es/news/2023/074-mansplaining

## Referentes teóricos

* Concepto de manspreading como práctica relacionada con el uso desigual del espacio compartido.
* Reflexiones sobre convivencia y género en espacios públicos.

---

# Diagrama de flujo
---
### Mi diagrama de flujo : https://miro.com/app/board/uXjVHPyg7iQ=/
---
<img width="257" height="493" alt="image" src="https://github.com/user-attachments/assets/bc1e5e11-77ea-4da1-aa3e-ffb6abfda6f0" />
<img width="246" height="534" alt="image" src="https://github.com/user-attachments/assets/34433890-8c00-4ffe-ac68-46682577d1d3" />

---
### Mi codigo p5js : https://editor.p5js.org/amanda.venegas1/sketches/HXfX3WCua
---


### Mi codigo 

``` let imagenFondo;
let chicaI;
let chicoI;
let enojoI;
let imagenReinicio;
let estado = 0;
let click = 0; 
let rojo; 
let miSonido;
let desplazamientoMujer = 7;

// 9. ARRAY asignado para guardar las partículas creadas por la clase
let particulas = []; 

// Variables dinámicas para las posiciones de los personajes
let chico, chica;

class Particula {
  constructor(x, y) {
    this.x = x;
    this.y = y;
    this.vx = random(-2, 2);
    this.vy = random(-5, -2); 
    this.alfa = 255; 
    // El tamaño de la partícula escala según el ancho de la ventana
    this.tamano = random(width * 0.008, width * 0.015);
  }

  actualizar() {
    this.x += this.vx;
    this.y += this.vy;
    this.alfa -= 7; 
  }

  mostrar() {
    noStroke();
    fill(150, 20, 20, this.alfa); 
    circle(this.x, this.y, this.tamano);
  }

  estaMuerta() {
    return this.alfa <= 0; 
  }
}

// ==========================================
// FUNCIONES DEL SISTEMA P5.JS
// ==========================================
function preload() {
  // NOTA: Asegúrate de que los nombres de archivo coincidan exactamente en tu carpeta
  miSonido = loadSound("tusoundtrack.mp3");
  imagenFondo = loadImage("metrofondo.png");
  chicaI = loadImage("chica.png"); 
  chicoI = loadImage("chico.png"); 
  enojoI = loadImage("enojo.png");
  imagenReinicio = loadImage("reinicio.png");
}

function setup() {
  // El lienzo toma el tamaño total de la ventana del navegador
  createCanvas(windowWidth, windowHeight); 
  frameRate(20);
  
  // Verificación de seguridad para el volumen del sonido
  if (miSonido && typeof miSonido.setVolume === 'function') {
    miSonido.setVolume(0.15); 
  }
  
  // Inicializa las posiciones responsivas
  inicializarDimensiones();
}

function draw() {
  if (estado == 0) {
    pantallaInicio();
  } else if (estado == 1) {
    pantallaInstrucciones();
  } else {
    backgroundS();
    gestionarParticulas(); 
    hombre();
    mujer();
    titulo();
    enojo(); 
    botonReiniciar();
  }
}

// Esta función se ejecuta automáticamente cuando cambias el tamaño de la ventana
function windowResized() {
  resizeCanvas(windowWidth, windowHeight); 
  inicializarDimensiones();
}

function inicializarDimensiones() {
  let chicoAnchoBase = width * 0.30;
  let chicoAltoBase = chicoAnchoBase * 1.2;

  chico = {
    x: width * 0.60,       
    y: height * 0.50 - 20,      
    ancho: chicoAnchoBase,   
    alto: chicoAltoBase, // <--- Ahora heredará la proporción exacta sin estirarse
    piernaD: width * 0.63, 
    // ... el resto de tu objeto chico igual 
    piernaI: width * 0.54, 
    tamPierna: width * 0.05,
    lado: width * 0.09,
    originalPiernaD: width * 0.63, 
    originalPiernaI: width * 0.54
  };

  // Hacemos lo mismo con la chica para que tampoco se deforme al redimensionar
  let chicaAnchoBase = width * 0.17;
  let chicaAltoBase = chicaAnchoBase * 2.3; // Ajusta según la proporción de tu imagen

  chica = {
    x: (width / 2) - 95,        
    y: (height / 2) + 160,
    ancho: chicaAnchoBase,   
    alto: chicaAltoBase, 
    circuloX: (width / 2) - 95, 
    originalX: (width / 2) - 95,
    originalCirculoX: (width / 2) - 95
  };
  
  // ... (el resto de tu función con los "click *" se queda exactamente igual)
  chico.ancho += click * (width * 0.008);
  chico.alto += click * (height * 0.006);
  chico.lado += click * (width * 0.003);
  chico.piernaD += click * (width * 0.006);
  chico.piernaI -= click * (width * 0.01);
  chico.tamPierna += click * (width * 0.004);
  
  if (click >= 5) {
    chica.x = chica.originalX - (width * 0.036);
    chica.circuloX = chica.originalCirculoX - (width * 0.036);
  }
}

function pantallaInicio() {
  background(0);
  textAlign(CENTER, CENTER);
  textFont("Georgia");
  fill(255);

  textSize(min(width * 0.05, 75));
  text("Manspreading", width / 2, height * 0.38);

  textSize(min(width * 0.025, 38));
  text(
    "Es una costumbre en la que algunas personas abren\n" +
    "excesivamente las piernas al sentarse, ocupando más\n" +
    "espacio del necesario y llegando a incomodar a la\n" +
    "persona que está a su lado.",
    width / 2,
    height * 0.52
  );

  textSize(min(width * 0.02, 30));
  fill(250, 250, 250, 200);
  text("Haz clic en la pantalla para continuar", width / 2, height * 0.82);
}

function pantallaInstrucciones() {
  background(0);
  fill(255);
  textAlign(CENTER);

 textSize(min(width * 0.04, 56));
  text("Instrucciones", width / 2, height * 0.17);

 textSize(min(width * 0.022, 34));
  text(
    "1. Haz clic en la pantalla para interactuar.\n \n" +
    "2. Cada clic aumenta el espacio que ocupa el personaje masculino.\n \n" +
    "3. La interacción tiene un máximo de 5 clics.\n \n" +
    "4. Observa los cambios en la escena.\n \n" +
    "5. Reinicia cuando quieras.",
    width / 2,
    height * 0.52
  );

textSize(min(width * 0.018, 26));
  fill(250, 250, 250, 200);
  text("Haz clic en la pantalla para comenzar", width / 2, height * 0.82);
}

function backgroundS() {
  if (!chico) return;

  // valores fijos tipo tu código original
  let anchoMin = chico.ancho - (click * (width * 0.008));
  let anchoMax = chico.ancho + (5 * (width * 0.008));

  rojo = map(click, 0, 6, 0, 255);

  if (click === 0) rojo = 0;

  background(rojo, 0, 0);

  if (imagenFondo) {
    image(imagenFondo, 0, 0, width, height);
  }

  fill(rojo, 0, 0, 150);
  rect(0, 0, width, height);
}

function mujer() {
  noStroke();

  if (chicaI) {
    image(
      chicaI,
      chica.x - chica.ancho / 2,
      chica.y - chica.alto / 2,
      chica.ancho,
      chica.alto
    ); 
  }

  let diametroCirculo = width * 0.10;
  let cabezaY = (chica.y - chica.alto * 0.35) - 110 ;

  if (click == 6) {
    fill(random(255), random(255), random(255));
    circle(
      chica.circuloX + desplazamientoMujer,
      cabezaY,
      random(diametroCirculo * 1.5)
    );
  } else {
    fill(238, 157, 225);
    circle(
      chica.circuloX + desplazamientoMujer,
      cabezaY,
      diametroCirculo
    ); 
  }
}

function hombre() {
  if (!chico) return;

  push();
  fill(91, 69, 169); 
  noStroke();

  rect(chico.piernaI, chico.y + (chico.alto * 0.4), chico.tamPierna, height * 0.27); 
  rect(chico.piernaD, chico.y + (chico.alto * 0.4), chico.tamPierna, height * 0.27); 

  imageMode(CENTER);
  rectMode(CORNER);
  
  if (chicoI) {
    image(chicoI, chico.x, chico.y, chico.ancho, chico.alto);
  }
  pop();
}

function titulo() {
  push();
  fill(255);
  textSize(width * 0.032);
  textFont("Georgia");
  textAlign(CENTER, TOP);
  text("¿Como ocupas el espacio?", width / 2, height * 0.05);
  pop();
}

function enojo() {
  if (click >= 5) {
    push();
    let cabezaY = (chica.y - chica.alto * 0.35) - 150;
    translate(chica.circuloX + 30, cabezaY); 
    rotate(frameCount * 0.05);  
    imageMode(CENTER);
    let tamEnojo = width * 0.05;
    if (enojoI) {
      image(enojoI, 0, 0, tamEnojo, tamEnojo);  
    }
    pop();

    if (click == 6) {
      if (frameCount % 2 == 0) { 
        let origenX = chica.circuloX + random(-width * 0.02, width * 0.02);
        let origenYParticles = cabezaY + random(-height * 0.03, height * 0.03);
        particulas.push(new Particula(origenX, origenYParticles)); 
      }
    }
  }
}

function gestionarParticulas() {
  for (let i = particulas.length - 1; i >= 0; i--) {
    particulas[i].actualizar(); 
    particulas[i].mostrar();     
    if (particulas[i].estaMuerta()) {
      particulas.splice(i, 1); 
    }
  }
}

function botonReiniciar() {
  let botonX = width * 0.93;
  let botonY = height * 0.06;
  let diametroBoton = width * 0.04;
  push();
  fill(0);
  stroke(255);
  circle(botonX, botonY, diametroBoton);
  imageMode(CENTER);
  if (imagenReinicio) {
    image(imagenReinicio, botonX, botonY, diametroBoton * 0.6, diametroBoton * 0.6);
  }
  pop();
}

function mousePressed() {
  if (estado == 0) {
    estado = 1;
    return;
  }
  if (estado == 1) {
    estado = 2;
    return;
  }
  if (estado == 2) {
    let botonX = width * 0.93;
    let botonY = height * 0.06;
    let distanciaBoton = dist(mouseX, mouseY, botonX, botonY);
    if (distanciaBoton < (width * 0.02)) {
      reiniciar();
      return; 
    }
    
    // Si 'chico' no está listo, no procesa clics del juego
    if (!chico) return;

    if (click < 6) {
      chico.ancho += width * 0.008; 
      chico.alto += height * 0.006; 
      chico.lado += width * 0.003;
      chico.piernaD += width * 0.006; 
      chico.piernaI -= width * 0.01; 
      chico.tamPierna += width * 0.004; 
      click++; 
    }
    if (click == 5) {
      chica.x -= width * 0.036; 
      chica.circuloX -= width * 0.036; 
    }
    if (click == 6) {
      if (miSonido && typeof miSonido.isPlaying === 'function' && !miSonido.isPlaying()) {
        miSonido.loop();
      }
    }
  }
}

function reiniciar() {
  estado = 0; 
  click = 0;
  if (miSonido && typeof miSonido.stop === 'function') miSonido.stop(); 
  particulas = []; 
  inicializarDimensiones();
} 
```
