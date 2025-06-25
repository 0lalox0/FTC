### Practica 11 Logica de predicados Semantica

Ejercicio 1 Señalar las ocurrencias libres o ligadas de x1, x2 , x3 en la siguiente fbf escrita en un lenguaje de primer orden donde C = {c}, F = {f,g} y P = {A} con f de aridad 1; g de aridad 2,A de aridad 2 determinar Cual es una fbf abierta y cual es cerrada.

I. (A;x1)((E;X2) A(x1,f(x2,x3))-> (A;x3)A(g(c),x1) o A(x1,x3))
II. (∀𝑥1)((∃𝑥2)𝐴(𝑥1,𝑓(𝑥2,𝑥3))) → (∀𝑥3)𝐴(𝑔(𝑐), 𝑥1) ∨ 𝐴(𝑥1,𝑥3)

 Los cuantificadores tienen un alcance o  scoupe, o radio de acción determinado. 
Por ejemplo, en la fórmula bien formada: 
A;x P1/1(x) -> P1/2(x)
 las dos ocurrencias del símbolo de variable x suceden dentro del alcance del cuantificador 
 Mientras que en la fórmula bien formada: 

 el  alcanza sólo a la primera ocurrencia de x. Diremos en el primer caso que x está ligada, y en el segundo que 
la primera x está ligada y la otra está libre (por lo que podría sustituirse por cualquier otro símbolo de variable). 
Una fbf es abierta si contiene algún símbolo de variable libre, y cerrada si todos los símbolos de variables están 
ligados.

Por lo tanto:
I. (A;x1)((E;X2) A(x1,f(x2,x3))-> (A;x3)A(g(c),x1) o A(x1,x3))
