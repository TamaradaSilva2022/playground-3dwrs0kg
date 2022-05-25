# Arrays

Arrays são usados para armazenar vários valores em uma única variável, em vez de criar variáveis separadas para cada valor.

Para criar um array, use a função `arrayOf()` e coloque os valores em uma lista separada por vírgulas dentro dela.

```kotlin
val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
```

# Acesse os elementos de um array

Você pode acessar um elemento do array referindo-se ao **número do índice**, entre **colchetes**.

No exemplo abaixo, acessamos o valor do primeiro elemento em um array chamado `cars`:

```kotlin runnable
fun main(args: Array<String>) {
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    println(cars[0])
}
```

***Nota: Assim como com as Strings, os índices dos Arrays começam com 0: [0] é o primeiro elemento. [1] é o segundo elemento, etc.***

# Alterar um elemento de um array

Para alterar o valor de um elemento específico, consulte o número do índice.

**Exemplo:**

```kotlin
cars[0] = "Opel"
```

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    cars[0] = "Opel"
    println(cars[0]) 
}
```

# Comprimento / Tamanho de um array

Para descobrir quantos elementos um array possui, use a propriedade size.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    println(cars.size) 
}
```

# Verifique se existe um elemento no array

Você pode usar o operador `in` para verificar se existe um elemento em um array.

**Exemplo**

```kotlin runnable
fun main(args: Array<String>) {
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    if ("Volvo" in cars) {
        println("It exists!")
    } else {
        println("It does not exist.")
    }
}
```

# Loop através de um array

Muitas vezes, quando você trabalha com arrays, precisa percorrer todos os elementos dele.
Para isso, você pode percorrer os elementos do array com o loop `for`.

O exemplo a seguir imprime todos os elementos no array `cars`.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val cars = arrayOf("Volvo", "BMW", "Ford", "Mazda")
    for (x in cars) {
        println(x)
    }
}
```
