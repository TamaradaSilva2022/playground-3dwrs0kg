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
