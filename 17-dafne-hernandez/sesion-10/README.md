# sesión 10 - 12/06  

# DISEÑO RESPONSIVO (windowResized)  

**Cómo se crea un sketch que se adapte a diferentes tamaños de pantalla**  

**Paso 01**  
CREAR UN CANVAS CON DIMENSIONES DINÁMICAS   
Para esto usaremos las variables integradas en el sistema: ```(windowWidth ,  windowHeight)``` estas variables leen constantemente el ancho y alto disponibles de la ventana del navegador.    

**Paso 02**  
CREAR UN EVENTO ```windowResized()```  
Si el usuario estira o encoge la ventana del navegador, el lienzo se adaptará al tamaño de la ventana en tiempo real.    

**Paso 03**  
USAR VALORES RELATIVOS  
Ahora p5.js actualiza estas variables width y height automáticamente con el tamaño actual del lienzo.   
Se usarán fracciones y proporciones:  
Ej: Ej: Centro del lienzo:  ```(width / 2 , height / 2)```  

**Paso 04**  
INCLUIR UN FACTOR DE REFERENCIA   
```referencia = min(width, height)```  
Creamos una variable global (referencia) y la asignamos para que calcule el mínimo.    
Observa el ancho y el alto de la ventana, los compara, y se queda solo con el que sea más pequeño en ese momento.    

**Paso 05**  
USAR TRANSLATE - PUSH Y POP  (En caso de proyectos complejos)  
En lugar de hacer matemáticas complejas en cada rect() o ellipse(), usamos translate() para moverlos.  
Y siempre utilizando push() y pop() para cada figura o elemento.   

## Load pixels   
Toma todos los píxeles de la pantalla (o de una imagen) y los carga en la memoria de acceso rápido (RAM). Se comunica directamente con la tarjeta gráfica píxel por píxel en tiempo real.  


![Gato](https://i.pinimg.com/736x/ea/13/66/ea13661381a4f501cccfd71a0fd3166b.jpg)

