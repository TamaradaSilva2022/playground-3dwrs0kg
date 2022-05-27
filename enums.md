# Enum

Ao desenvolver um aplicativo, pode surgir uma situação em que queremos que uma variável tenha um valor fora de um **determinado conjunto de valores permitidos**, por exemplo, se tivermos uma variável `pizzaSize`, ela deverá ter os seguintes valores: pequena, média e grande.

Em Kotlin, os Enums nos ajudam a conseguir isso.

Em Kotlin podemos criar uma **classe enum** com a ajuda da palavra-chave `enum`. As enums (ou enumerações) podem ter propriedades, funções, podem implementar interfaces, etc.

### Classe Enum

Vamos criar uma classe enum simples contendo tamanhos de pizza no exemplo a seguir.

**Exemplo:**

```kotlin runnable
enum class pizza{
    PEQUENA, MÉDIA, GRANDE
}

//Agora vamos usar este enum na main()função:

fun main() {
    val pizzaSize = pizza.LARGE
    println("O tamanho da pizza pedida é $pizzaSize")
}
```
 
Cada constante enum atua como um objeto separado. Eles são separados por vírgulas. No exemplo acima PEQUENA, MÉDIA e GRANDE são objetos.


### Enum: inicializando constantes

Nas enums podem ter construtores primários. Como constantes em enum são instâncias, elas podem ser inicializadas passando valores para o construtor.

```kotlin runnable
enum class pizza(val diameter: Int){
    SMALL(10),
    MEDIUM(12),
    LARGE(14)
}

// Vamos usar este enum na main()função:

fun main() {
    val pizzaSize = pizza.LARGE
    println("O tamanho da pizza pedida é $pizzaSize")
    println("O diâmetro da pizza GRANDE é ${pizzaSize.diameter}")
}
```


### Kotlin Enums: funções `values` e `valueOf`

Em Kotlin, temos duas funções em cada Enum por padrão. A função `values()` retorna uma matriz contendo todas as constantes da classe enum. Usando a função `valueOf(name: String)`, podemos obter a constante usando o valor da string para a constante enum.

**Exemplo:**

```kotlin runnable

enum class pizza(val diameter: Int){
    SMALL(10),
    MEDIUM(12),
    LARGE(14)
}

fun main() {
    for(pizza in pizza.values()){
        println(pizza)
    }
    val largePizza = pizza.valueOf("LARGE")
    println("Diameter: ${largePizza.diameter}")
}
```

No exemplo de código acima, usamos a função values() para obter todos os valores enum, depois usamos um loop for para iterar sobre os valores e, finalmente, usamos a função `valueOf` para obter a constante enum usando seu valor de string.
