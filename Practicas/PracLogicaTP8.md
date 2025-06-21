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

| x   | y   | z   | y#z | x#y | x#(y#z) | (x#y)#z | x#(y#z) <-> (x#y)#z |
| --- | --- | --- | --- | --- | ------- | ------- | :-----------------: |
| V   | V   | V   | F   | F   | V       | V       |          V          |
| V   | V   | F   | V   | F   | F       | F       |          V          |
| V   | F   | V   | V   | V   | F       | F       |          V          |
| V   | F   | F   | F   | V   | V       | V       |          V          |
| F   | V   | V   | F   | V   | V       | V       |          V          |
| F   | V   | F   | V   | V   | F       | F       |          V          |
| F   | F   | V   | V   | F   | F       | F       |          V          |
| F   | F   | F   | F   | F   | F       | F       |          V          |

# Es asociativo


II.  Probar que # es conmutativo, es decir, y#z es lógicamente equivalente a z#y.

| y | z | y#z | z#y | y#z <-> z#y |
| - | - | --- | --- | ----------- |
| V | V | F   | F   | V           |
| V | F | V   | V   | V           |
| F | V | V   | V   | V           |
| F | F | F   | F   | V           |

# Es conmutativo

Ejercicio  8.  ¿Es  cierto  que en el Cálculo de Enunciados pueden escribirse dos fbfs que tengan  diferentes  letras  de  proposición  y  aun  así  ambas  fbfs  sean  lógicamente equivalentes?. En caso de responder positivamente, dar un ejemplo y justificar. En caso de responder negativamente, justificar.

Si es posible, simplemente hay q elegir dos tautologias.

por ejemplo p V -p <-> q V -q es una tautogia

Ejercicio 9. Determinar cuáles de las siguientes fbfs son lógicamente implicadas por la fbf 
(A ∧ B). Fundamentar. 
 
I.  A 
II.  A ↔ B 
III.  ¬B → ¬A 
IV.  A → B 

Para ver si una fbf es logicamente implicada tiene que ser una tautologia lo siguiente

fbf -> fbf

(A  ∧ B) -> A

| A   | B   | A ∧ B | (A ∧ B) -> A |     |
| :-- | --- | ----- | ------------ | --- |
| V   | V   | V     | V            |     |
| V   | F   | F     | V            |     |
| F   | V   | F     | V            |     |
| F   | F   | F     | V |     |

Como es una tautologia a ∧ B logicamente implica a A

Ejercicio 10. Dada la siguiente tabla de verdad, encontrar tres fbfs para cada una que las 
tenga por tablas de verdad:  
 
I.  una fbf (sin restricciones de conectivos).  
-(p <-> q)
II.  una fbf en FNC (forma normal conjuntiva) 
ORs juntados por ANDs
(-p o -q) y (p o q)
III.  una fbf en FND (forma normal disyuntiva)
ANDs juntados por ORs
(p∧¬q)∨(¬p∧q)

| p   | q   | ?   |
| :-- | --- | --- |
| V   | V   | F   |
| V   | F   | V   |
| F   | V   | V   |
| F   | F   | F   |

Ejercicio  11.  Explicar  porque  el  siguiente  conjunto  no  es  un  conjunto  adecuado  de conectivas {∧, ∨}.

Un conjunto adecuado de conectivas es un conjunto tal que toda funcion de verdad puede representarse por medio dde una forma enunciativa que contenga solamente conectivas del conjuto

GPT:
No es adecuado ya que
Porque no incluye la negación (¬).

Sin ¬ no podemos representar funciones que impliquen negar una variable.

Por ejemplo, no podemos expresar la función ¬p usando solo ∧ y ∨.

Más formalmente:

Si tenemos solo ∧ y ∨, las únicas funciones que podemos formar son monótonas: es decir, funciones que si aumentamos el valor de alguna variable (de F a V), no va a disminuir el valor de la función.

Pero funciones como ¬p o el XOR (que vimos antes) no son monótonas.


12)  ¿Es cierto que si una fbf A es satisfactible entonces A es una tautología”
     profe : Encontrar una formula satisfacible y no tautologia, metodo de contra ejemplo.
    Falso ya que existen fbfs que son satisfacibles pero no tautologias.
    Por ejemplo la fbf A = p V q Es satisfacible ya que si p o q son verdaderas va a ser verdadera asique es satisfacible pero si p y q son falsas es falsa asique no es una tautologia.(metodo de contra ejemplo)
13)Contra ejemplo o absurdo?
Ejercicio 13. Sea A una fbf donde aparecen solo los conectivos ∧, ∨, ¬ . Sea A* la fbf que se  obtiene  a  partir  de  A  reemplazando  cada  ∧  por  ∨  y  cada  ∨  por  ∧.  Si  A  es  una tautología, A* ¿también lo es? Justificar.

(q v -q) v (q y q)  -> tautologia

(p y -q) y (q o q) -> contradiccion no tautologia

Ejercicio  14.  Demostrar  utilizando  la  técnica  del  absurdo  que  dadas  A  y  B  fbfs cualesquiera, siempre ocurre que si A y A → B son tautologías entonces B también lo es.  
Ayuda: ver prop. 1.9, Hamilton

Para usar el Absurdo  veamos el caso contrario.
Si A es una tautologia -> siempre da V
y A -> B es una tautologia siempre da V
suponemos que B no es una tautologia, es decir que podria dar F
en ese caso como A siempre es V y b puede dar F deducimos que
V -> F = V lo cual es mentira ya que seria falso, haciedno que A -> B no sea una tautologia lo cual contradice la supocicion inicial.

Ejercicio 15. Demostrar utilizando la técnica del **absurdo** que (p∧¬p)→q es una tautología.

(p∧¬p)→q es una tautologia

Suponemos que no es una tautologia para que una -> de falso solo existe una opcion y es que sea : V -> F y p y -p siempre da  Falso, por lo tanto nunca se comple la condicion.

Ejercicio 16.  Sea A una fbf donde aparecen solo los conectivos ∧, ¬. Sea A* la fbf que se obtiene  a  partir  de  A  reemplazando  cada  ∧  por  ∨  y  cada  letra  de  proposición  por  su negación  (o  sea,  cada  p  por  ¬p,  cada  q  por  ¬q,  etc.).  Probar,  utilizando  la  técnica  de inducción que A* es lógicamente equivalente a ¬A. 
 
Ayuda: ver prop 1.15, Hamilton 

Ejercicio  17.  Demostrar  utilizando  la  técnica  de  inducción  que  cualquier  fórmula  bien 
formada A que contenga sólo los conectivos {∨, ∧} puede tomar el valor F. 
 
Ayuda: ver ejercicio resuelto en clase teórica

Para probar esto vamos a tomar una valuacion que haga que A sea falsa.
Sea v una valuacion que hace q todas las letras sean falsa osea v(pi) = F para todo i. Con esa valuacion la fbf A tmb va a tomar el valor F

N = cantidad de conectivos de la fbf

Caso base n = 0
No hay conectivos A es atomica A = p
v(p) = F por lo tanto v(A) = F
Se cumple

Hipotesis Inductiva: Asumimos que para toda fbf A q contiene solo V y Y con N o menos conectivos v(A) = F

Caso N+1
Usando la H.I. tenemos que poder probar que v(A)=F, para una fórmula A que tiene N+1 conectivos. 
A ppuede tener dos formatos con un conectivo:
Caso 1: A es (B ∨ C) 
Caso 2: A es (B ∧ C)
Vemos que tanto B como C tienen N o menos conectivos , por lo tanto para ellas vale la 
H.I., es decir v(B)=F y v(C)=F .
 Entonces, por la definición de la semántica del ∨ y del ∧, tanto en el caso 1 como en el caso 2, v(A)=F.
 Con esto hemos demostrado que v(A)=F, para cualquier fbf (que contenga sólo ∨ y ∧ )
 Hemos demostrado que A puede tomar el valor Falso y por lo tanto 
A no es una Tautología.