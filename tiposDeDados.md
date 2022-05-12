# Tipos de dados

Em Kotlin, o tipo de uma variável é decidido pelo seu valor:

```kotlin
val myNum = 5             // Int
val myDoubleNum = 5.99    // Double
val myLetter = 'D'        // Char
val myBoolean = true      // Boolean
val myText = "Hello"      // String
```

No entanto, você aprendeu no capítulo anterior que é possível especificar o tipo se desejar:

```kotlin
val myNum: Int = 5                // Int
val myDoubleNum: Double = 5.99    // Double
val myLetter: Char = 'D'          // Char
val myBoolean: Boolean = true     // Boolean
val myText: String = "Hello"      // String
```

Às vezes você tem que especificar o tipo, e muitas vezes não. De qualquer forma, é bom saber o que os diferentes tipos representam.

Os tipos de dados são divididos em diferentes grupos:

- Numbers (Números)
- Characters (Caracteres)
- Booleans (Booleanos)
- Strings (frases)
- Arrays (vetores e matrizes)

# Numbers

Os tipos de numbers (os números) são divididos em dois grupos:

Os **tipos inteiros** armazenam números inteiros, positivos ou negativos (como 123 ou -456), sem decimais. 
Os tipos válidos são `Byte`, `Short`, `Int` e `Long`.

Os **tipos ponto flutuante** representam números com uma parte fracionária, contendo um ou mais decimais. 
Existem dois tipos: `Float` e `Double`.

***OBS: Se você não especificar o tipo de uma variável numérica, ela geralmente é retornada como `Int` para números inteiros e `Double` para números de ponto flutuante.***

## Tipos inteiros

### Byte

O tipo de dados `Byte` pode armazenar números inteiros de -128 a 127. 
Isso pode ser usado em vez de `Int` ou outros tipos inteiros para economizar memória quando você tiver certeza de que o valor estará entre -128 e 127.

Exemplo: 

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Byte = 100
    println(myNum)
}
```

### Short

O tipo de dados `Short` pode armazenar números inteiros de -32768 a 32767.

Exemplo: 

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Short = 5000
    println(myNum)
}
```

### Int

O tipo de dados `Int` pode armazenar números inteiros de -2147483648 a 2147483647.

Exemplo:

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Int = 100000
    println(myNum)
}
```

### Long

O tipo de dados `Long` pode armazenar números inteiros de -9223372036854775807 a 9223372036854775807. 
Isso é usado quando `Int` não é grande o suficiente para armazenar o valor. 
Opcionalmente, você pode terminar o valor com um "L".

Exemplo:

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Long = 15000000000L
    println(myNum)
}
```

