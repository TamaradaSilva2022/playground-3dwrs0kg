# Operadores

Os operadores são usados para realizar operações em variáveis e valores.

O valor é chamado de operando, enquanto a operação (a ser realizada entre os dois operandos) é definida por um operador:

Operando | Operador | Operando
:-------:| :------: | :------:
   100   |    +     |    50

No exemplo abaixo, os números 100 e 50 são **operandos** e o sinal `+` é um **operador**.

Exemplo:

```kotlin runnable
fun main(args: Array<String>) {
    var x = 100 + 50
    println(x) 
```

Embora o operador `+` seja frequentemente usado para somar dois valores, como no exemplo acima, ele também pode ser usado para somar uma variável e um valor, ou uma variável e uma variável.

Exemplo:

```kotlin runnable
fun main(args: Array<String>) {
    var sum1 = 100 + 50       // 150 (100 + 50)
    var sum2 = sum1 + 250     // 400 (150 + 250)
    var sum3 = sum2 + sum2    // 800 (400 + 400)
    println(sum1) 
    println(sum2) 
    println(sum3)
```

Kotlin divide os operadores nos seguintes grupos:

- Operadores aritméticos
- Operadores de atribuição
- Operadores de comparação
- Operadores lógicos

# Operadores aritiméticos

Operadores aritméticos são usados para realizar operações matemáticas comuns.

Operador | Nome          | Descrição                  | Exemplo
:-------:| :-----------: | :------------------------: | :-------:
    +    | Adição        | Soma dois valores          | x + y
    -    | Subtração     | Subtrai um valor de outro  | x - y
    *    | Multiplicação | Multiplica dois valores    | x * y 
    /    | Divisão       | Divide um valor de outro   | x / y
    %    | Módulo        | Retorna o resto da divisão | x % y
    ++   | Incremento    | Aumenta o valor em 1       | ++x
    --   | Diminuir      | Diminui o valor em 1       | --x

# Operadores de atribuição

Os operadores de atribuição são usados para atribuir valores a variáveis.

No exemplo abaixo, usamos o **operador de atribuição** (`=`) para atribuir o valor 10 a uma variável chamada **x**:

```kotlin runnable
fun main(args: Array<String>) {
    var x = 10
    println(x) 
```

O operador de atribuição de adição (`+=`) adiciona um valor a uma variável:

```kotlin runnable
fun main(args: Array<String>) {
    var x = 10
    println(x) 

    x += 5
    println(x) 
```

A tabela abaixo lista todos os operadores de atribuição:

Operador | Exemplo | É o mesmo que 
:-------:| :-----: | :-----------: 
    =    |  x = 5  |   x = 5     
    +=   |  x += 3 |   x = x + 3
    -=   |  x -= 3 |   x = x - 3
    *=   |  x *= 3 |   x = x * 3
    /=   |  x /= 3 |   x = x / 3
    %=   |  x %= 3 |   x = x % 3

# Operadores de comparação

Os operadores de comparação são usados para comparar dois valores e retornam um valor booleano: `true` (verdadeiro) ou `false` falso.

Exemplo: 

```kotlin runnable
fun main(args: Array<String>) {  
    var x = 5
    var y = 3
    println(x == y) // retorna false (falso), porque 5 é diferente de 3
}
```

A tabela abaixo lista todos os operadores de comparação:

Operador | Nome             | Exemplo
:-------:| :--------------: | :-------:
    ==   | Igual a          | x == y
    !=   | Diferente de     | x != y
    >    | Maior que        | x > y
    <    | Menor que        | x < y
    >=   | Maior ou igual a | x >= y
    <=   | Menor ou igual a | x <= y

# Operadores lógicos

Os operadores lógicos são usados para determinar a lógica entre variáveis ou valores.

Exemplo (operador lógico &&):

```kotlin runnable
fun main(args: Array<String>) {  
  var x = 5
  println(x > 3 && x < 10) // retorna true (verdadeiro), porque 5 é maior que 3 E 5 menor que 10
}
```

A tabela abaixo lista todos os operadores lógicos:

Operador | Nome       | Descrição                                                        | Exemplo
:-------:| :--------: | :--------------------------------------------------------------: | :--------------:
   `&&`  | E lógico   | Retorna verdadeiro se ambas as declarações forem verdadeiras     | `x < 5 &&  x < 10`
   `||`  | OU lógico  | Retorna verdadeiro se uma das afirmações for verdadeira          | `x < 5 || x < 4`
   `!`   | NÃO lógico | Inverte o resultado, retorna falso se o resultado for verdadeiro | 

