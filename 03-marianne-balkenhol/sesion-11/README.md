# CLASE 11
## Sonido y sintesis de audio

Subir sonidos a p5*

Recomendaciones:

- formatos mp3 o wav
- nombres cortos
- minusculas
- sin espacios
- crear carpeta ASSETS

**Preload**

Se crea una variable global para guardar el sonido.

El sonido se carga con loadSound() dentro de preload().

**Activar sonido**

Con play() el sonido comienza al ejecutar el sketch.

## Control del sonido

**Metodos de control**

- play() = reproduce una vez
- loop() = reproduce en bucle
- stop() = detiene completamente
- pause() = pausa el sonido
- setVolume() = modifica el volumen
- rate() = modifica la velocidad de reproduccion

**Metodos de consulta**

- isPlaying() = indica si el sonido esta sonando
- isPaused() = indica si esta pausado
- isLooping() = indica si esta en loop
- currentTime() = devuelve el tiempo actual
- duration() = devuelve la duracion total
- getVolume() = devuelve el volumen actual
- getRate() = devuelve la velocidad actual


## Sintesis de audio

La sintesis de audio se realiza con p5.sound().

**3 componentes de un sintetizador basico**

**Oscilador**

Es el motor que genera el sonido.

Tipos de onda:

- sine = sonido suave
- triangle = sonido intermedio
- sawtooth = sonido brillante y rasposo
- square = sonido retro tipo videojuegos

**Frecuencia**

Controla que tan rapido vibra la onda.

- mayor frecuencia = sonido mas agudo
- menor frecuencia = sonido mas grave

Se mide en Hertz (Hz).

**Amplitud**

Controla el volumen.

- 0.0 = silencio
- 1.0 = volumen maximo

