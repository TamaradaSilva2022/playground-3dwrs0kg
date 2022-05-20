# Ponto de entrada

Um ponto de entrada de um aplicativo Kotlin é a função ``main``, o que significa que todo programa Kotlin começa com a função main(). 
As funções são criadas com a palavra-chave ``fun`` no Kotlin (leremos mais sobre funções no capítulo sobre elas).

**Sintaxe:**

```kotlin
fun main() {

}
```

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    println("Hello, World!")
}
```

>**Explicando o exemplo anterior**
>
>***O programa começa com a função `main`, que é o ponto de entrada de todo programa escrito em Kotlin.*** 
***Dentro da função `main`, utilizamos a função `println()` imprimir o texto "Hello, World!" no console (a função print será explicada no próximo bloco).***

# Palavras reservadas

Toda linguagem de programação tem certas palavras predefinidas que carregam algum significado especial. Elas são conhecidas como palavras reservadas. 
As palavras-chave **não** podem ser usadas como identificadores.

Um identificador é o nome dado a uma variável, classe, função, interface etc.

Por exemplo, ``name`` é um identificador aqui:

```kotlin
val name: String = "emp_name"
```

As palavras reservadas Kotlin são:

as     | break | class     | continue
-------|-------|-----------|---------- 
do     | else  | false     | for
-------|-------|-----------|---------- 
fun    | if    | in        | interface
-------|-------|-----------|---------- 
is     | null  | object    | package
-------|-------|-----------|---------- 
return | super | this      | throw
-------|-------|-----------|---------- 
true   | try   | typealias | typeof
-------|-------|-----------|---------- 
val    | var   | when      | while