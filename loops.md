# Loops

Os loops podem executar um bloco de código desde que uma condição especificada seja alcançada.

Os loops são úteis porque economizam tempo, reduzem erros e tornam o código mais legível.

# while

O loop `while` percorre um bloco de código enquanto uma condição especificada for verdadeira.

**Sintaxe:**

```kotlin
while (condição) {
  // bloco de código a ser executado
}
```

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>){
    var i = 0
    while (i < 5) {
        println(i)
        i++
    } 
}
```

***Nota: Não esqueça de aumentar a variável usada na condição, caso contrário o loop nunca terminará.***

# do...while

O loop `do..while` é uma variante do loop `while`. Este loop executará o bloco de código uma vez, antes de verificar se a condição é verdadeira, então repetirá o loop enquanto a condição for verdadeira.

**Sintaxe:**

```kotlin
do {
  // bloco de código a ser executado
}
while (condição);
```

O exemplo abaixo usa um loop `do/while`. O loop sempre será executado pelo menos uma vez, mesmo que a condição seja falsa, pois o bloco de código é executado antes que a condição seja testada.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>){
    var i = 0
    do {
        println(i)
        i++
    }
    while (i < 5) 
}
```

***Novamente, não esqueça de aumentar a variável usada na condição, caso contrário o loop nunca terminará!***

# break e continue

### break

A instrução `break` é usada para sair de um loop.

O exemplo abaixo sai do loop quando `i` é igual a 4:

```kotlin runnable
fun main(args: Array<String>){
    var i = 0
    while (i < 10) {
        println(i)
        i++
        if (i == 4) {
            break
        }
    }
}
```

### continue

A instrução `continue` interrompe uma iteração (no loop), se ocorrer uma condição especificada, e continua com a próxima iteração no loop.

O exemplo abaixo ignora o valor de 4:

```kotlin runnable
fun main(args: Array<String>){
    var i = 0
    while (i < 10) {
        if (i == 4) {
        i++
        continue
    }
    println(i)
    i++
    }
}
```

# for

Muitas vezes, quando você trabalha com arrays, precisa percorrer todos os elementos desse array.

Para percorrer os elementos do array, use o loop `for` junto com o operador `in`.

**Exemplo: Imprima todos os elementos no array cars:**

```kotlin runnable
fun main(args: Array<String>){
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    for (x in cars) {
        println(x)
    }
}
```

Você pode percorrer todos os tipos de matrizes. No exemplo acima, usamos um array de strings.

No exemplo abaixo, percorremos um array de inteiros:

```kotlin runnable
fun main(args: Array<String>){
    val nums = arrayOf(1, 5, 10, 15, 20)
    for (x in nums) {
        println(x)
    }
}
```

### Loop for tradicional

Ao contrário do Java e de outras linguagens de programação, não existe um loop `for` tradicional no Kotlin.

No Kotlin, o loop `for` é usado para percorrer arrays, intervalos e outras coisas que contêm um número contável de valores.


# Ranges (intervalos)

Com o loop `for`, você também pode criar intervalos de valores com "`..`".

**Exemplo:** *Imprima o alfabeto inteiro:*

```kotlin runnable
fun main(args: Array<String>){
    for (chars in 'a'..'x') {
       println(chars)
    }
}
```

