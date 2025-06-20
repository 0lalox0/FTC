### Ejercicio 1
A: El Unicornio es mitico
B: Es inmortal
C: Es un Mamifero
D: Tiene un cuerno
E: Es Magico

Simbolizar en el Calculo de Enunciados
y Responder

(A -> B)
(!A -> (!B & C))
(A | C) -> D
D -> E
I.  El unicornio es mıtico?. 
No, no hay pruebas suficiente para ver si el unicornio es mitico.
II.  El unicornio no es mítico?. 

III.  El unicornio es mágico?.

Sabiendo ahora que el unicornio es inmortal, responder: 
 
IV.  El unicornio no es mágico?. Fundamentar.

5)
    i) ((-(A → B) )→ C )  
        No es tautologia ni contradiccion ya que depende de C y esta podria valer o V o F y cambiaria el resultado de la formula.
    ii) (C → ((¬A ) ∨ B))
        Es tautologia, ya que aunque no se sabe el valor de C, sabemos que )-a V B) siempre sera verdadero, por lo tanto la formula siempre sera verdaera.
    iii) ((¬A ) → B )
        No tenemos informacion suficiente para saber si es una tautologia o si es una contradiccion.
6)
    i) ¿“(p → q)” es lógicamente equivalente a “(p ∨ ¬q)” ?
        Para saber esto, debemos comprobar que 
        (p -> q) <-> (p V -q) es una tautologia, si lo es son logicamente equivalentes, sino no.

|  1  |  p  |  q  | p -> q | -q  | p1 v -q1 | (p -> q) <-> (p v -q) |
| :-: | :-: | :-: | :----: | :-: | :------: | :-------------------: |
|  3  |  V  |  V  |   V    |  F  |    V     |           V           |
|  4  |  V  |  F  |   F    |  v  |    V     |           F           |
|  5  |     |     |        |     |          |                       |
|     |     |     |        |     |          |                       |

Es falso no es logicamente equivalente ya que (p -> q) <-> (p v -q) no es una tautologia

Ejercicio 7. Sea # el operador binario definido como p#q = (p ∧ ¬q) ∨ (¬p ∧ q). 
 
I.  Probar que # es asociativo, es decir, x#(y#z) es lógicamente equivalente a (x#y)#z.  

Para comprobar esto comprobamos si x#(y#z) <-> (x#y)#z es una tautologia
| x   | y   | z   | z#y | x#y | x#(y#z) | (x#y)#z | x#(y#z) <-> (x#y)#z |     |
| :-- | --- | --- | --- | --- | ------- | ------- | ------------------- | --- |
| V   | V   | V   |     |     |         |         |                     |     |


II.  Probar que # es conmutativo, es decir, y#z es lógicamente equivalente a z#y. 

12)  Encontrar una formula satisfacible y no tautologia, metodo de contra ejemplo.
13)Conrea ejemplo o absurdo?
