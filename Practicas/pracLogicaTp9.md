### TP9 FTC
### Sistema formal L: axiomas y reglas de inferencia

Ejercicio 1. Dada la siguiente demostración sintáctica válida en  : 𝐿
 
1.   (((¬𝑝)→(¬(𝑞→𝑟)))→((𝑞→𝑟)→𝑝))
2.    ((-p)->(-(q->r))
3.  ((q->r)->p)
 
a)  Identificar  el  conjunto  R  con  menor  cantidad  de  fórmulas  bien  formadas  (fbfs) y la 
fórmula  A  tal  que Γ├L 𝐴 .  Indicar,  si  es  posible,  que  axioma,  hipótesis  o  regla  de 
inferencia fue aplicado en cada paso de la demostración. 
1. Axioma L3
2. Hipotesis
3. MP de 1 y 2
R={((-p)->(-(q->r))}
A = ((q->r)->p)
b)  ¿Es A  un teorema de  L? Justificar.
para comprobar si A es un teroma de L hay que ver si se cumple
() ├𝐿 𝐴, es decir si con un conjunto vacio se deduce con L A.
() |-L ((q->r)->p)
por metateorema de la deduccion podemos decir que si probamos esto eso se cumple.
(,(q->r)) |-L p

c)  ¿Es A  tautología? Justificar.
A no es una tautologia.
si q = V, r = V, p = f, el valor el falso de A

Chat GPT confirma ajdsja