# sesión 12 - 19/06

## Sonidos en p5js  -----> loadSound()

💮 **Paso 1** 
- Subir tus sonidos a p5js

**1.** Hacer click en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.

**2.** Hacer clic en el icono de + o el menú desplegable junto a Files.

**3.** Seleccionar Upload file (Subir archivo).

**4.** Arrastrar el archivo de sonido. Formatos recomendados profe .mp3 o .wav

**5.** Recomendación profe: Usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS , para subir tus sonidos, igual que las imagenes.

💮 **Paso 2**
- Declarar y precargar el sonido en **function preload();**

**1.** Creamos una variable global al inicio del código para guardar nuestro sonido.

**2.** Usamos la función function preload() inicializamos nuestra variable y cargamos el sonido con loadSound()

EJ: 

<img width="382" height="107" alt="Captura de pantalla 2026-06-26 015647" src="https://github.com/user-attachments/assets/dea6a8e9-ed9b-4aa0-8690-b89506793cf0" />

💮 **Paso 3** 
- Activamos nuestro sonido

⭐Le damos play al sonido en el function setup con:

**nombreVariable.play();**

⭐ Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.

<img width="402" height="270" alt="Captura de pantalla 2026-06-26 015926" src="https://github.com/user-attachments/assets/3845fa2d-c05d-47f7-84fb-b3217599cd8c" />


#### Ideal activar mi sonido con un mousepressed 

<img width="445" height="286" alt="Captura de pantalla 2026-06-26 015907" src="https://github.com/user-attachments/assets/aeb21864-6f47-48aa-9ed8-e95b6a234fdf" />

-------------------------------------------
## ¿Cómo controlo mi sonido?

🦋 **Métodos de control de sonido**

* nombreVariable.play() : Reproduce el sonido una vez.
* nombreVariable.loop() : Reproduce el sonido en bucle infinito.
* nombreVariable.stop() : Detiene el sonido por completo.
* nombreVariable.pause() : Pausa el sonido en el segundo actual.

* nombreVariable.setVolume(valor) : Modifica el volumen. Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).

* nombreVariable.rate(valor) : Modifica la velocidad de reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0 es el doble (suena más agudo).

🌙 **Métodos de consulta o estados del sonido**

* nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.
* nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().
* nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().
* nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).
* nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).
* nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0 y 1.0).
* nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el doble).

## Desafío Radio play/pause

[Desafio radio gaby](https://editor.p5js.org/gabyferradaexe/sketches/z7DO4QgUB)

----------------------------------
### Síntesis de audio **( p5.sound() )**

📻 **3 Componentes de un SINTETIZADOR BÁSICO**

⭐ **El Oscilador (p5.Oscillator):** Es el motor que genera el sonido. Puede tener distintas "formas de onda" que cambian el timbre del sonido:

• 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).

• 'triangle' (onda triangular: sonido intermedio).

• 'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los 80).

• 'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).

⭐ **La Frecuencia (Frequence):** Controla qué tan rápido vibra la onda. Matemáticamente, a mayor frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).

⭐ **La Amplitud (Amplitude):** Controla la altura de la onda, lo que nosotros percibimos como el volumen. Va de 0.0 (silencio) a 1.0 (máximo).

---------------------------------------------
### EJEMPLO SINTETIZADOR BÁSICO

<img width="490" height="372" alt="Captura de pantalla 2026-06-26 020830" src="https://github.com/user-attachments/assets/4cd2a1d3-a4c8-4144-bb67-eac903f9e1f6" />

[EJ profe](https://editor.p5js.org/PoliMujica/sketches/FhD6y43H7)






