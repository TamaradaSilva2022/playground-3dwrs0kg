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
fun main(args: Args<String>){
    if (20 > 18) {
    println("20 é maior que 18")
}
}
```