# LABORATORIO 03
## Instrucciones condicionales e iterativas

### TAREA 1. Ejercicios obligatorios
1. **Función condicional.** Escribe una _función_ llamada **f** que, dados dos valores enteros `x` y `pos`, devuelve otro valor entero de acuerdo con la siguiente fórmula:
    ```math
    𝑓(𝑥, 𝑝𝑜𝑠) = {
        𝑥 𝑠𝑖 𝑝𝑜𝑠 𝑒𝑠 𝑝𝑎𝑟
        2𝑥 𝑠𝑖 𝑝𝑜𝑠 𝑒𝑠 𝑖𝑚𝑝𝑎𝑟 𝑦 𝑥 < 5
        2𝑥 − 9 𝑠𝑖 𝑝𝑜𝑠 𝑒𝑠 𝑖𝑚𝑝𝑎𝑟 𝑦 𝑥 ≥ 5
    }
    ```
2. **Trigonométrica a polar.** Implementa el _procedimiento_ **polar** que, dado un número complejo en formato trigonométrico (a,b), nos devuelve el mismo número complejo en forma polar. Para definir exactamente el ángulo, hace falta estudiar el signo de `a` y `b` y determinar el cuadrante en el que se encuentra. En Ada, existe la biblioteca `Ada.Numerics.Elementary_Functions` que ofrece la arcotangente (`arctan`).
    ```math
    𝑚𝑜𝑑𝑢𝑙𝑜 = |√𝑎^2 + 𝑏^2|
    𝑎𝑟𝑔𝑢𝑚𝑒𝑛𝑡𝑜 = {
        𝑎𝑟𝑐𝑡𝑎𝑛(𝑏/𝑎) 𝑠𝑖 𝑎 > 0 𝑦 𝑏 > 0
        2𝜋 + 𝑎𝑟𝑐𝑡𝑎𝑛(𝑏/𝑎) 𝑠𝑖 𝑎 > 0 𝑦 𝑏 < 0
        𝜋 + 𝑎𝑟𝑐𝑡𝑎𝑛(𝑏/𝑎) 𝑠𝑖 𝑎 < 0
        +𝜋/2 𝑠𝑖 𝑎 = 0 𝑦 𝑏 ≥ 0
        -𝜋/2 𝑠𝑖 𝑎 = 0 𝑦 𝑏 ≤ 0
    }
    ```
3. **Resultado de la ONCE.** Crea un _algoritmo_ que, dados dos números de cuatro cifras (el número de cupón premiado y el número de cupón que hay que comprobar), obtenga el premio que le corresponde al cupón a comprobar, sabiendo que si tiene los cuatro dígitos iguales (y en el mismo orden) le corresponden 100000 euros, si coinciden los tres últimos dígitos le corresponden 50000 euros y si son los dos últimos el premio son 3 euros. El resto de los casos no tiene premio asociado.
4. **Contar y sumar múltiplos.** Dados dos números naturales `N1` y `N2`, haz un _procedimiento_ que devuelve la suma de los múltiplos de 3 entre `N1` y `N2` (ambos inclusive). `N1` es estrictamente menor que `N2`. Haz que el programa cuente también los múltiplos de 3.
    - Ejemplo: Para `N1=5` y `N2=15`, la suma es 42 (es decir, 42=6+9+12+15) y la cuenta es 4 (los cuatro números mencionados).
5. **Factorial.** Crea una _función_ que, dado un número positivo, devuelva el número factorial de ese número. La fórmula que define el factorial de un número es la siguiente:
    ```math
    𝑛! = 𝑛 ∙ (𝑛 − 1) ∙ (𝑛 − 2) ∙ ⋯ ∙ 2 ∙ 1
    ```
6. **Decimal a Binario.** Crea un _procedimiento_ que, dado un número decimal, lo convierta a un número binario haciendo divisiones sucesivas entre dos.
    - Ejemplo: Para los datos 127 y 2925, los resultados deben ser 1111111 y 101101101101, respectivamente.

### TAREA 2. Ejercicios extra
7. **Segundo anterior.** Crea el _procedimiento_ **segundo_anterior** que, dada una hora válida (horas, minutos y segundos), calcule qué hora era un segundo antes.
8. **Ecuación de segundo grado.** Crea el _procedimiento_ **solucionar** que nos devuelva las soluciones de una ecuación de segundo grado. Solo estamos interesados en las soluciones reales (no las imaginarias). El procedimiento debe detectar cuántas soluciones reales tiene la ecuación (0, 1 ó 2) y devolver los valores adecuados para ello. Si no hay soluciones, los valores de las soluciones no tendrán sentido. Si solo hay una solución, solo se dará una solución y si hay dos las dos.
    - La fórmula de las soluciones de una ecuación de segundo grado 𝑎𝑥^2 + 𝑏𝑥 + 𝑐 es la que aparece más abajo. Para calcular la raíz cuadrada, puedes usar la función `Sqrt` de la biblioteca de funciones `Ada.Numerics.Elementary_functions`.
    ```math
    𝑥 = −𝑏 ± √𝑏^2 − 4𝑎𝑐 / 2𝑎
    ```
9. **Añadir duración a una tarea.** Crea un _algoritmo_ que, dada la hora de comienzo de una tarea y la duración en segundos de ésta, calcule la hora en que finalizará la tarea. La duración de la tarea puede ser de varias horas, pero nunca superior a media jornada (14400s). Las tareas incompletas continúan en la siguiente jornada. La jornada laboral es de 8:00 a 16:00.
10. **Secuencia de Collatz.** Escribe un _procedimiento_ que muestre en pantalla la secuencia de Collatz de un número entero positivo dado, y devuelva, además, la longitud de la secuencia y la suma de sus números.
    - Ejemplo: Para el dato 18, la secuencia de Collatz es <18, 9, 28, 14, 7, 22, 11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1>. La secuencia tiene 21 números y la suma es 357.
11. **Fibonacci.** Crea una _función_ que calcule el número de la serie de Fibonacci. La serie de Fibonacci comienza con los números 0 y 1 y el resto de los elementos se corresponde con la suma de los dos anteriores.
    ```
    F0  F1  F2  F3  F4  F5  F6  F7  F8  F9  F10  F11  F12  F13 ...
    0   1   1   2   3   5   8   13  21  34  55   89   144  233 ...
    ```
12. **Divisores propios.** Crea un _procedimiento_ que indique cuántos divisores propios tiene un número entero `N`. Contamos entre los posibles divisores a aquellos números positivos entre 1 y `N-1` cuya división es exacta.

### TAREA 3. Ejercicios para pensar
13. **Día anterior.** Crea un _procedimiento_ que, modifique una fecha dada (día, mes y año) y coloque en su lugar el día anterior. Comienza considerando que todos los años no son bisiestos. Luego añade la condición de que el año puede ser bisiesto. Los años bisiestos son los que son múltiplos de 4 y no son múltiplos de 100. Los múltiplos de 400 son una excepción, ya que, aun siendo múltiplos de 100, son bisiestos.
14. **Estación del año.** Crea una _función_ que dados dos números enteros día y mes, indique a qué estación del año corresponde dicha fecha. Se considera que la primavera va desde el 21 de marzo hasta el 20 de junio; el verano se extiende desde el 21 de junio al 20 de septiembre; el otoño dura desde el 21 de septiembre hasta el 20 de diciembre; y el invierno ocurre entre el 21 de diciembre y el 20 de marzo.
15. **Estación del año enumerada.** Crea una _función_ equivalente a la del ejercicio anterior que, en lugar de devolver un STRING, devuelva un valor del tipo `T_Estacion` (ya definido en el fichero de especificación).
16. **Número perfecto.** Crea la _función_ **es_perfecto** que, dado un número entero positivo `N`, indique si `N` es perfecto. Se considera que un número es perfecto si el número es igual a la suma de sus divisores propios.
17. **Contenido del texto.** Construye un _procedimiento_ que lea del teclado un texto que termina en punto (.) y devuelva (1) cuántos espacios, (2) cuántas letras y (3) cuántos dígitos hay en dicho texto. Cualquier otro carácter encontrado se ignora en la cuenta. Por ejemplo, si el texto es "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum." el resultado debería ser el correspondiente hasta el primer punto encontrado (lo que aparece en negrita, terminado en aliqua) y sería: 102 letras, 18 espacios y 0 dígitos.
18. **El método de Newton-Raphson.** Es un _algoritmo_ para encontrar aproximaciones de los ceros o raíces de una función real. También puede ser usado para encontrar el máximo o mínimo de una función, encontrando los ceros de su primera derivada. Sean dos funciones `f(x)` y su derivada `f'(x)`. La idea consiste en ir calculando sucesivos valores de `x_i` siguiendo la fórmula siguiente, hasta que el error sea menor que una cierta cantidad.
    ```math
    𝑥𝑖 = 𝑥𝑖−1 − 𝑓(𝑥𝑖−1) / 𝑓′(𝑥𝑖−1)
    𝐸𝑟𝑟𝑜𝑟 = |𝑥𝑖 − 𝑥𝑖−1| / |𝑥𝑖|
    ```
    - Ejemplo: Aplica el método para calcular `x` de `𝑓(𝑥) = cos(𝑥) − 𝑥^3`, partiendo de `x0=0.5` con un error menor a 0.001. Necesitarás definir una función `f(x)`, la función derivada `𝑓′(𝑥) = 𝑠𝑒𝑛(𝑥) − 3𝑥^2`.

