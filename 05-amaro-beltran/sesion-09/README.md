# sesión 08 - 29/05  

# ARRAYS & CLASS  

## Repaso diagrama de flujo  
### Algoritmo  
Es una secuencia instrucciones paso a paso, lógicas, definidas, ordenadas y finitas que permiten solucionar un problema o realizar una tarea específica.  
**Sus caracteristicas fundamentales son:**  
* precision: Cada paso debe estar claro (sin ambigüedades).
* Orden: Los pasos llevan una secuencia lógica.
* Finitud: Tiene que terminar en algún momento, no puede ser infinito.
* Definición: Si sigues el mismo algoritmo dos veces con los mismos datos, deberías obtener siempre el mismo resultado.

  ### Estructura
  **Input (Entrada):** La información o los ingredientes que necesitas para empezar.
  **Proceso:** Los pasos lógicos que transforman esa entrada. (algoritmo)
  **Output (Salida):** El resultado final o la solución al problema.

  ### Diagrama de flujo
  Representación gráfica de un algoritmo o de los pasos de un proceso. En programación, se utiliza como una herramienta de planificación para visualizar la lógica de un programa antes de escribir una sola línea de código.
Se usa simbología especifica, para que cualquier programador pueda entenderlo.

## Arrays (listas)  
Un contenedor con compartimentos numerados donde puedes guardar múltiples datos bajo un mismo nombre. Es una lista que mantiene varios datos ordenados. Los arreglos (Arrays) son muy útiles para almacenar datos relacionados y pueden contener datos de cualquier tipo.  

```let nombreArray =[e0 , e1 , e2 , e3 , e4 , e5] ;```  
ejemplo: ```let Colores = [ “red”, “orange”, “yellow”, “green”, “blue”] ;```  
**¿Como usar los elementos de array?**  
Para llamar a alguno de los valores de mi Array vamos a usar: nombreArray [ numero elemento ]  

## Class (molde)  
Una clase (class) es un molde o plantilla abstracta que define la estructura, los datos (propiedades) y los comportamientos (métodos) que tendrá un tipo de objeto específico.  
ej: Imagínala como el plano de diseño de una casa o un cortador de galletas: no es el objeto real en sí, sino las instrucciones empaquetadas para fabricar infinitas copias independientes basadas en ese mismo modelo utilizando la palabra clave **new**  

La sintaxis básica de una clase en JavaScript se estructura siempre en tres partes dentro de un bloque de llaves:
1. La palabra clave class + nombre que le quiera dar.
2. El método constructor (donde se definen las propiedades del objeto usando .this)
3. Las funciones personalizadas que definen lo que hace el objeto.

## Class+Array  
