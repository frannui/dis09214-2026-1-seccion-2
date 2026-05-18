# sesión 05 - 10/04

## TRANSFORMACIONES & CONDICIONALES  
### Transformaciones  
#### Ángulos  
angleMode(); por defecto p5.js usa radiantes para medir los ángulos  
angleMode(RADIANS);  
Para cambiar a grados se usa esto en el function SETUP  
angleMode(DEGREES);  
(hay que pensar como se mueven las agujas del reloj; TWO_PI 360º, PI 180º, HALF_PI 90º, QUARTER_PI 45º)

#### Rotación  
rotate(); sirve para rotar elementos, SIEMPRE ROTA ALREDEDOR DEL PUNTO DE ORIGEN (0,0). Se recomienda usar con translate(); y en algunos casos con rectMode(CENTER);  
SINTAXIS: rotate(valor radianes o en grados);  
EJEMPLO: rotate(20);

#### Trasladar  
translate(); sirve para trasladar el PUNTO DE ORIGEN (0,0) a otra cordenada de mi canvas.  
SINTAXIS: translate(x,y);  
EJEMPLO: transalte(200,200);

#### Guardar y Restaurar
push();  
pop();  
Funciones que trabajan juntas como un "sistema de memoria temporal" para el estilo y las transformaciones del lienzo.  
SINTAXIS: push();  
SINTAXIS: pop();

#### Escala  
scale(); la función scale() ajusta la escala del sistema de coordenadas actual por el factor específico.  
SINTAXIS: scale(x,y);  
EJEMPLO: scale(2,2);

### CONDICIONALES  
* LÓGICA CONDICIONAL
* EXPRESIÓN BOOLEANA: una expresión booleana es cualquier enunciado, dato o instrucción que, al ser evaluado, solo puede arrojar uno de dos valores posibles: verdadero (True) o falso (False).
TRUE OR FALSE -> ejemplo: si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar.
Expresión Booleana para construir este tipo de expresiones se utilizan 3 tipos de elementos: OPERADORES
- Operados (o valores): son los datos básicos que se evalúan. Pueden ser:
* Variables: (como x,y o mouseX, mouseY, etc)
* Constantes o Literales: Valores fijos como 5, "Hola" o los mismos valores booleanas True of False.

- Operadores de Comparación: permiten contrastar dos valores
* == (igual a )
* != (diferente de)
* > o < (mayor o menor que)
* >= 0 <= (Mayor o igual / menos o igual que)

- Operadores Lógicos: sirven para combinar varias expresiones
* AND (&&): es verdadero solo si ambas partes son verdaderas
* OR (||): es verdadero si al menos una de las partes es verdadera
* NOT (!): invierte el valor (si era verdadero, pasa a ser falso)

Menor que < y mayor que >  
Al comparar números, el operador devuelve un booleano basado en la comparación matemática.  
Menor o igual que: < = y mayor o igual que: > =  
Similar a < y >, pero también devuelve true cuando ambos valores son iguales

### SENTENCIA CONDICIONAL  
#### if - else if - else  
La sentencia if es una estructura especial que existe en casi todos los lenguajes de programación; toma una condición -expresada como un booleano- y ejecuta una pieza de código contenida dentro de las llaves { }  
if (condición){ejecuta este código si es true}  
ejemplo: si algún estudiante apaga por completo las luces de la sala, la profesora debe bailar. 

#### if - else if - else  
La sentencia if puede completarse con la sentencia else if, que añade condiciones de prueba complementarias a la original, y con la sentencia else, que implica tofos los casos que no cumplen con la condición original. (dato: puedes añadir tantas sentencias else if como desees)  
If (condición){ejecuta este código si es true}  
else if (condición 2){ejecuta este código si es true}  
else{ejecuta este código si ambas condiciones son falsas}  
ejemplo: si algúne estudiante apaga por completo las luces de la sala, la profesora debe bailar. Si no se cumple lo anterior SI la ayudante se levanta de su silla, la profesora debe cantar. Y SI NO SE CUMPLEN NINGUNA DE LAS ANTERIORES, los estudiantes guardan silencio.

if(estudainteApagaLuces){  
profesora.nailar();  
}  
else if (ayudanteSeLevanta){  
profesora.cantar();  
}  
else{  
estudiantes.guardarSilencio();  
}
