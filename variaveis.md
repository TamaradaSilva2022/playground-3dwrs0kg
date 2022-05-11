# Variáveis Kotlin

Variáveis são contêineres para armazenar valores de dados.

Para criar uma variável, use `var` ou `val` e atribua um valor a ela com o sinal de igual `=`:

### Sintaxe

```
var variableName = value
val variableName = value
```

### Exemplo

```kotlin runnable
fun main(args: Array<String>) {
     /*Declaração das variáveis*/
    var name = "John"
    val birthyear = 1975
    
    /*Impressão das variáveis*/
    println(name)
    println(birthyear)
}
```

A diferença entre `var` e `val` é que as variáveis declaradas com a palavra-chave `var` **podem ser alteradas/modificadas**, 
enquanto as variáveis `val` **não podem**.

# Tipo de variável

Ao contrário de muitas outras linguagens de programação, as variáveis em Kotlin não precisam ser declaradas com um tipo específico 
(como "String" para texto ou "Int" para números, se você estiver familiarizado com eles).

Para criar uma variável em Kotlin que deve armazenar texto e outra que deve armazenar um número, veja o exemplo a seguir:

```kotlin runnable
fun main(args: Array<String>) {
    /*Declaração das variáveis*/
    var name = "John"      // String (texto)
    val birthyear = 1975   // Int (número)

    /*Impressão das variáveis*/
    println(name)          // Imprime o valor de name
    println(birthyear)     // Imprime o valor de birthyear
}
```

Kotlin é inteligente o suficiente para entender que **"John"** é uma `String` (texto) e que **1975** é uma variável `Int` (número inteiro).

No entanto, é possível especificar o tipo se você desejar:

```kotlin runnable
fun main(args: Array<String>) {
    /*Declaração das variáveis*/
    var name: String = "John"   // String (texto)
    val birthyear: Int = 1975   // Int (número)

    /*Impressão das variáveis*/
    println(name)          // Imprime o valor de name
    println(birthyear)     // Imprime o valor de birthyear
}
```

Você também pode declarar uma variável sem atribuir o valor, atribuindo o valor posteriormente. 
No entanto, isso só é possível quando você especifica o tipo:

- Exemplo que funciona: tipo especificado ao criar a variável

```kotlin runnable
fun main(args: Array<String>) {
   var name: String
   name = "John"
   println(name)
}
```

- Exemplo que não funciona: não especificou o tipo ao criar a variável

```kotlin runnable
fun main(args: Array<String>) {
   var name: String
   name = "John"
   println(name)
}
```
