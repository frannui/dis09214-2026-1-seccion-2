# EXAMEN : 
Nombre del proyecto: ***¡Tu opinión no nos importa!***  

Hecho por : 
**Gabriela Ferrada**
**Francisca Ovalle**  

----------
**Link al P5.js:**  
[P5.js](https://editor.p5js.org/gabyferradaexe/sketches/Lt-R7fSRp)

## ¿Que es el proyecto?
*El proyecto busca expresar metafóricamente una problemática de género: la brecha de autoridad que existe hacia las mujeres. Esta se refiere a cómo a las mujeres se les otorga menos autoridad, respeto y credibilidad que a los hombres. En el día a día, muchas recibimos cuestionamientos sobre nuestra inteligencia e incluso se nos hace dudar de nuestras propias vivencias, a través de comentarios sobre experiencias que hemos vivido o temas que ya conocemos. Un caso típico es la menstruación o el embarazo, donde muchas veces se minimizan los dolores porque no se comprende que una mujer pueda soportar ciertas experiencias, poniendo constantemente en duda su conocimiento y su experiencia.
Esto programado en p5.js con una resolución nativa de 1920x1080, que se adapta al tamaño de tu navegador web, utiliza (ml5.js y faceMesh) y captura de video en vivo para reflexionar sobre la validación de la voz y el espacio a través de una experiencia en 3 estados.*  
![a](https://i.pinimg.com/1200x/62/20/d7/6220d777dc10871e90b9d966796b91c9.jpg)

## ¿Que se ve en la pantalla?
En la pantalla se pueden apreciar los tres estados de nuestro proyecto. En el primero, se observa un fondo amarillo con un espiral rojo y, en el centro, un teléfono sonando que invita al usuario a contestar mediante un recuadro con el texto ubicado en la parte inferior. Sobre el teléfono aparece la frase "¿Te gustaría que...?", haciendo alusión a esas situaciones en las que alguien interrumpe constantemente sin dejarte terminar de hablar durante una llamada.

En el segundo estado, aparece un recuadro amarillo con un agujero circular en el centro. Este recurso visual está inspirado en las clásicas escenas de sitcoms y teleseries, donde las conversaciones telefónicas entre personajes se mostraban dentro de un círculo. Además, tomamos como referencia la escena poscréditos de Toy Story 2, en la que Barbie, caracterizada como azafata, se dirige al público a través de un encuadre similar. La diferencia es que, cuando el usuario abre la boca, aparece una X roja que simboliza que "no puede hablar". Esto va acompañado de tres botones con frases como: "Déjame explicarte...", "Lo que tú quisiste decir fue...", "¿De verdad sabes?" y "A ver, te lo explico mejor...". Finalmente, al lado se ve el teléfono ya "contestado", haciendo alusión a que el usuario ya está dentro de la llamada, junto a una frase superior que lo invita a escoger una de las tres respuestas que recibirá.

En el tercer estado, la pantalla cambia a un fondo rojo con un mensaje de advertencia que dice: "Recuerda no hablar cuando te están explicando algo que ya sabes." Debajo aparece una encuesta de satisfacción con la frase: "¿Entendiste o te lo volvemos a explicar? :)", la cual permite reiniciar la experiencia y volver al estado inicial.  

#### ¿Cual es la regla de oro de tu sistema?  
**La idea de este sketch visual era darle un estilo vintsge usar este recurso de la llamada, en este caso el Facemesh es nuestro recurso clave ya que complementa todo el resto de la idea visual y hacer parte al usuario de la experiencia mostrando su rostro.**  

#### ¿Cómo se relaciona esta lógica con la problemática de género elegida?  
Queríamos abordar la problemática a través de una situación más cotidiana y  neutral, como una llamada telefónica, sin perder la esencia de nuestra segunda solemne, centrada en las frases típicas que muchas mujeres suelen escuchar. Para ello, utilizamos la lógica de emisor y receptor propia de una llamada, pero con una diferencia: en este caso, el receptor no puede responder. Esto hace alusión a la idea de que, dentro de situaciones de mansplaining, la voz de la mujer es constantemente interrumpida o invalidada, reforzando el estereotipo de que siempre sabe menos que un hombre.  
  
**INPUT**: Detecta cuando el usuario toca el telefono para cambiar al segundo estado.  
**PROCESO**: Cuando el usuario abre la boca el facesmesh coloca una X roja en la boca abierta y al tocar uno de los tres botones aparece una de las frases dichas anteriormente y abajo sale un boton para terminar la llamada y pasar al ultimo estado.
**OUTPUT**: Aparecen la señal e asvertencia y la encuesta de satisfacción que invita a que suceda el reset y vuelva al estado 1.   

#### Referentes:  
En este caso, nuestros referentes fueron las escenas que aparecen a continuación, la escena íconica de la Barbie azafata en los postcreditos de "Toy Story 2". Este recurso nos permitió reforzar la idea de que el usuario está "dentro de una llamada".
Para la paleta de colores nos inspiramos en la estética retro-pop, utilizando tonos intensos como el rojo y el amarillo, asociados a los teléfonos antiguos y a la gráfica publicitaria de mediados del siglo XX. Elegimos esta estética porque queríamos ironizar la situación: una interfaz llamativa y colorida contrasta con el contenido incómodo de las frases de mansplaining, generando un choque entre la apariencia y el mensaje crítico.  

![2](https://i.pinimg.com/736x/32/e4/9e/32e49e8f7d5339873205b813e2d8f61b.jpg)![4](https://i.pinimg.com/736x/e0/49/90/e049909bc586cc3803184fa316de3e6b.jpg)![1](https://i.pinimg.com/736x/a2/79/90/a27990d311f39674e2b84862b72f436a.jpg)  

#### Diagrama de flujo:  
![b](https://github.com/gabyferradaexe/dis09214-2026-1-seccion-2/blob/main/14-gabriela-ferrada/Examen%20final/Diagrama.jpg?raw=true)



