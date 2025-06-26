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

II.   ∃𝑥()(∀𝑦)𝑅(𝑥,𝑦) (∀𝑦)∃𝑥()𝑅(𝑥,𝑦)