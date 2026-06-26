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
