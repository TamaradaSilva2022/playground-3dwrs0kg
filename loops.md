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

# continue

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

