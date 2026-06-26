# sesión 06 - 19/06

## SONIDO  
loadSound()  
### * Paso 1.
Subir archivos en formato .mp3 o .wav. Como recomendacion usar nombres de archivos cortos. Hacer una carpeta llamada ASSETS.

### * Paso 2.  
Declarar y precargar el sonido. function preload()  
Creamos ina variable global al inicio del código para guardar nuestro sonido. Usamos la función function preload() inicializamos nuestra variable y cargamos el sonido con loadSound()

### * Paso 3.  
Activar mi sonido.  
Le damos play al sonido en el function setup con: nombreVariable.play(); Con esta instrucción, el sonido va a comenzar cuando le damos play a a nuestro sketch.


## Métodos de control del sonido:
nombreVariable.play(); Reproduce el sonido una vez  
nombreVariable.loop(): Reptoduce el sonido en bucle infinito  
nombreVariable.stop(): Detiene el sonido por completo  
nombreVariable.pause(): Pausa el sonido en el segundo actual  

nombreVariable.setVolume(valor):  Modifica el volumen. Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo)   
nombreVariable.rate(valor): Modifica la velocidad ce reproducción 1.0 es normal, 0.5 es la mitad de la velocidad (suena más grave) y 2.0 es el doble (suena más agudo)

## Métodos de consulta o estados del sonido  
nombreVariable.isPlaying(): Devuelve true si el sonido está sonando en este momento y false si no. 
nombreVariable.isPaused(): Devuelve true si el sonido fue congelado con pause()  
nombreVariable.isLooping(): Devuelve true si el sonido está configurado para repetrise en loop()  
nombreVariable.currentTime(): Devuelve el segundo exacto en el que va la reproducción (ej. 12.45)  
nombreVariable.duartion(): Devuelve la duración total del archivo de audio en segundos(ej: 180.0)  
nombreVariable.getVolumen(): Devuelve el nivel de volumen actual del reproductor (un numero entre 0.0 y 10)  
nombreVariable.getRate(): Devuelve la velocidad de reprodycción actual (ej: 1.0 para normal, 2.0 para el doble)

### DESAFÍO CLASE  
radio  
play/pause LO HICE YUJU

## SÍNTESIS DE AUDIO p5.sound()  

### Componentes de un sintetizador básico  
- El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas de onda" que cambian el timbre del sonido:
* 'sine' (onda senoidal o sinusoidal: un sonido suave, como una flauta)
* 'triangle' (onda triangular: sonido intermedio)
* 'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los 80)
* 'square' (onda cuadrada: sonido retro, tipo videojuegos de 8 bits)

- La frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor frecuencia, el sonido es más agudo y a menor frecuencia es más grave.

- La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el volumen. Va de 0.0 (silencio) a 1.0 (máximo)



