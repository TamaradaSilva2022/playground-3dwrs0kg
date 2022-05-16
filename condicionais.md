# Condicionais

Kotlin suporta as condições lógicas usuais da matemática, como:

- Menor que: `a < b`
- Menor ou igual a: `a <= b`
- Maior que: `a > b`
- Maior ou igual a: `a >= b`
- Igual a: `a == b`
- Diferente de: `a != b`

Você pode usar essas condições para executar ações diferentes para decisões diferentes através das condicionais do Kotlin. 

Assim, Kotlin tem as seguintes condicionais:

- Use `if` para especificar um bloco de código a ser executado, se uma condição especificada for verdadeira
- Use `else` para especificar um bloco de código a ser executado, se a mesma condição for falsa
- Use `else if` para especificar uma nova condição a ser testada, se a primeira condição for falsa
- Use `when` para especificar muitos blocos alternativos de código a serem executados

# if

Use `if` para especificar um bloco de código a ser executado se uma condição for `true` (verdadeira).

Sintaxe:

```kotlin
if (condição) {
  // bloco de código a ser executado se a condição for verdadeira
}
```

***Observe que `if` está em letras minúsculas. Letras maiúsculas (If ou IF) gerarão um erro.***

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    if (20 > 18) {
        println("20 é maior que 18")
    }
}
```

Também podemos testar variáveis, como no exemplo abaixo:

```kotlin runnable
fun main(args: Array<String>){
    val x = 20
    val y = 18
    if (x > y) {
        println("x é maior que y")
    }
}
```

### ***Explicação do exemplo***

***No exemplo acima usamos duas variáveis, `x` e `y`, para testar se `x` é maior que `y` (usando o operador `>`).*** 
***Como `x` é 20 e `y` é 18, e sabemos que 20 é maior que 18, imprimimos na tela que "x é maior que y".***

# else

Use `else` para especificar um bloco de código a ser executado se a condição for falsa.

Sintaxe:

```kotlin
if (condição) {
   // bloco de código a ser executado se a condição for verdadeira
} else {
   // bloco de código a ser executado se a condição for falsa
}
```

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    val time = 20
    if (time < 18) {
        println("Bom dia.")
    } else {
        println("Boa noite.")
    }
}
```

### ***Explicação do exemplo***

***No exemplo acima, `time` (20) é maior que 18, então a condição é falsa, então passamos para a condição `else` e imprimimos na tela "Boa noite".*** 
***Se a hora fosse menor que 18, o programa imprimiria "Bom dia".***

# else if

Use `else if` para especificar uma nova condição se a primeira condição for falsa.

Sintaxe:

```kotlin
if (condição1) {
   // bloco de código a ser executado se condition1 for true
} else if (condição2) {
   // bloco de código a ser executado se a condição1 for falsa e a condição2 for verdadeira
} else {
   // bloco de código a ser executado se condition1 for false e condition2 for false
}
```

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    val time = 22
    if (time < 12) {
        println("Bom dia.")
    } else if (time < 18) {
        println("Boa tarde.")
    } else {
        println("Boa noite.")
    }
}
```

### ***Explicação do exemplo***

No exemplo acima, `time` (22) é maior que 10, então a primeira condição é falsa. 
A próxima condição, na instrução `else if`, também é falsa, então passamos para a condição `else`, já que condição1 e condição2 são ambas falsas, e imprimimos na tela "Boa noite".
No entanto, se a hora fosse 14, nosso programa imprimiria "Boa tarde".

# Expressões if...else

Em Kotlin, você também pode usar instruções `if...else` como expressões (ou seja, atribuir um valor a uma variável e devolvê-lo).

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    val time = 20
    val greeting = if (time < 18) {
        "Bom dia."
    } else {
        "Boa noite."
    }
    println(greeting)
}
```

Ao usar `if` como uma expressão, você também deve incluir `else` (obrigatório).

***Observação: você pode omitir as chaves {} quando `if` tiver apenas uma instrução.***

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    val time = 20
    val greeting = if (time < 18) "Bom dia." else "Boa tarde."
    println(greeting)
}
```

# When

Em vez de escrever muitas expressões `if..else`, você pode usar a expressão `when`, que é muito mais fácil de ler.
Ele é usado para selecionar um dos muitos blocos de código a serem executados.

**Exemplo:** *Use o número do dia da semana para calcular o nome do dia da semana:*

```kotlin runnable
fun main(args: Array<String>){
    val day = 4

    val result = when (day) {
        1 -> "Segunda-feira"
        2 -> "Terça-feira"
        3 -> "Quarta-feira"
        4 -> "Quinta-feira"
        5 -> "Sexta-feira"
        6 -> "Sábado"
        7 -> "Domingo"
        else -> "Dia inválido"
    }
    println(result)
}
```

É assim que funciona:

- A variável dentro de `when` (`day`) é avaliada uma vez
- O valor da variável `day` é comparado com os valores de cada "ramo"
- Cada ramo começa com um valor, seguido por uma seta (`->`) e um resultado, que é armazenado na variável `result`
- Se houver uma correspondência, o bloco de código associado é executado
- `else` é usado para especificar algum código a ser executado se não houver correspondência
- No exemplo acima, o valor de `day` é 4, significando que o valor "Quinta-feira" será impresso