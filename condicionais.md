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

***No exemplo acima, o tempo (20) é maior que 18, então a condição é falsa, então passamos para a condição `else` e imprimimos na tela "Boa noite".*** 
***Se a hora fosse menor que 18, o programa imprimiria "Bom dia".***

# else if

Use `else if` para especificar uma nova condição se a primeira condição for falsa.

Sintaxe:

```kotlin
if (condição1) {
   // bloco de código a ser executado se condition1 for true
} else if (condição2) {
   // bloco de código a ser executado se a condição1 for falsa e a condição2 for verdadeira
} senão {
   // bloco de código a ser executado se condition1 for false e condition2 for false
}
```

Exemplo: