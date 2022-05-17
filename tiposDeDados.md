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

**Exemplo:** 

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Byte = 100
    println(myNum)
}
```

### Short

O tipo de dados `Short` pode armazenar números inteiros de -32768 a 32767.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Short = 5000
    println(myNum)
}
```

### Int

O tipo de dados `Int` pode armazenar números inteiros de -2147483648 a 2147483647.

**Exemplo:**

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

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Long = 15000000000L
    println(myNum)
}
```

### Diferença entre Int e Long

Um número inteiro é um `Int` desde que seja até 2147483647. Se for além disso, esse inteiro é definido como `Long`.

```kotlin
val myNum1 = 2147483647  // Int
val myNum2 = 2147483648  // Long
```

## Tipos de ponto flutuante

O tipo de dados Ponto Flutuante representa números com um decimal, como 9,99 ou 3,14515.

Os tipos de dados `Float` e `Double` podem armazenar números fracionários.

**Exemplo de Float:**

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Float = 5.75F
    println(myNum)
}
```

**Exemplo de Double:**

```kotlin runnable
fun main(args: Array<String>) {
    val myNum: Double = 19.99
    println(myNum)
}
```


###### ***Quando usar Float ou Double?***

***A precisão de um valor de ponto flutuante indica quantos dígitos o valor pode ter após o ponto decimal (a vírgula).*** 
***A precisão do `Float` é de apenas seis ou sete dígitos decimais, enquanto as variáveis `Double` têm uma precisão de cerca de 15 dígitos.*** 
***Portanto, é mais seguro usar `Double` para a maioria dos cálculos.***

***Observe também que você deve terminar o valor de um tipo `Float` com um "F".***


## Números científicos
Um número de ponto flutuante também pode ser um número científico com um "e" ou "E" para indicar a potência de 10.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myNum1: Float = 35E3F
    val myNum2: Double = 12E4
    println(myNum1)
    println(myNum2)

}
```

# Booleans

Muitas vezes, na programação, você precisará de um tipo de dados que só pode ter um de dois valores, como:

- SIM / NÃO
- LIGADO / DESLIGADO
- VERDADEIRO / FALSO

Para isso, o Kotlin possui um tipo de dado chamado `Boolean`, que pode assumir os valores  `true` (verdadeiro) ou `false` (falso).

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val isKotlinFun: Boolean = true
    val isOnionTasty: Boolean = false
    println(isKotlinFun)   // Outputs true
    println(isOnionTasty)   // Outputs false 
}
```

## Expressões Booleanas

Uma expressão booleana retorna um valor booleano: `true` ou `false`.

Você pode usar um operador de comparação, como o operador maior que (>), menor que (<), igual (==), etc, para descobrir se uma expressão (ou uma variável) é verdadeira.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val x = 10
    val y = 9
    println(x > y) // Retorna true (verdadeiro), porque 10 é maior que 9
}
```

Ou ainda mais fácil:

```kotlin runnable
fun main(args: Array<String>) {
    println(10 > 9) // Retorna true (verdadeiro), porque 10 é maior que 9
}
```

**Mais um exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val x = 15;
    println(x == 10); // Retorna false (falso), porque o valor de x é diferente de 10
}
```

***O valor booleano de uma expressão é a base para todas as comparações e condições Kotlin.***

# Characters

O tipo de dados `Char` é usado para armazenar um **único** caractere. 
Um valor char deve estar entre **aspas simples**, como 'A' ou 'c'.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myGrade: Char = 'B'
    println(myGrade)
}
```
Em Kotlin, você não pode usar valores ASCII para exibir determinados caracteres. 
O valor 66 geraria um "B" em Java, por exemplo, mas geraria um erro em Kotlin.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myLetter: Char = 66
    println(myLetter) // Error
}
```

# Strings

O tipo de dados `String` é usado para armazenar texto.
Uma string contém uma coleção de caracteres entre **aspas duplas**.

```kotlin
var greeting = "Hello"
var greeting: String = "Hello"
```

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val myText: String = "Hello World"
    println(myText)
}
```

***Nota: Se você deseja criar uma String sem atribuir o valor (e atribuir o valor posteriormente), deve especificar o tipo ao declarar a variável.***

**Exemplo (vai dar erro por não especificar o tipo ao declarar a variável):**
```kotlin runnable
fun main(args: Array<String>) {
    var name
    name = "John"
    println(name)
}
```

Mesmo exemplo escrito de forma correta (sem erros):

```kotlin runnable
fun main(args: Array<String>) {
    var name: String
    name = "John"
    println(name)
}
```

### Acessando uma string

Para acessar os caracteres (elementos) de uma string, você deve consultar o **número do índice** entre **colchetes** (`[]`).

Os índices de string começam com 0. No exemplo abaixo, acessamos o primeiro e o terceiro elemento em `txt`:

```kotlin runnable
fun main(args: Array<String>) {
    var txt = "Hello World"
    println(txt[0]) // first element (H)
    println(txt[2]) // third element (l)
}
```

***Assim, [0] é o primeiro elemento. [1] é o segundo elemento, [2] é o terceiro elemento, etc.***

### Comprimento de uma String

Uma String em Kotlin é um objeto que contém propriedades e funções que podem realizar certas operações em strings, escrevendo um caractere de ponto (`.`) após a variável de string específica. Por exemplo, o comprimento de uma string pode ser encontrado com a propriedade `length`, como mostrado no exemplo a seguir:

```kotlin runnable
fun main(args: Array<String>) {
    var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    println("O comprimento da String txt é: " + txt.length)
}
```

### Funções de String

Existem muitas funções de String disponíveis Kotlin, por exemplo, `toUpperCase()` e `toLowerCase()`.

```kotlin runnable
fun main(args: Array<String>) {
    var txt = "Hello World"
    println(txt.toUpperCase())   // Mostra "HELLO WORLD"
    println(txt.toLowerCase())   // Mostra "hello world"
}
```

Para enconntrar mais funções úteis olhe sempre a documentação da linguagem.

# Comparando Strings

A função `compareTo(string)` compara duas strings e retorna 0 se ambas forem iguais.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var txt1 = "Hello World"
    var txt2 = "Hello World"
    println(txt1.compareTo(txt2))  // Mostra 0 (eles são iguais)
}
```

# Encontrando uma string dentro de uma string

A função ``indexOf()`` retorna o **índice** (a posição) da primeira ocorrência de um texto especificado em uma string (incluindo espaços em branco).

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var txt = "Please locate where 'locate' occurs!"
    println(txt.indexOf("locate"))  // Mostra 7
}
```

***Lembre-se que o Kotlin conta as posições a partir do zero.
0 é a primeira posição em uma string, 1 é a segunda, 2 é a terceira, etc.***

# Aspas dentro de uma string

Para usar aspas dentro de uma string, use aspas simples (').

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var txt1 = "It's alright"
    var txt2 = "That's great"
    println(txt1)
    println(txt2)
}
```

# Concatenação de Strings

O operador `+` pode ser usado entre strings para adicioná-las para formar uma nova string. 
Isso é chamado de concatenação.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var firstName = "John"
    var lastName = "Doe"
    println(firstName + " " + lastName)
}
```

***Observe que adicionamos um texto vazio (" ") para criar um espaço entre `firstName` e `lastName` na impressão.***

Também é possível usar a função `plus()` para concatenar duas strings.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var firstName = "John "
    var lastName = "Doe"
    println(firstName.plus(lastName))
}
```

# Expressões modelo/Interpolação

Em vez de concatenação, você também pode usar expressões modelo (template strings), que é uma maneira fácil de adicionar variáveis e expressões dentro de uma string. 
Uma expressão modelo começa com um cifrão (`$`).

**Exemplo:** 

```kotlin runnable
fun main(args: Array<String>) {
    var firstName = "John"
    var lastName = "Doe"
    println("My name is $firstName $lastName")
}
```

***"String Templates" é um recurso popular do Kotlin, pois reduz a quantidade de código. Por exemplo, você não precisa especificar um espaço em branco entre firstName e lastName, como fizemos no exemplo de concatenação.***

# Arrays

# Conversão de tipo

A conversão de tipo é quando você converte o valor de um tipo de dados para outro tipo.

Em Kotlin, a conversão de tipo numérico é diferente de Java. 
Por exemplo, não é possível converter um tipo `Int` em um tipo `Long` com o seguinte código:

```kotlin runnable
fun main(args: Array<String>) {
    val x: Int = 5
    val y: Long = x
    println(y) // Error: Type mismatch 
}
```

Para converter um tipo de dados numérico para outro tipo, você deve usar uma das seguintes funções: 
`toByte()`, `toShort()`, `toInt()`, `toLong()`, `toFloat()`, `toDouble()` ou `toChar()`.

Exemplo:

```kotlin runnable
fun main(args: Array<String>){
    val x: Int = 5
    val y: Long = x.toLong()
    println(y)
}
```