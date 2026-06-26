# sesión 07 - 15/05

### LOOPS   
## WHILE & FOR  
Un loop es una secuencia de repetición infinita

Un bucle o un loop (Según la RAE)  
Proceso que se repite indefinidamente  
Informática: Serie de instrucciones que se repiten indefinidamente mientras no se cumpla una condición previamente establecida.  
LOOP -> Una condición de control que permite ejecutar un bloque de instrucciones de manera repretitiva mientras se cumpla una condición específica o hasta que alcance un estado determinado.  
* Dato: El loop repite objetos, imágenes, dibujo no hace animaciones ni movimiento 

## WHILE (en español es mientars)  
Los bucles while son útiles para repetir instrucciones mientras una condicion sea verdadera. Son como sentencias if que se repite.  
while(condicíon booleana){ 
ejecuta este codigo si es true }  
mientras (x sea menos o igual que el alto de mi lienzo){  
x incrementara 1 cada vez }  
Ejemplo: while(x <= height {  
x=x+1 }

## For  
una forma de repetir un bloque de código cuando se conoce el número de iteraciones. Los bucles 'for' son útile s para repetir instrucciones un numero determinado de vecea. Son una especie de SHORTCUT para hacer loops y siempre tienen 4 elementos:  
1. Inicialización de una variable
2. Condición booleana (V-F)
3. Actualización ( Incrementación o decrementación)
4. Lo que queremos que pasé cuando la condición sea TRUE

for(inicialización variable; condición booleana; actualización){  
Lo que queremos que pase cuando la condición sea verdadera
}  
Ejemplo: for(let x=0; x<= width; x=x+1) {  
ellipse/x,200,random(300))  
}

## NESTED LOOPS  
Un loop dentro de otro loop  
un for dentro de otro for  
for(inicialización variable; condición booleana; actualización){  
lo que queremos que pase cuadno esta condición sea verdadera  
for(inicialización cariable; condición booleana; actualización){  
lo que queremos que pase cuando esta condición sea verdadera  
}  
ejemplo: for (let x=0 ; x <= width; x=x+25) {

for (let y=0 ; y <= height; y=y+25) {
fill (0, 0, 255);
ellipse (x , y, 15);
}
}

* el loop que va a ser primero es el que esta dentro

## frameCount  
variable numérica que registra la cantidad de fotogramas dibujados desde que comenzó el boceto. El valor de 'frameCount' es 0 dentro de 'setup()'. Se incrementa en 1 cada vez que finaliza la ejecución del código en 'draw()'.

