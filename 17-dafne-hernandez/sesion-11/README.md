# sesión 11 - 19/06  

# SONIDO EN p5.js  

**Paso 01**  
SUBIR SUS SONIDOS A P5  
Se suben de igual forma que subir una imagen, sólo que este debe ser .mp3  

**Paso 02**  
DECLARAR Y PRECARGAR EL SONIDO   
Para que esto funcione, se debe pre-cargar en el ```function preload()```  pero a diferencia de las imágenes debe ser con ```loadSound()```  

**Paso 03**  
ACTIVAR MI SONIDO  
Le damos play al sonido en el function setup con:  ```nombreVariable.play();```   
Con esta instrucción, el sonido va a comenzar cuando le demos play a nuestro sketch.   

**Lo ideal es activar el sonido con un ```mousePressed();```  

¿CÓMO CONTROLAR MI SONIDO?  

nombreVariable.play() : Reproduce el sonido una vez.  
nombreVariable.loop() : Reproduce el sonido en bucle infinito.   
nombreVariable.stop() : Detiene el sonido por completo.    
nombreVariable.pause() : Pausa el sonido en el segundo actual.  
nombreVariable.setVolume(valor) : Modifica el volumen. Recibe un número entre 0.0 (silencio) y 1.0 (volumen máximo).   
nombreVariable.rate(valor) : Modifica la velocidad de reproducción. 1.0 es normal, 0.5 es la mitad de velocidad (suena más grave) y 2.0 es el doble (suena más agudo).  


**Métodos de consulta  o estados del sonido**  

nombreVariable.isPlaying() : Devuelve true si el sonido está sonando en este momento y false si no.  
nombreVariable.isPaused() : Devuelve true si el sonido fue congelado con pause().   
nombreVariable.isLooping() : Devuelve true si el sonido está configurado para repetirse en loop().   
nombreVariable.currentTime() : Devuelve el segundo exacto en el que va la reproducción (ej: 12.45).   
nombreVariable.duration() : Devuelve la duración total del archivo de audio en segundos (ej: 180.0).    
nombreVariable.getVolume() : Devuelve el nivel de volumen actual del reproductor (un número entre 0.0 y 1.0).   
nombreVariable.getRate() : Devuelve la velocidad de reproducción actual (ej: 1.0 para normal, 2.0 para el doble).  

SÍNTESIS DE AUDIO  

3  COMPONENTES DE UN SINTETIZADOR BÁSICO    
- El Oscilador (p5.Oscillator): Es el motor que genera el sonido. Puede tener distintas "formas de onda" que cambian el timbre del sonido:  
   • 'sine' (onda senoidal ó sinusoidal: un sonido suave, como una flauta).  
   • 'triangle' (onda triangular: sonido intermedio).  
   • 'sawtooth' (onda de diente de sierra: un sonido brillante y rasposo, como de sintetizador de los 80).  
   • 'square' (onda cuadrada: sonido retro, tipo videojuego de 8 bits).  
- La Frecuencia (Frequence): Controla qué tan rápido vibra la onda. Matemáticamente, a mayor frecuencia, el sonido es más agudo; a menor frecuencia, es más grave. Se mide en Hertz (Hz).  
- La Amplitud (Amplitude): Controla la altura de la onda, lo que nosotros percibimos como el volumen. Va de 0.0 (silencio) a 1.0 (máximo).

