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

Os tipos de números são divididos em dois grupos:

Os **tipos inteiros** armazenam números inteiros, positivos ou negativos (como 123 ou -456), sem decimais. 
Os tipos válidos são `Byte`, `Short`, `Int` e `Long`.

Os **tipos ponto flutuante** representam números com uma parte fracionária, contendo um ou mais decimais. 
Existem dois tipos: `Float` e `Double`.

***OBS: Se você não especificar o tipo de uma variável numérica, ela geralmente é retornada como `Int` para números inteiros e `Double` para números de ponto flutuante.***

