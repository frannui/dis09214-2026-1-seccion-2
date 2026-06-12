# sesión 10 - 12/06
DISEÑO RESPONSIVO
-
(windowResised)

function windowResised 
resizeCanvas (windowWidth, windowHeight)

usar valores relativos 
usar fraciones y proporciones para organizar mis elementos del sketch 
(width / 2, height / 2) división 
(width . 0.25) multiplicación

si solamente utilizo estos comandos se va a deformar el dibujo 

estos e usa para arreglar ese problema 
incluir factor de referencia 
let referencia 
referencia=min(width, height) 

para crear figuras que no se deformen se deben crear variables que determinen una medida especifica que se utilizara de referencia y luego se incorporan a los valores relativos 
