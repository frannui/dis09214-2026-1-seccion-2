Examen Final 
-

PROBLEMÁTICA DE GÉNERO LLEVADA AL CÓDIGO 
-

*Julio Andreé, Javiera Corral*
-
Para el examen de pensamiento computacional nos enfrentamos al desafío de seleccionar una problemática de género y transformar su significado y presencia a un sketch interactivo en la plataforma de P5.js. 
Nosotros como dupla decidimos trabajar con la problemática de  encasillar/ etiquetar a las personas según su apariencia.

Encasillar / etiquetar personas según apariencias 
-
*Etiqueta (RAE): Calificación estereotipada y simplificadora.*

*Encasillar(RAE): Clasificar personas o hechos con criterios poco flexibles o simplistas.*

El problema con encasillar personas según su apariencia es la consecuencia de quitar o eliminar la diversidad y complejidad que posee el humano, reemplazandola por etiquetas simples que promueven el pensamiento estereotipado de quienes nos perciben y de nosotros mismos.  Esto puede llevar a una crisis de identidad personal ya que al no sentirse de acuerdo con la etiqueta que otras personas te otorgan tendemos a sentir una desconexión con nuestro entorno y nosotros mismos.

las etiquetas en si no suelen ser del todo maliciosas pero al ser tan cerradas en su significado (gay, lesbiana, mujer, hombre, trans, etc.) resultan restrictivas y deshumanizantes. 

ejemplos:
-
pensar que una persona es mujer o usa pronombres femeninos solo por vestirse con vestidos y tener pelo largo o pensar que es hombre solo por vestir con pantalones y llevar el pelo estilizado de manera “masculina”.


<img width="273" height="272" alt="image" src="https://github.com/user-attachments/assets/6e405375-c861-4599-bd17-23b1362c5d50" />
<img width="424" height="281" alt="image" src="https://github.com/user-attachments/assets/b949ec00-25cf-4921-9924-c7474dcb8ae0" />


"La diversidad nos aporta riqueza en todos los sectores y ámbitos de nuestra vida. Sin embargo, en numerosas ocasiones, por simplificar tendemos a “etiquetar” a las personas dentro de una determinada categoría que los define de una manera concreta, a etiquetarlos con unas características inamovibles y concretas. Al actuar de esta manera, muchas veces inconsciente, no tenemos en cuenta que estamos limitando nuestra percepción de los demás, perdiéndonos toda la complejidad de las personas, sus matices y en definitiva, toda esa riqueza que aporta la diversidad."
*Fragmento extraído de:[divem.accem.es]( https://divem.accem.es/problema-encasillar-personas/)*

IDEA DEL SKETCH
-

*• Descripción objetiva* (arreglar)
-
¿Qué es el proyecto? 

Nuestro proyecto es un código creado en la plataforma de p5.js que tiene como función etiquetar individuos en diferentes identidades sexuales predeterminadas que pueden o no ser acertadas a la realidad.

¿Qué se ve en pantalla? 

El sketch inicia con la imagen de soy una pringada y yenesi (miembros de la comunidad LGBTQ+ e inspiraciones para nuestro filtro) que sirve como propósito de una pantalla de inicio donde se le da al usuario el nombre del sketch y las instrucciones de lo que debe hacer para interactuar con este. En la siguiente pantalla de estado la cámara del computador se activa y detecta la cara del individuo frente a ella y de forma aleatoria comienzan a circular diferentes banderas de la comunidad lgbtq+ el usuario al interactuar presionando el mouse detiene la circulación de las imágenes de las banderas y se le designa una bandera al azar. Al ser seleccionada la bandera esta se posiciona en la frente del usuario seguida de diferentes textos que las acompañan y reiteran la etiqueta designada. El último estado muestra la manera de reiniciar el filtro y volver al inicio.

¿Qué elementos visuales aparecen? 

La imagen de soy una pringada y yenesi que muestran las instrucciones del filtro, La cámara donde se aprecia la cara del usuario, la bandera LGBTQ+ que se posiciona sobre su frente, el texto que determina la identidad en un solo caso resultante (el de la bandera trans) y el confetti que celebra el resultado (el confetti solo aparece en el caso de que se muestra la bandera trans).

*• Descripción conceptual*
-
Idea central del proyecto y su relación con el sistema diseñado?

Para nuestro sketch nos centraremos en explorar la idea de determinación de identidad sexual tomando las características de diferentes etiquetas e implementarlas en una especie de selección aleatoria. el usuario deberá interactuar para ser encasillado en alguna categoría la cual puede o no ser acertada. La respuesta que dé el usuario al sketch demostrará nuestro pensar sobre la problemática tratada aunque nuestro sketch es más irónico y gracioso a la hora de demostrar el concepto a tratar.

Buscamos con el sketch hacer que el usuario se sienta minimizado a una sola identidad por culpa de un sistema invisible que no pueden controlar. Para esto pensamos implementar en nuestro sketch la cámara para detectar la cara del usuario y utilizando imágenes de las banderas de la comunidad LGBTQ+ seguidas por textos que reafirman la etiqueta seleccionada aleatoriamente por el programa el usuario tendrá el resultado pegado a su frente sin poder deshacerse de él dejando al usuario satisfecho o no con su resultado eso no importa ya que el código no está hecho para tener las emociones humanas en cuenta y el usuario llevará el peso internalizado de la etiqueta que se le asignó.

Para crear ese resultado decidimos crear un sketch algo cómico que demuestre diferentes banderas LGBTQ+ que representan las etiquetas que la sociedad le determina  de manera superficial o algo discriminatoria a cualquier ser humano sin importar su compleja personalidad e identidad, más allá de lo que se ve a simple vista. 

Para crear una sensación de aminorar el sentir o "pasa a llevar" que un individuo encasillado puede experimentar se implementa en el código partículas de confeti que acompañan al resultado y le agregan un pequeño morbo a la deshumanización de etiquetar al usuario.

*• Referentes*
-
nuestra mayor inspiración fueron los filtros de tiktok que determinaban qué bandera LGBTQ+ era la persona en pantalla. la mayoría de veces representaban al usuario de manera errónea y en los videos se nos demostraba la emoción que el usuario posee al inicio cambiar. El usuario puede animarse, decaer o hasta indignarse por el resultado adquirido.

<img width="247" height="443" alt="image" src="https://github.com/user-attachments/assets/d2c9a284-76a1-478e-a476-f5c84ba3b766" />

<img width="253" height="449" alt="image" src="https://github.com/user-attachments/assets/34c2bb97-86c1-4cda-a387-33df6af95908" />



FaceMesh de la biblioteca ml5js : utilizamos este referente para lograr mapear la cara del sujeto.
[biblioteca ml5js](https://docs.ml5js.org/#/reference/facemesh?id=methods) 

<img width="355" height="311" alt="image" src="https://github.com/user-attachments/assets/49dfaff0-da30-412f-a70b-9e6654561eb1" />


[Código que se utilizó de base para el confeti](https://editor.p5js.org/aceschen/sketches/A1Yn7XDc8)

```
let confetti = [];

function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
  for (let i = 0; i < 100; i++) {
    let col = color(random(100, 255), random(100, 255), random(100, 255), random(120, 240));
    confetti[i] = new Confetto(random(width), random(0, 30), random(10, 20), col);
  }
}

function draw() {
  background(0);
  for (let c of confetti) {
    c.move();
    c.display();
  }
}

class Confetto {
  constructor(_x, _y, _s, _c) {
    this.x = _x;
    this.y = _y; 
    this.size = _s;
    this.color = _c;
    this.shape = round(random(0, 1));
    this.speed = random(0.5, 2);
    this.time = random(1, 100);
    this.amp = random(2, 30);
  }
  
  display() {
    push();
    noStroke();
    fill(this.color);
    translate(this.x, this.y);
    translate(this.amp*cos(this.time), this.amp*sin(this.time));
    rotate(this.time);
    scale(cos(this.time), sin(this.time));
    if (this.shape == 1) {
      ellipse(0, 0, this.size);      
    } else {
      rect(0, 0, this.size, this.size/2);
    }
    pop();
  }
  
  move() {
    this.y += this.speed;
    this.speed += 0.005;
    this.time += 0.05;
    if (this.y > height) {
      this.y = 0;
      this.speed = random(0.5, 2);
    }
  }
}
```
<img width="305" height="296" alt="image" src="https://github.com/user-attachments/assets/a9f9113a-2624-409e-9c4e-124ce91226bb" />


DIAGRAMA DE FLUJO (arreglar)
-
[link de pagina](https://canva.link/e0sex9b12uywgud)
<img width="1777" height="815" alt="image" src="https://github.com/user-attachments/assets/a7366c90-2784-47b2-93af-3128b4b82a77" />


aun no agrego imagen

NUESTRO PROYECTO: ¿ERES TRANS?
-
[¿ERESTRANS?](https://editor.p5js.org/andrenaliine/sketches/eyg1--_fPm)

```
let video; //Variable que guarda la cámara que vamos a utilizar.
let faceMesh; //Variable que guardar el modelo de IA (Facemesh) de ml5js.
let options = { maxFaces: 1, refineLandmarks: false, flipped: false }; // Configuración del reconocimiento facial, reconoce solo una cara (maxFaces), no busca detalles avanzados(refineLandmarks) y no voltea la imagen de la cámara (flipped).
let faces = []; //Base de datos donde la IA guardará las coordenas del rostro.
let imagenesBanderas = []; //Lista para guardar las imagenes que subimos a files.
let banderaSeleccionada; //Variable que guardará la imagen de la bandera que se esta mostrando en la pantalla.
let confetti = []; // Lista para almacenar todas las partículas de confeti en una sola variable.
let cantidadConfeti = 100; //Cantidad de partículas que caerán en la pantalla.
let pausa = false; //Nos dice si la ruleta de banderas se detuvo o sigue girando.
let sonidos = []; //Lista para guardar todos los efectos de sonido del juego.
let estado = "inicio"; //Variable que controla en qué pantalla estamos (inicio, juego o final).
let tiempoTrans = 0; //Temporizador para contar el tiempo tras salir la bandera trans.
let duracionCelebracion = 300; //Duración de la fiesta antes de ir a la pantalla final.
let pringada1; //Variable para guardar la primera imagen de la pantalla de inicio.
let pringada2; //Variable para guardar la segunda imagen de la pantalla de inicio.
let rushh; //Variable para guardar la música de fondo que suena en bucle.
let yenesiPringada; //Variable para guardar la imagen decorativa de la pantalla final.

let gayEcho; //Variable para guardar el sonido especial de la bandera gay.
let grillos; //Variable para guardar el sonido de grillos de la bandera hetero.

let textosBanderas = [
  //Lista de textos con las frases para cada a cada bandera.
  "LGBTQARE+ o algo así", //Frase para la bandera LGBT (índice 0).
  "¡¡¡¡¡¡¡¡ES TRANS!!!!!!!!", //Frase para la bandera Trans (índice 1).
  "eres biiiiiii⸜(˃ ᵕ ˂ )⸝", //Frase para la bandera Bi (índice 2).
  "eres gay que guay", //Frase para la bandera Gay (índice 3).
  "LEEELAAAAAAAAAA", //Frase para la bandera Lesb (índice 4).
  "......", //Frase para la bandera Hetere (índice 5).
  "SOY NOBINARIE", //Frase para la bandera No Binarie (índice 6).
  "género fluido0o0oo", //Frase para la bandera Género Fluido (índice 7).
  "pan", //Frase para la bandera Pansexual (índice 8).
];

function preload() {
  //Función para cargar los archivos antes de iniciar.
  faceMesh = ml5.faceMesh(options); //Inicializamos el modelo faceMesh de ml5js y dandole las configuraciones que guardamos en el let options.
  //cargamos nuestros archivos multimedia
  imagenesBanderas[0] = loadImage("banderalgbt.png");
  imagenesBanderas[1] = loadImage("banderal.png");
  imagenesBanderas[2] = loadImage("bandera3.png");
  imagenesBanderas[3] = loadImage("banderagay.png");
  imagenesBanderas[4] = loadImage("banderalesb.png");
  imagenesBanderas[5] = loadImage("hetere.png");
  imagenesBanderas[6] = loadImage("noBinarie.png");
  imagenesBanderas[7] = loadImage("generoFluido.png");
  imagenesBanderas[8] = loadImage("pansexual.png");
  pringada1 = loadImage("pantallaInicio/pringada.png"); //Carga la foto de la Pringada para el inicio.
  pringada2 = loadImage("pantallaInicio/yenesi.png"); //Carga la foto de Yenesi para el inicio.
  yenesiPringada = loadImage("pantallaInicio/yenesiPringada.png"); //Carga la foto para el final.
  sonidos[0] = loadSound("Sonidos/aplausos.mp3"); //Carga el sonido de aplausos en la primera posición de la lista.
  sonidos[1] = loadSound("Sonidos/audiencia.mp3"); //Carga el sonido de la audiencia sorprendida en la segunda posición.
  sonidos[2] = loadSound("Sonidos/esTrans.mp3"); //Carga el audio que grita "Es Trans" en la tercera posición.
  rushh = loadSound("Sonidos/RUSH.mp3"); //Carga la canción de fondo RUSH.
  gayEcho = loadSound("Sonidos/gayEcho.mp3"); //Carga el eco para el resultado gay.
  grillos = loadSound("Sonidos/grillos.mp3"); //Carga el sonido de grillos para el resultado hetero.
}

function setup() {
  // Función que se ejecuta solo una vez
  createCanvas(640, 480); //Crea un lienzo de 640 x 480.
  rectMode(CENTER); //Configura los rectángulos para que se dibujen desde su centro y no desde la esquina.
  rushh.play(); //Inicia la música de fondo RUSH.
  textFont("Bitcount Single"); //Tipografía para todos los textos.
  for (let i = 0; i < cantidadConfeti; i++) {
    //Bucle que se va a repetir exactamente 100 veces (desde i = 0 hasta i = 99).
    let col = color(
      //Crea un color aleatorio para el confeti actual. Formato RGBA (Rojo, Verde, Azul, Alfa/Transparencia).
      random(100, 255),
      random(100, 255),
      random(100, 255),
      random(120, 240)
    );
    confetti[i] = new Confetto( //En la posición i de nuestra lista, guardamos un "nuevo" objeto de la clase Confetto (que está definida más abajo). Le pasa cuatro datos al azar (Argumentos): Una posición X cualquiera dentro del ancho del lienzo (random(width)). Una posición Y inicial cerca del borde superior (random(0, 30)). Un tamaño entre 10 y 20 píxeles. El color(col) que acabamos de calcular.
      random(width),
      random(-50, 0),
      random(10, 20),
      col
    );
  }

  video = createCapture(VIDEO); //Activa la cámara web del usuario.
  video.size(640, 480); //Configuramos la resolución del video para que coincida con el lienzo.
  video.hide(); //Sirve para ocultar el video original que p5js crea por defecto abajo del lienzo.
  faceMesh.detectStart(video, gotFaces); //Empezamos a decirle a ml5js que analice el video continuamente y cuando detecte un rostro llamará a la función "gotFaces" para darnos los datos.

  banderaSeleccionada = random(imagenesBanderas); //Con random se selecciona una bandera aleatoria de nuestra lista.
}

function gotFaces(result) {
  //Función de respuesta de la IA, result contiene toda la información que recopiló la IA de ml5js.
  faces = result; //Guardamos los resultados dentro de la variable faces para usarlas en nuestro draw.
}

function draw() {
  //Función Draw que se ejecuta a 60fps de forma continua.
  if (estado === "inicio") {
    //Si el estado actual es igual a "inicio".
    transPantallaInicio(); //Llama a la función para dibujar la pantalla inicial.
  } else if (estado === "juego") {
    //Si el estado actual es igual a "juego".
    transJuego(); //Llama a la función principal para la interacción con la cámara.
  } else if (estado === "final") {
    //Si el estado actual es igual a "final".
    transPantallaFinal(); //Llama a la función que muestra la pantalla final.
  }
}

function transPantallaInicio() {
  //Función que dibuja la interfaz del menú principal.
  background(255, 255, 0); //color el fondo.
  push(); //Guardamos una configuración que aislada.
  image(pringada1, 250, 1, 480, 480); //Dibuja la imagen de la Pringada en el lado derecho.
  image(pringada2, -85, 80, 400, 400); //Dibuja la imagen de Yenesi en el lado izquierdo.
  textAlign(CENTER, CENTER); //Alinea los textos en el centro horizontal y vertical.
  fill(0, 0, 0); //Color del texto negro.
  noStroke(); //Sin bordes.
  textSize(70); //tamaño del titulo.
  text("¿¿ERES TRANS??", width / 2, height / 7);
  textSize(18); //Tamaño de la fuente a 18 píxeles.
  fill(0, 0, 0); //Color del texto negro.
  text("Haz click para comenzar", width / 2, height / 5); //Muestra las instrucciones debajo del título.
  pop(); //Fin de la configuración aislada.
}

function transPantallaFinal() {
  //Función que dibuja la pantalla final para cuando salga la bandera trans.
  background(255, 173, 243); //Color de fondo.
  push(); //Aísla la configuración.
  image(yenesiPringada, 0, 180, 650, 300); //Pone la foto de la Yenesi y la Pringada abajo.
  textAlign(CENTER, CENTER); //Centra los textos.
  fill(0, 0, 0); //Color de relleno negro.
  noStroke(); //Sin bordes.
  textSize(65); //Tamaño de fuente a 65 píxeles.
  fill(0, 0, 0); //Relleno negro.
  text("¡ERES MUUY TRANS!", width / 2, height / 2 - 50); //Pone el texto en el centro.
  textSize(30); //Tamaño de letra a 30 píxeles.
  fill(0, 0, 0); //Color del texto en negro.
  text("¡Felicidades vv!", width / 2, height / 2 + 10); //Pone el segundo texto debajo del titulo.
  fill(0, 0, 0); //Color de texto negro.
  textSize(14); //Tamaño a 14 píxeles.
  text("Haz click para volver al Inicio", width / 2, height / 1.7); //Texto para volver a la pantalla inicial.
  pop(); //Final de configuracion de la pantalla final.
}

function transJuego() {
  //Función que ejecuta el bucle interactivo de la cámara y la ruleta.
  image(video, 0, 0, width, height); //Pone el video de la cámara.
  if (!pausa) {
    // Si NO está pausado, la bandera cambia aleatoriamente a 60 fps.
    banderaSeleccionada = random(imagenesBanderas); //Elige una bandera completamente al azar del array.
  }

  if (pausa) {
    //Si el juego se detiene porque el usuario hizo click.
    if (banderaSeleccionada === imagenesBanderas[1]) {
      // Si es la bandera trans (posición 1), activamos el confeti.
      for (let c of confetti) {
        //Bucle que recorre cada partícula dentro de la lista de confetis.
        c.move(); //Actualiza los cálculos de movimiento de la partícula actual.
        c.display(); //Pone las partículas en la pantalla.
      }
    }

    let indiceActual = imagenesBanderas.indexOf(banderaSeleccionada); // Buscamos cuál es el índice de la bandera seleccionada.
    let textoAMostrar = textosBanderas[indiceActual]; // Obtenemos el texto correspondiente a esa bandera.

    push(); //Aísla la configuración del texto trans
    fill(255); //Pinta el relleno de las figuras y las letras de blanco.
    stroke(0); //Añade un borde negro.
    strokeWeight(4); //Grosor 4 píxeles.
    textSize(42); //Tamaño del texto a 42 píxeles.
    textAlign(CENTER, TOP); //Alínea el texto horizontalmente al centro y verticalmente en la parte superior.
    text(textoAMostrar, width / 2, 40); // Aquí se dibuja el texto dinámico según la bandera que salga.
    square(90, 90, 20); //Dibuja un cuadrado decorativo en el lado izquierdo.
    quad(560, 78, 548, 82, 560, 96, 572, 82); //Dibuja un diamante decorativo en el lado derecho.
    pop(); //Termina la configuración del texto trans.

    if (banderaSeleccionada === imagenesBanderas[1]) {
      //Cambio de estado despues de los 300 fotogramas (solo para la bandera trans).
      tiempoTrans++; //Suma 1 al contador de fotogramas en cada vuelta que pasa pausado.
      if (tiempoTrans >= duracionCelebracion) {
        //Si el tiempo transcurrido supera el límite de los 300 fotogramas.
        estado = "final"; //Pasa a la pantalla final automáticamente.
        for (let i = 0; i < sonidos.length; i++) {
          //Bucle que pasa por todos los array de sonido.
          sonidos[i].stop(); //Detenemos los sonidos para que no se queden sonando en la pantalla final
        }
      }
    }
  }

  for (let i = 0; i < faces.length; i++) {
    //Bucle que procesa la lista de caras que detectó la inteligencia artificial.
    let face = faces[i]; //Guarda la información específica de la cara que se está procesando actualmente.

    if (face.keypoints && face.keypoints[9]) {
      //Verifica que existan los puntos y el punto de la frente (índice 9).
      let xRostro = face.keypoints[9].x; //Valor de la coordenada x de la frente detectada.
      let yRostro = face.keypoints[9].y; //Obtiene el valor de la coordenada y de la frente detectada.
      let anchoBandera = 120; //Ancho de la bandera.
      let altoBandera = 80; //Alto de la bandera.

      image(
        banderaSeleccionada, //Pasa la imagen de la bandera que se detuvo o está girando.
        xRostro - anchoBandera / 2, //Resta la mitad del ancho para que quede perfectamente centrada con la frente.
        yRostro - 100, //Eleva la imagen 100 píxeles hacia arriba para ponerlo sobre la frente
        anchoBandera, //Aplica el ancho configurado.
        altoBandera //Aplica el alto configurado.
      );
    }
  }

  push(); // Configuraciones para los textos informativos en la esquina inferior.
  fill(255); // Color de la letra.
  noStroke(); // Sin bordes.
  textSize(16); //Tamaño de la letra
  textAlign(LEFT, BOTTOM); //Alinea las frases hacia la izquierda y pegadas a la base.
  if (!pausa) {
    //Si la ruleta sigue girando.
    text("Haz clic para DETENER la ruleta", 20, height - 20); //Mensaje que indica detener.
  } else {
    //De lo contrario, si la ruleta ya está detenida.
    text("Haz clic para REINICIAR la ruleta", 20, height - 20); //Menasje que puede reiniciar.
  }
  pop(); //Fin de la configuración aisalda.
}

function mousePressed() {
  //Función que detecta clicks en la pantalla.
  if (estado === "inicio") {
    //Si el usuario cliquea la pantalla estando en el menú principal.
    estado = "juego"; //Cambia el estado para cargar el módulo del juego y la cámara.
    pausa = false; // Asegura que la ruleta empiece girando libremente.
    tiempoTrans = 0; // Inicializa el contador de la ruleta a cero.
  } else if (estado === "juego") {
    //Si el usuario cliquea la pantalla durante la simulación de la cámara.
    pausa = !pausa; // Invierte el valor de pausa (si corría se detiene, si estaba frenado vuelve a girar).

    if (pausa) {
      // Si el juego se acaba de detener tras el click.
      if (banderaSeleccionada === imagenesBanderas[1]) {
        // Si la ruleta se detiene en la bandera Trans...
        tiempoTrans = 0; // Se resetea el contador para asegurar los 300 fotogramas exactos
        for (let i = 0; i < sonidos.length; i++) {
          //Recorre el array de sonidos.
          sonidos[i].play(); //Activa todos los sonidos de Sonidos (aplausos, gritos, audiencia).
        }
      } else if (banderaSeleccionada === imagenesBanderas[3]) {
        // Si la ruleta se detiene específicamente en la bandera Gay (posición 3)
        gayEcho.play(); //Reproduce el audio gayEcho.
      } else if (banderaSeleccionada === imagenesBanderas[5]) {
        //Si la ruleta se detiene en la bandera Hetero (índice 5)
        rushh.stop(); // Apaga la música de fondo
        grillos.play(); // Suenan solo los grillos.
      }
    } else if (!pausa) {
      //Si el juego se reanuda quitando la pausa con un click.
      for (let i = 0; i < sonidos.length; i++) {
        //Recorre la lista de los archivos.
        sonidos[i].stop(); // Si el juego se reanuda, apagamos todos los sonidos.
      }
      gayEcho.stop(); //Apaga el sonido gayEcho si la ruleta vuelve a girar.
      grillos.stop(); //Apaga grillos y reactivar la música RUSH al volver a girar.
      if (!rushh.isPlaying()) {
        //Verifica si la canción principal de fondo se encuentra apagado.
        rushh.play(); //Vuelve a encender la música en bucle.
      }
    }
  } else if (estado === "final") {
    //Si el juego está en la pantalla final y el usuario cliquea.
    resetearAlInicio(); //Reiniciar todas las variables al principio (todo se reinicia).
  }
}

function resetearAlInicio() {
  //Función para el reseteo total.
  estado = "inicio"; //Cambia el estado a la pantalla inicial.
  pausa = false; //Desactiva la pausa para dejar la ruleta lista para girar en la próximo click.
  tiempoTrans = 0; //Reinicia a cero el conteo del temporizador trans.
  banderaSeleccionada = random(imagenesBanderas); // Elige una bandera al azar.

  for (let i = 0; i < sonidos.length; i++) {
    //Bucle para limpiar los sonidos activos.
    sonidos[i].stop(); // Asegura que los sonidos estén completamente detenidos.
  }
  gayEcho.stop(); //Asegura apagar el gayEcho.
  grillos.stop(); //Asegura apagar a los grillos.

  for (let c of confetti) {
    // Bucle para eliminar todas las partículas de papeles del lienzo.
    c.y = random(-50, 0); //Devuelve la partícula actual a una altura por arriba del lienzo
    c.x = random(width); //Le da una coordenada random en horizontal.
    c.speed = random(0.5, 2); //Reestablece la velocidad de caida.
  }
}

class Confetto {
  //class: es una plantilla o molde para crear objetos. Te permite empaquetar variables (datos) y funciones (comportamientos) juntos. Define qué propiedades tiene cada confetti y qué debe hacer.
  constructor(x, y, s, c) {
    //This es una referencia al objeto actual en el que se está ejecutando el código. Permite diferenciar entre una variable global y la propiedad específica de un objeto individual.
    this.x = x; //Punto x del confetti.
    this.y = y; //Punto y del confetti.
    this.size = s; //Tamaño del confetti.
    this.color = c; // Color del confetti.
    this.shape = round(random(0, 1)); //Elige al azar si el confeti será un círculo o un rectángulo. random(0, 1) da un decimal como 0.3 o 0.7, y round() lo redondea al entero más cercano (o 0 o 1).
    this.speed = random(0.5, 2); //Define qué tan rápido va a caer hacia abajo el confeti.
    this.time = random(1, 100); //Contador que avanzará constantemente.
    this.amp = random(2, 30); //(amplitud) define qué tan amplio será el "vaivén" u oscilación horizontal y vertical del confeti al caer.
  }

  display() {
    //Apariencia del confetti.
    push(); //Inicio grupo de dibujo aislado.
    noStroke(); //Sin borde.
    fill(this.color); //Relleno
    translate(this.x, this.y); //Traslación de figura en x,y.
    translate(this.amp * cos(this.time), this.amp * sin(this.time)); //Desplaza un poco más el origen usando trigonometría. Al combinar el coseno (cos) y el seno (sin) con el tiempo que avanza hace que las particulas caigan de esa manera.
    rotate(this.time); //Rotación del confetti sobre su propo eje usando el contador time.
    scale(cos(this.time), sin(this.time)); //Escala visual en los ejes x e y usando ondas mecánicas. Como el coseno y el seno oscilan entre -1 y 1, provoca un efecto visual para estirar el confetti.

    if (this.shape == 1) {
      //Si la propiedad shape es igual a 1, dibuja un ellipse. Si no, dibuja un rectángulo cuya altura es la mitad de su ancho.
      ellipse(0, 0, this.size); //dibuja una ellipse en las cordenadas 0,0 del tamaño de la propiedad size.
    } else {
      //de lo contrario
      rect(0, 0, this.size, this.size / 2); //dibuja una rectangulo con ancho size y altura size/2
    }
    pop(); //Fin del grupo aislado.
  }

  move() {
    //Movimiento del confetti.
    this.y += this.speed; //Aumenta la posición y del confeti según su velocidad actual, lo que hace que caiga hacia abajo.
    //Funcion MAP
    let gravedadDinamica = map(this.y, 0, height, 0.002, 0.015); //map toma la posición y (this.y) y la combierte a un valor de ravedad dinámica.
    this.speed += gravedadDinamica; //Suma la aceleración de gravedad dinámica calculada directamente a la velocidad actual de caída.
    this.time += 0.05; //Velocidad de los giros del confeti.
    if (this.y > height) {
      //Si la propiedad this.y es mayor a la altura del canvas.
      this.y = random(-20, 0); //this.y es igual a un valor aleatorio arriba de la pantalla.
      this.x = random(width); //Reubica la coordenada horizontal de manera aleatoria a lo ancho de la ventana.
      this.speed = random(0.5, 2); //this.speed es igual a un valor aleatorio entre 0,5 y 2
    }
  }
}
``` 

explicación de nuestro sistema:
-

• ¿Cuál es la regla de oro de tu sistema?

el código que creamos funciona en base al reconocimiento facial del usuario que interactúa con el programa y en base a ese reconocimiento banderas de la comunidad lGBTQ+ circulan al azar hasta detenerse al interactuar con el sketch. esto  representa la etiqueta que se le otorga al usuario en base a su "apariencia" (detectar rostro, interactuar = etiqueta de identidad).

• ¿Cómo se relaciona esta lógica con la problemática de género elegida?

con esta lógica podemos representar como la sociedad simplifica al usuario a un simple objeto para detectar visualmente y ser "juzgado" por su apariencia la cual después es analizada y etiquetada, deshumanizando al usuario. 
• Input / Output y sistema

¿Qué datos entran? (INPUT) *reconocimiento facial del usuario y click a la pantalla.*
¿Qué respuesta visual producen? (OUTPUT) *se clasifica con una bandera LGBT al detectar tu rostro o cambia con el click del mouse.*

• Pensamiento computacional

Reglas que gobiernan el sistema (inputs, procesos, outputs)
Explicación del sistema de interactividad 
*El programa al detectar el rostro del usuario empieza a circular múltiples imágenes  de las banderas de la comunidad LGBT de manera aleatoria y al interactuar con ellas se detienen y se selecciona aleatoriamente una bandera. La cual se queda pegada a la frente delusuario sin la capacidad de cambiarla por más que lo intenten.*

Mensaje final
-
Este sketch puede categorizarse como lo más divertido y estresante que hemos hecho durante este ramo, tan intrigante y lleno de nueva información que nos motiva a seguir aprendiendo y desafiando qué tan lejos puede llegar el diseño en cualquier medio que se realice. para nosotros esta problemática es bastante cercana ya que dia a dia se pone a prueba como las personas nos perciben y si su percepción es acertada o no es la incertidumbre que lleva a la ansiedad de encajar o ser visto de la mejor manera posible por todas las personas que alguna vez tuvieron que verte y categorizarse. puede ser difícil tomar esta situación como algo más que un tema extremadamente serio y ese es el desafío que nos planteamos a la hora de empezar el proyecto, que tanto podemos aligerar una carga tan grande para toda una comunidad marginada de personas que solo buscan la aceptación y comprensión de quienes los rodean, a nuestro parecer. Lo logramos con éxito.


Agradecimiento 🍰
-
gracias a melissa salgado por dar la idea de incorporar la bandera heterosexual (de manera despectiva) ⭐
