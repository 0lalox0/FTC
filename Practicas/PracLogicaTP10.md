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
O(y) open source
Cola(x) x es colaborativo

(U(x) y C(x,y) y O(y)) -> Cola(x) ????
II.  Ningún sistema que tenga bugs críticos puede ser entregado ni desplegado en 
producción. 
S(x) x es un sistema //Hace falta?
B(x, y) x tiene bugs de tipo y(hace falta y o solo pongo tiene bugs criticos)
Cri(y) y es critico
E(x,p)x no puede ser entregado en p
D(x,p)x no puede ser deployado en p
Prod(p) p es producion
-E;(x) (S(x) y B(x,y) y Cri(y) -> (E(x,p) o D(x,p))) ????
III.  Ningún modelo de IA que se entrena con datos erróneos es preciso. 
IV.  Todo estudiante que cursa FTC (Fundamentos de Teoría de la computación) y sube sus 
ejercicios a IDEAS aprueba la práctica. 
V.  Todos los alumnos de FTC, cuyo documento es par y han aprobado el parcial con nota 
mayor a 7 están inscriptos en la mesa de finales de agosto. 
VI.  Todos los estudiantes que cursan  FTC y subieron correctamente el código al repositorio 
están habilitados para correr las pruebas automáticas del sistema. 
VII.  Algunos modelos de inteligencia artificial entrenados por alumnos de  FTC lograron 
superar el umbral de precisión del 90%