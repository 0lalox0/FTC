# TP 10 Logica de predicados

Ejercicio 1.  Expresar en un lenguaje de predicados de primer orden las siguientes afirmaciones: 
I.  Algunas aves no vuelan 
V(x) = x vuela
A(x) = x es una Ave
(E;(x)) (A(x) y -V(X))

II.  No todas las aves vuelan
-(A;)(A(x) -> V(X))

Ejercicio 2. Expresar en un lenguaje de predicados de primer orden el conocimiento asociado a 
las siguientes situaciones: 

I.  Los usuarios que contribuyen en proyectos open source son colaborativos.
U(x) x es un usuario
C(x,y) x contribuye a proyectos de tipo y
O(y) y es open source
Cola(x) x es colaborativo

A;(x) (U(x) y C(x,y) y O(y)) -> Cola(x) ???
II.  Ningún sistema que tenga bugs críticos puede ser entregado ni desplegado en 
producción. 
S(x) x es un sistema //Hace falta ???
B(x, y) x tiene bugs de tipo y(hace falta y o solo pongo tiene bugs criticos)
Cri(y) y es critico
E(x,p)x no puede ser entregado en p
D(x,p)x no puede ser deployado en p
Prod(p) p es producion
-E;(x) (S(x) y B(x,y) y Cri(y) y -(E(x,p) o D(x,p))) ???
o
A;(x) (S(x) y B(x,y) y Cri(y)) -> (E(x,p) o D(x,p)
III.  Ningún modelo de IA que se entrena con datos erróneos es preciso. 
M(x) x es un modelo de ia
E(x)x se entrea con datos Erroneos
P(x) x es preciso
-E;(x) (M(x)  y  E(x)) y P(x)
Porque no 
-E;(x) (M(x)  y  E(x)) -> P(x) ???
IV.  Todo estudiante que cursa FTC (Fundamentos de Teoría de la computación) y sube sus 
ejercicios a IDEAS aprueba la práctica. 
E(x) x es un estudiante
C(x,y) x cursa la maateria y
FTC(y) y es ftc ???
Su(x) sube sus ejercicos a ideas
Ap(x) x aprueba la practica
A(x) ((E(x) y C(x,ftc) y Su(x)) -> ap(x))


V.  Todos los alumnos de FTC, cuyo documento es par y han aprobado el parcial con nota mayor a 7 están inscriptos en la mesa de finales de agosto. 

AFTC(x) x es alumno de ftc
doc(x) x tiene documento par
apro(x) x aprobo el parcial con mas de 7
inscrip(x) x esta inscripto en la mesa de finales

A;(x){(AFTC(x) y doc(x) y apro(x)) -> inscrip(x)}
VI.  Todos los estudiantes que cursan  FTC y subieron correctamente el código al repositorio 
están habilitados para correr las pruebas automáticas del sistema. 
AFTC(x) x es alumno de ftc
Repo(x) x subio correctamente el codigo al repo
Hab(x) esta habilitado para correr pruebas automaticas

A;(x) (AFTC(x) y Repo(x)) -> Hab(x)


VII.  Algunos modelos de inteligencia artificial entrenados por alumnos de  FTC lograron superar el umbral de precisión del 90%

IA(x) x es un modelo de ia
Ent(x,y) x ha sido entrenado por y
Log(x) x logro superar el umbral de presicion del 90% ???
E;(x) (IA(x) y Ent(x,Alumnos FTC) y Log(x))


Ejercicio 3.  Escribir las siguientes proposiciones usando un lenguaje de predicados de primer 
orden: 
I.  El cero es el menor natural. 
Mnatu(x) x es el menor natural
Mnatu(x)
Chargpt:
<=(x,y) x es menor o igual a y
N(x) x es natural
A;(x) (N(x) -> <=(x,0)) 

Ahora q pienso tmb se cumple:

-E;(x) (N(x) y -<=(x,0))

II.  El conjunto vacío está incluido en cualquier conjunto. 
Conju(x) x es un conjunto
C(x,y) x esta incluido en y
A;(x)(Conju(x) -> C({},x))
o (devuelta)
-E(x)(Conju(x) y -C({},x))
III.  Si se prueba una propiedad para el cero y luego se prueba que esa misma propiedad vale para el número n+1 si vale para n, entonces se ha probado que la propiedad vale para cualquier natural.


P(x,y) la propiedad x se prueba para el num y
N(x) x es natural

x es la propiedad
(P(x,0) y P(x,n+1) y P(x,n)) -> (A;(y) N(y) -> P(x,y))
chatgpt:
(P(x,0) y (A;(n) (N(x) -> P(x,n) -> P(x,n+)))) -> (A;(y) N(y) -> P(x,y))


IV.  Si hay un número natural que cumple una cierta propiedad, entonces hay un mínimo natural que cumple esa propiedad.

P(x,y) el numero x cumple con la propiedad y
Nat(x) x es un numero natural
MinNat(x) x es un minimo natural

P(x,y) y Nat(x) -> [E;(n) (MinNat(n) y P(n,y))]

o

[E;(x) P(x,y) y Nat(x)] -> [E;(n) (MinNat(n) y P(n,y))]

Chatgpt:
(∃x(Nat(x)∧P(x)))→∃m(Nat(m)∧P(m)∧∀y(Nat(y)∧P(y)→m≤y))
