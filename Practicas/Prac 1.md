Ejercicio 1. Responder breve y claramente los siguientes incisos: 
1. ¿En qué se diferencia un problema de búsqueda de un problema de decisión? 
		Los problemas de búsqueda necesitan de la maquina devolver una solución a un probelma, en cambio en la de decision solo tiene que devolver si Acepta o Rechaza la entrada
2. ¿Por qué en el caso de los problemas de decisión, podemos referirnos indistintamente a 
problemas y lenguajes?
	Si,
3. El problema de satisfactibilidad de las fórmulas booleanas, en su forma de decisión, es: “Dada 
una fórmula φ, ¿existe una asignación A de valores de verdad que la hace verdadera?” 
Enunciar el problema de búsqueda asociado. 
		
4. Otra visión de MT es la que genera un lenguaje (visión generadora). En el caso del problema 
del inciso anterior, ¿qué lenguaje generaría la MT de visión generadora que resuelve el 
problema? 
		
5. ¿Qué postula la Tesis de Church-Turing? 
		Todo dispositivo computacional físicamente realizable puede ser simulado por una MT.
6. ¿Cuándo dos MT son equivalentes? ¿Y cuándo dos modelos de MT son equivalentes? 
		• Dos MT son equivalentes si aceptan el mismo lenguaje (es decir, si resuelven el mismo problema). 
		• Dos modelos de MT son equivalentes si dada una MT de un modelo existe una MT equivalente del otro.


Ejercicio 2. Dado el alfabeto Ʃ = {0, 1}: 
Obtener el conjunto Ʃ* y el lenguaje incluido en Ʃ* con cadenas de a lo sumo 2 símbolos.  
Sea el lenguaje L = {0n1n | n ≥ 0}. Obtener los lenguajes Ʃ*
 
⋂ L, Ʃ*
 
⋃ L y LC respecto de Ʃ*.  
**En el repositorio de FrancoCirielli**
Ejercicio 3. En clase se mostró una MT no determinística (MTN) que acepta las cadenas de la 
forma han o hbn, con n ≥ 0. Construir (describir la función de transición) una MT determinística 
(MTD) equivalente.
**En el repositorio de FrancoCirielli**


Ejercicio 4. Describir la idea general de una MT con varias cintas que acepte, de la manera más eficiente posible (menor cantidad de pasos), el lenguaje L = {a'n b'n c'n | n ≥ 0}.



Ejercicio 5. Explicar cómo una MT sin el movimiento S (el no movimiento) puede simular (ejecutar) otra que sí lo tiene.
Que en el estado qR o qA osea rechazado o aceptado, solo se mueva de IZQ a Derecha infinitamente hasta q alguien la frene?




Ejercicio 7. Construir una MT que calcule la resta de dos números. Ayuda: se puede considerar la idea de solución propuesta en clase.

IDEA: Idea general: tachar el primer 1 antes del 0, luego el primer 1 después del 0, luego el segundo 1 antes del 0, luego el segundo 1 después del 0, y así hasta tachar al final el 0.


Definición de la MT M = (Q, Γ, δ, q0, qA, qR):
Estados Q = {q0, qa, qb, qL, qH, qA, qR} 
q0 : estado inicial
qa : M busca a 0
qb : M busca un 1 dsp del cero 
qL : M vuelve a buscar a
qH: M vuelve a buscar 0
qH : no hay mas 1
Alfabeto Γ = {a,0,1,B}
Función de transición 


1.δ(q0, 1) =  (qa,a,R)
2.δ(qa, 1) = (qa,1,R)
3.δ(qa, 0) = (qb,0,R)
4.δ(qb, 1) = (qh,a,L)
5.δ(qh, a) = (qh,a,L)
6.δ(qh, 0) =  (ql,0,L)
7.δ(ql, 1) =(ql,1,L)
8.δ(ql, a) =(q0,a,R)
9.δ(q0, 0) =(qA,0,S)
10.δ(qb, a) =(qb,a,R)
11.δ(qb, B) =(qA,B,S)

¿Hace falta limpear las a?
Como se podria haber echo?
