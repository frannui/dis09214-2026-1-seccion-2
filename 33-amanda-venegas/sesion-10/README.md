# 🌸 # sesión 10 - Sonido loadSound()🌸 

#### Paso 1 

1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de
Play). Esto abrirá el menú de archivos laterales.

2. Hacer clic en el icono de + o el menú desplegable junto a Files.

3. Seleccionar Upload file (Subir archivo).

4. Arrastrar el archivo de sonido. Formatos recomendados: .mp3 o .wav

5. Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS

#### Paso 2  - DECLARAR Y PRECARGAR EL SONIDO function preload()

1. Creamos una variable global al inicio del código para guardar nuestro sonido.

2. Usamos la función function preload() inicializamos nuestra variable y cargamos el sonido con loadSound()

#### Paso 3 

Le damos play al sonido en el function setup con:

nombreVariable.play();

Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.

LO IDEAL ES ACTIVAR MI SONIDO CON UN MOUSEPRESSED

¿CÓMO CONTROLAR MI SONIDO?

Métodos de control de sonido

<img width="458" height="256" alt="image" src="https://github.com/user-attachments/assets/07cf3810-68ee-4f20-9d2d-216053a00857" />

Métodos de consulta o estados de sonido 

<img width="658" height="224" alt="image" src="https://github.com/user-attachments/assets/4eae25d2-9b9b-473c-b19c-1188f460d20b" />

Sintesis de audio p5.sound()

3 COMPONENTES DE UN SINTETIZADOR BÁSICO

- El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas
de onda" que cambian el timbre del sonido:

 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).
 'triangle' (onda triangular: sonido intermedio).
'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los
80).
'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).


- La Frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor
frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).

- La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el
volumen. Va de 0.0 (silencio) a 1.0 (máximo).

Para revisar https://learningsynths.ableton.com/ y https://learningsynths.ableton.com/en/playground





