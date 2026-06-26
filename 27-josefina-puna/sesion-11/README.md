# sesión 06 - 14/04
# Clase 11: Sonido en p5.js  
## loadSound()  
### Paso 1: Subir los sonidos a P5  
1. Hacer clic en la pequeña flecha hacia la derecha (>) ubicada en la esquina superior izquierda del editor (debajo del botón de Play). Esto abrirá el menú de archivos laterales.  
2. Hacer clic en el icono de + o el menú desplegable junto a Files.  
3. Seleccionar Upload file (Subir archivo).  
4. Arrastrar el archivo de sonido.  
Formatos recomendados: .mp3 o .wav  
5. Recomendación: usar nombres de archivo cortos, en minúsculas y sin espacios. Hacer una carpeta llamada ASSETS.

### Paso 2: Declarar y precargar el sonido   function preload()  
1. Creamos una variable global al inicio del código para guardar nuestro sonido.  
2. Usamos la función function preload()  inicializamos nuestra variable y cargamos el sonido con loadSound().  

### Paso 3: Activar mi sonido  
Le damos play al sonido en el function setup con:  
nombreVariable.play();  
Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.  

### Lo ideal es activar mi sonido con un mousePressed  

## ¿Cómo controlar mi sonido?  
### Metodos de control de sonido  
nombreVariable.play() : Reproduce el sonido una vez.  
nombreVariable.loop() : Reproduce el sonido en bucle infinito.  
nombreVariable.stop() : Detiene el sonido por completo.  
nombreVariable.pause() : Pausa el sonido en el segundo actual.  

nombreVariable.setVolume(valor) : Modifica el volumen. Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).  
nombreVariable.rate(valor) : Modifica la velocidad de reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0 es el doble (suena más agudo).  

### Metodos de consulta o estados del sonido  
nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.  
nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().  
nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().  
nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).  
nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).  
nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0 y 1.0).  
nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el doble).  

## Síntesis de audio  p5.sound()  
### 3 componentes de un sintetizador básico  
1.  El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas de onda" que cambian el timbre del sonido: 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).  'triangle' (onda triangular: sonido intermedio).  'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los 80).  'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).  
2.    La Frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).  
3.  La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el volumen. Va de 0.0 (silencio) a 1.0 (máximo). 
