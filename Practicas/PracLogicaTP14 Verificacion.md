### Trabajo Practico nro 14
#### Ejercicio 1.
1.1)La prueba semantica utiliza las instrucciones del lenguaje, mientras q la sintactica usa axiomas y reglas de un metodo logico-deductivo

### Ejercicio 2
{x = X and X > 0} S {x = X and y = X*X}

Programa:
z := x;
y := x*z

formal:
{x = X and X > 0} z := x, y:= x * z {x = X and y = X*X}


### Ejercicio 3
3.1:  {x > 0} while x > 0 do x := x – 2 od {true}
Se cumple

3.2. {x > 0} while x > 0 do x := x – 2 od {x = 0}
No se cumple, podria ser x = -1

3.3. {x > 0} while x ≠ 0 do x := x – 2 od {true} 
No se cumple, si x = -1, sigue infinitamente

### Ejercicio 4
{True}x := 0;x := x + 1; x := x+2 {x = 3}
1. [ASI]{x + 2 = 3} x := x+2{x = 3}
2. [ASI]{(x + 1) + 2 = 3} x := x+1{x+2 = 3}
3. [ASI]{0 + 1 + 2 = 3} x := 0{x +1 +2 = 3}
4. //0 +1 +2 = 3 es TRUE
5. [SEC 1,2,3]{TRUE}x := 0;x := x + 1; x := x+2{x = 3}


### Ejercicio 5 
 Se cumple {x = 10} while x > 0 do x := x – 1 od {x = 0}. Se pide probar (usando la 
lógica de Hoare) que el predicado p = (x  0) es un invariante del while.

 p = (x >= 0) 
 Ayuda: hay que probar, por un lado: x = 10 ⟶ p, y por otro lado: {p y x > 0} x := x – 1 {p}. 

 x = 10 ⟶ p?
 x = 10 -> x >= 0 Si es matematica pura.

 {x >= 0 y x > 0} x:= x -1 {x >= 0} ?
 Logica de Hoare
 { x-1 >= 0} x:= x-1 {x >= 0} ASI
 {x >= 0 y x > 0} x:= x -1 {x >= 0} CONS:
{x >= 0 y x > 0 }-> {x-1 >= 0} es cierto, como x > 0 x -1 siempre va a 
ser >= 0, 
P = x >= 0 es una invariante del while
### Ejercicio 6.
 La instrucción repeat S until B consiste en ejecutar S, luego evaluar B, si B es falsa 
volver  a  iterar,  y  en  caso  contrario  terminar.  Explicar  informalmente  por  qué  la  siguiente  regla 
para probar  la instrucción es sensata (es decir, si se cumplen las premisas, entonces también 
se cumple la conclusión):  
   {p} S {q} , q y ¬B ⟶ p    
{p} repeat S until B {q y B}


