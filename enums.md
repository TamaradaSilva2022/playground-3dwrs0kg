# Enum

Enum é um tipo de dados que consiste em um conjunto de constantes. Em Kotlin podemos criar uma **classe enum** com a ajuda da palavra-chave `enum`. 
As enums (ou enumerações) podem ter propriedades, funções, podem implementar interfaces, etc.

### Classe Enum

Vamos criar uma classe enum simples contendo tamanhos de pizza no exemplo a seguir.

**Exemplo:**

```kotlin runnable
enum class pizza{
    PEQUENA, MÉDIA, GRANDE
}

//Agora vamos usar este enum na main()função:

fun main(args: Array<String>) {
    val pizzaSize = pizza.LARGE
    println("O tamanho da pizza pedida é $pizzaSize")
}
```
 
Cada constante enum atua como um objeto separado. Eles são separados por vírgulas. No exemplo acima PEQUENA, MÉDIA e GRANDE são objetos.


### Enum: inicializando constantes

Nas enums podem ter construtores primários. Como constantes em enum são instâncias, elas podem ser inicializadas passando valores para o construtor.

```kotlin runnable
enum class pizza(val diameter: Int){
    PEQUENO(10),
    MEDIO(12),
    GRANDE(14)
}

// Vamos usar este enum na main()função:

fun main(args: Array<String>) {
    val pizzaSize = pizza.GRANDE
    println("O tamanho da pizza pedida é $pizzaSize")
    println("O diâmetro da pizza GRANDE é ${pizzaSize.diameter}")
}
```


### Kotlin Enums: funções `values` e `valueOf`

Em Kotlin, temos duas funções em cada Enum por padrão. A função `values()` retorna uma matriz contendo todas as constantes da classe enum. Usando a função `valueOf(name: String)`, podemos obter a constante usando o valor da string para a constante enum.

**Exemplo:**

```kotlin runnable

enum class pizza(val diameter: Int){
    PEQUENO(10),
    MEDIO(12),
    GRANDE(14)
}

fun main(args: Array<String>) {
    for(pizza in pizza.values()){
        println(pizza)
    }
    val largePizza = pizza.valueOf("GRANDE")
    println("Diameter: ${largePizza.diameter}")
}
```

No exemplo de código acima, usamos a função values() para obter todos os valores enum, depois usamos um loop for para iterar sobre os valores e, finalmente, usamos a função `valueOf` para obter a constante enum usando seu valor de string.
