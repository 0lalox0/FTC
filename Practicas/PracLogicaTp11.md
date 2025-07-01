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
I. (A;x1)((E;X2)A(x1,f(x2,x3))-> (A;x3)A(g(c),x1) o A(x1,x3))                |                           |       |
x1 Esta ligada, en todo la fbf, para A;(x1) del principio

I. (A;x1)((E;X2)A(x1,f(x2,x3))-> (A;x3)A(g(c),x1) o A(x1,x3))                    |
X2 esta ligada en todos lados

I. (A;x1)((E;X2)A(x1,f(x2,x3))-> (A;x3)A(g(c),x1) o A(x1,x3))                      | 
 |         
X3 esta Libre en todos lados
Como x3 esta libre la fbf es abierta

Ligadas:
                 |    |
II (∀𝑥1)((∃𝑥2)𝐴(𝑥1,𝑓(𝑥2,𝑥3))) → (∀𝑥3)𝐴(𝑔(𝑐),𝑥1) ∨ 𝐴(𝑥1,𝑥3)
Lires                    |                   |       |  |
II (∀𝑥1)((∃𝑥2)𝐴(𝑥1,𝑓(𝑥2,𝑥3))) → (∀𝑥3)𝐴(𝑔(𝑐),𝑥1) ∨ 𝐴(𝑥1,𝑥3)

Es abierta              ??????????


Ejercicio 2 Sea A una fbf que no contiene cuantificadores (es decir, abierta) escrita en algún lenguaje de primer orden. Sea I una interpretación para tal lenguaje. ¿Es posible decidir acerca del 𝐼
valor de verdad de A en I? Fundamentar. ???? Ni idea

Pero creo q si se puede decidir hacerca dle valor de verdad


Ejercicio 3. Analizar si son o no lógicamente equivalentes los siguientes pares de fbfs (usar noción 
de i-equivalencia o contraejemplos según corresponda)

| Nº  | Fórmula A                     | Fórmula B                     |
|-----|-------------------------------|-------------------------------|
| I   | (∀x)P(x)                      | (∃x)P(x)                      |
| II  | (∃x)(∃y)Q(x, y)               | (∃y)(∃x)Q(x, y)               |
| III | (∃x)(∀y)R(x, y)               | (∀y)(∃x)R(x, y)               |
| IV  | (∃x)(S(x) ∧ T(x))             | (∃x)S(x) ∧ (∃x)T(x)           |
| V   | (∃x)(S(x) ∨ T(x))             | (∃x)S(x) ∨ (∃x)T(x)           |
| VI  | (∀x)(S(x) ∨ T(x))             | (∀x)S(x) ∨ (∀x)T(x)           |

I. No son equivalentes porque en la formula B con que un solo x cumpla con P(x) vale pero en la formula A tienen que todos los x cumplir con P(x)

### ❌ Contraejemplo

Interpretación:

- Dominio \( D = \{1, 2, 3\} \)
- Definimos \( P^I = \{1\} \), es decir, **solo 1 cumple \( P(x) \)**

Evaluamos:

- \( \forall x \; P(x) \): ❌ **Falsa** (2 y 3 no lo cumplen)
- \( \exists x \; P(x) \): ✅ **Verdadera** (al menos 1 lo cumple)


| II  | (∃x)(∃y)Q(x, y)               | (∃y)(∃x)Q(x, y)               |
Si son logicamente equivalentes 

Chatgpt:
### ✅ Noción de i-equivalencia

Dos fórmulas son i-equivalentes si **en toda interpretación** y para **toda valuación**, tienen el **mismo valor de verdad**.

---

### 🧪 Evaluación:

Tomamos una interpretación:

- Dominio: D = {1, 2}  
- Q^I = { (1,1), (1,2) }

Evaluamos ambas fórmulas:

- (∃x)(∃y)Q(x, y): ✅ Verdadera (por ejemplo, x=1, y=2)  
- (∃y)(∃x)Q(x, y): ✅ Verdadera (y=2, x=1)

Probamos otras interpretaciones (Q^I vacío, Q^I con un solo par, etc.)  
y **en todos los casos** ambas fórmulas resultan con **el mismo valor de verdad**.

---

### ✅ Conclusión:

Sí, son **i-equivalentes**, porque en **toda interpretación y valuación** tienen el **mismo valor de verdad**.

III.   ∃(x)(∀𝑦)𝑅(𝑥,𝑦)   (∀𝑦)∃(x)𝑅(𝑥,𝑦)

No, no son logicamente equivalentes ya que dicen cosas distintas:
1° Existe(por lo menos) un x q para todo y R(x,y) se cumple
2° Para todo Y existe un x q R(x,y) se cumple



### 🧪 Evaluación:

Tomamos una interpretación:

- Dominio: D = {1, 2}  
- R^I = { (1,1), (2,2) }

Evaluamos ambas fórmulas:

- ∃(x)(∀𝑦)𝑅(𝑥,𝑦): ❌ Falso (por ejemplo, x=1, y=2)  
- ∃(x)(∀𝑦)𝑅(𝑥,𝑦): ✅ Verdadera (por ejemplo, x=1, y=1)   No cumple
- (∀𝑦)∃(x)𝑅(𝑥,𝑦): ✅ Verdadera (y=1, x=1)
- (∀𝑦)∃(x)𝑅(𝑥,𝑦): ✅ Verdadera (y=2, x=2)
  


| IV  | (∃x)(S(x) ∧ T(x))             | (∃x)S(x) ∧ (∃x)T(x)            |

Falso. Las fórmulas no son lógicamente equivalentes, ya que existe al menos una interpretación donde tienen distinto valor de verdad.

**Contraejemplo:**

- Dominio: D = ℕ (números naturales)  
- Interpretación:  
  - S(x): “x es par”  
  - T(x): “x es impar”

Evaluación:

- (∃x)(S(x) ∧ T(x)) → ❌ Falsa  
  No existe ningún número que sea par e impar al mismo tiempo.

- (∃x)S(x) ∧ (∃x)T(x) → ✅ Verdadera  
  Porque existen números pares (por ejemplo, 2) y existen números impares (por ejemplo, 3).

**Conclusión:**  
No son lógicamente equivalentes, ya que existe una interpretación donde una es verdadera y la otra falsa.


| V   | (∃x)(S(x) ∨ T(x))             | (∃x)S(x) ∨ (∃x)T(x)           |
Si, si son equivalentes ya que significan lo mismo:
o existe algun x q cumple S(x)
o existe algun x q cumple T(x)

Chatgpt(Nocion de i equivalencia):
✅ **Son i-equivalentes.**

Dos fórmulas son i-equivalentes si **en toda interpretación** y para **toda valuación**,  tienen el mismo valor de verdad.

---

### 🧪 Interpretación 1

- Dominio: D = {1}
- S^I = {1}
- T^I = ∅

- (∃x)(S(x) ∨ T(x)) → ✅ Verdadera (x = 1 cumple S)
- (∃x)S(x) ∨ (∃x)T(x) → ✅ Verdadera

---

### 🧪 Interpretación 2

- S^I = ∅, T^I = {2}, D = {1, 2}

- (∃x)(S(x) ∨ T(x)) → ✅ Verdadera (x = 2)
- (∃x)S(x) ∨ (∃x)T(x) → ✅ Verdadera

---

### 🧪 Interpretación 3

- S^I = ∅, T^I = ∅, D = {1, 2}

- Ambas fórmulas → ❌ Falsas

---

### ✅ Conclusión

Ambas fórmulas **tienen el mismo valor de verdad en todas las interpretaciones**.  
→ **Son lógicamente equivalentes por i-equivalencia**.



| VI  | (∀x)(S(x) ∨ T(x))             | (∀x)S(x) ∨ (∀x)T(x)           |

Guardo esta para despues


## Ejercicio 4

Sea un lenguaje de primer orden con las siguientes características:

- Conjunto de constantes: C = {c, u}
- Sin símbolos de función: F = ∅
- Conjunto de símbolos de predicado: P = {A}

Interpretación I sobre el dominio de los números naturales:

- I(c) = 0
- I(u) = 1
- I(A(x, y)) = "x ≤ y"

---

Verificar si las siguientes afirmaciones son o no correctas. Justificar las respuestas:

- A(c, x) es satisfactible en I.
  - Si es satisfactible ya que x = 0, 0 <= 0  = V
- A(u, x) es satisfactible en I.
  -  Si es satisfactible ya que x = 1 , 0 <= 1  = V
- (∀x)(A(c, x)) es satisfactible en I.
  - Si, todos los Naturales son o iguales o mayores a 0 ya que los negativos no pertenecen a este dominio
- (∀x)(A(u, x)) es satisfactible en I.
  - No, no todos los naturales son o mayor o iguales a u = 1, por ejemple 0 no cumple asique no cumple para todos los naturales
- A(c, x) es verdadera en I.
  Def:Si una fórmula A, con una interpretación I, se satisface en todas las valoraciones, se dice que A es VERDADERA en I. Se escribe así: |=I A.
 Por ejemplo, (∀x) 𝑃12(𝑓12(x, c1), x) es verdadera en la interpretación de losnaturales con la suma y la igualdad.Pq todo número natural x cumple que x + 0 = x
  Según la definición, para ser verdadera en I, debe cumplirse 0 ≤ x para todas las valoraciones posibles de x en el dominio ℕ.
   En ℕ, 0 ≤ x siempre se cumple (porque todos los naturales son ≥ 0). ????
- (∀x)A(c, x) es lógicamente válida.
  -Si una  fórmula es verdadera en toda interpretación  
es  LÓGICAMENTE VÁLIDA. 
La notación es |= A.
 Por ejemplo, ((∀x) P(x) → (∃x) P(x) )es válida, cualquiera sea P. 
  - En este dominio es verdadera la fbf, pero para ser logicamente valida iene q ser verdadero en todos los dominios posibles, y eso no pasa
  - ContraEjemplo:
    Si cambio el dominio a los numeros enteros.
    x = -1, 0 <= -1 = F, por lo tanto no es logicamente valida ??????
  -O tengo q cambiar lo que hace A(x,y) ??

- A(u, c) ∧ ¬A(u, c) es contradictoria.
  - Si es contradictoria, ya q da igual el dominio ni la Interpretacion siempre va a dar falso
  - Las fórmulas falsas en toda interpretación se identifican como CONTRADICCIONES.  
Por ejemplo, la negación de cualquier fórmula lógicamente válida.


### Ejercicio 5
Interpretacion donde todas las formunas son verdaderas:
  Dominio = N
  I-P(x,y) = x <= y
  c = 0
  f(x) = sucecion osea f(x) = x+1
  I. ∀(x) 𝑃(𝑥,𝑥)
    Siempre es verdadero para todo numero natural ya que es menor o igual
  II. ¬((∀y)(∀x)(𝑃(𝑥,𝑦)→𝑃(𝑦,𝑥))) 
      Es verdadero ya que si x <= y, y >= x y da falso pero como es negado da V
  III. ∀𝑥()∀𝑦()∀𝑧()((𝑃(𝑥,𝑦) ∧ 𝑃(𝑦,𝑧)) → 𝑃(𝑥,z))
      Verdadero, si x es menor o igaual a y e y es menor igual a z enyonces x es menor o igual a z.
  IV: ∀𝑥()𝑃(𝑐,𝑥)
      Constante es 0, el dominio los Naturales asique es verdadero que todo numero natural x es menor o igual a 0
  V: (∀𝑥)𝑃(𝑥,𝑓(𝑥))
    Para todo natural ese natural va a ser menor o igual a su sucecion

Interpretacion donde todas las formunas son Falsas
  Dominio = N
  I-P(x,y) = x != y
  c = 0
  f(x) = funcion q no hace nada f(x) = x
  I. ∀(x) 𝑃(𝑥,𝑥)
    Para todo X x no es igual a x
  II. ¬((∀y)(∀x)(𝑃(𝑥,𝑦)→𝑃(𝑦,𝑥))) 
      No es cierto que para todo "y" y para todo x si "x" , no es igual a "y" entonces "y" es no es igual a "x" ????
  III. ∀𝑥()∀𝑦()∀𝑧()((𝑃(𝑥,𝑦) ∧ 𝑃(𝑦,𝑧)) → 𝑃(𝑥,z))
      Para todo x , y , z si x no es igual a y Y y no es igual a z, entonces z no es igual a x
  IV: ∀𝑥()𝑃(𝑐,𝑥)
      para todo x, x no es igual a 0
  V: (∀𝑥)𝑃(𝑥,𝑓(𝑥))
    para todo x x no es igual a x.

