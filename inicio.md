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

Toda linguagens de programação tem certas palavras predefinidas que carregam algum significado especial. Elas são conhecidas como palavras reservadas. 
As palavras reservadas **não** podem ser usadas como identificadores.

Um identificador é o nome dado a uma variável, classe, função, interface etc.

Por exemplo, ``name`` é um identificador aqui:

```kotlin
val name: String = "emp_name"
```

As palavras reservadas Kotlin são:

|:------:|:-----:|:---------:|:----------:|
| as     | break | class     | continue   |
| do     | else  | false     | for        |
| fun    | if    | in        | interface  |
| is     | null  | object    | package    |
| return | super | this      | throw      |
| true   | try   | typealias | typeof     |
| val    | var   | when      | while      |

# Entrada e saída

A entrada e saída do usuário são parte essencial de qualquer programa. Eles vão ajudar na interação do usuário.

### Mostrando a saída no console

Para imprimir a saída na janela do console, podemos usar as funções `print()` e `println()`. 
A função `print()` continuará adicionando a saída à mesma linha, `println()` imprimirá a saída e moverá o cursor para a próxima linha. 

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    println("Hello")
    println("World!!\n")

    print("Bye, ")
    print("World!!")
}
```

>>**Explicando o exemplo anterior**
>
> ***Neste exemplo, as duas primeiras saídas são impressas usando a função `println()`. Então, elas apareceram em linhas diferentes.***
> ***Mas as próximas duas instruções são impressas usando a função `print()`, por conta disso elas aparecerão na mesma linha.***

### Obter entrada do usuário

Para receber a entrada do usuário, usamos a função `readline()`. 
Por padrão, ela receberá a entrada como uma String, que é um texto. 
Se precisarmos usar qualquer outro tipo de entrada, como número, booleano, etc., ela precisa ser convertida para um tipo específico, o que significa especificar e converter explicitamente a entrada de String para algum outro tipo de dados (os tipos de dados da linguagem serão mostrados em capítulos posteriores).

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    println("Digite a string: ")
    var inputString = readLine()
    println("A entrada no formato de string é: $inputString")

    println("Digite o número: ")
    var inputNumber = Integer.valueOf(readLine())
    println("A entrada no formato de número inteiro é: $inputNumber")
}
```

Outra forma de converter a entrada para diferentes tipos de dados em cada caso é criando um objeto da classe `Scanner` e usá-lo para receber entrada.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var scanner = Scanner(System.`in`)
    
    println("Digite um número: ")
    var inputNumber = scanner.nextInt()
    println("A entrada em formato de número inteiro é: $inputNumber")
}
```

Da mesma forma, podemos usar `nextBoolean()`, `nextFloat()`, `nextLong()` e `nextDouble()` para diferentes tipos de variáveis.

```
Fonte:

https://www.w3schools.com/kotlin/kotlin_output.php
https://www.studytonight.com/kotlin/kotlin-keywords-and-identifiers
https://www.studytonight.com/kotlin/kotlin-input-and-output

```