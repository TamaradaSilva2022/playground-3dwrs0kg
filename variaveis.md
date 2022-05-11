# Variáveis e constantes

Variáveis são contêineres para armazenar valores de dados.

Para criar uma variável, use `var` ou `val` e atribua um valor a ela com o sinal de igual `=`:

### Sintaxe

```kotlin
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

Ou seja, quando você cria uma variável com a palavra-chave `val`, o valor não pode ser alterado/reatribuído.

O exemplo a seguir irá gerar um erro:

```kotlin runnable
fun main(args: Array<String>) {
     /*Declaração da variável*/
    val name = "John"

    /*reatribuição do valor*/
    name = "Robert"  // Error (Val cannot be reassigned)
    
    /*Impressão da variável*/
    println(name)
}
```

Enquanto que ao usar `var`, você pode alterar o valor sempre que quiser:

```kotlin runnable
fun main(args: Array<String>) {
     /*Declaração da variável*/
    var name = "John"

    /*reatribuição do valor*/
    name = "Robert"  
    
    /*Impressão da variável*/
    println(name)
}
```

### Constantes

Além das variáveis, em Kotlin também existem constantes. 

Constantes são usadas para definir uma variável que tem um valor constante. 
A palavra-chave ``const`` é usada para definir uma variável constante. 
A palavra-chave ``const`` só pode ser usada com a palavra-chave ``val`` e não com a palavra-chave ``var``.

```kotlin
const val name = "John"
println(name) 
````

Se tentarmos declarar uma constante com a palavra-chave ``var``, obteremos uma mensagem de erro erro.

### Diferenças entre ``const``e ``val``

Ambas as palavras-chave ``val`` e ``const`` parecem estar fazendo o mesmo trabalho, ou seja, declarar variáveis constantes. 
Mas há uma pequena diferença entre elas. A palavra-chave ``const`` é usada para declarar constantes de tempo de compilação, 
enquanto a palavra-chave ``val`` pode declarar constantes em tempo de execução. Vamos entender com um exemplo:

Suponha que declaramos uma variável ``name`` e queremos atribuir a ela um valor, que será retornado por uma função ``sayHello()``. 
Se usarmos a palavra-chave ``val``, não teremos nenhum erro:
```kotlin runnable
fun main(args: Array<String>) {
    val name = sayHello()
    print(name)        
}

fun sayHello():String{
    return "Hello"
}
````

Mas, se declararmos esta variável com a palavra-chave ``const``, 
obteremos um erro porque o valor será atribuído a ``name`` em tempo de execução:

```kotlin runnable
fun main(args: Array<String>) {
    const val name = sayHello() 
    print(name) 
    }       

fun sayHello():String{
    return "Hello"
}
````
Portanto, a palavra-chave ``const`` só é usada para declarar variáveis cujos valores são conhecidos em tempo de compilação.

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

# Exibir variáveis

Como você viu nos exemplos acima, o método `println()` é frequentemente usado para exibir variáveis.

Para combinar texto e uma variável, use o caractere `+`:

```kotlin runnable
fun main(args: Array<String>) {
    val name = "John"
    println("Hello " + name)
}
```

Você também pode usar o caractere `+` para adicionar uma variável a outra variável:

```kotlin runnable
fun main(args: Array<String>) {
    val firstName = "John "
    val lastName = "Doe"
    val fullName = firstName + lastName
    println(fullName)
}
```

Para valores numéricos, o caractere `+` funciona como um operador matemático:

```kotlin runnable
fun main(args: Array<String>) {
    val x = 5
    val y = 6
    println(x + y) // Print the value of x + y 
}
```

A partir do exemplo acima, você pode notar que:

- x armazena o valor 5
- y armazena o valor 6
- Em seguida, usamos o método `println()` para exibir o valor de x + y, que é **11**

# Nomes das variáveis

Uma variável pode ter um nome curto (como x e y) ou nomes mais descritivos (idade, soma, volume total).

A regra geral para os nomes de variáveis em Kotlin é:

- Os nomes podem conter letras, números, _ e $
- Os nomes devem começar com uma letra
- Os nomes também podem começar com $ e _ (mas não o usaremos neste tutorial)
- Os nomes diferenciam maiúsculas de minúsculas ("myVar" e "myvar" são variáveis diferentes)
- Os nomes devem começar com uma letra minúscula e não podem conter espaços em branco
- Palavras reservadas (como as palavras-chave do Kotlin, como `var` ou `String`) não podem ser usadas como nomes

### Variáveis camelCase
Você pode notar que usamos **"firstName"** e **"lastName"** como nomes de variáveis nos exemplos acima, em vez de "firstname" e "lastname". 
Isso é chamado de "camelCase" e é considerado uma boa prática, 
pois facilita a leitura quando você tem um nome de variável com palavras diferentes, por exemplo, "myFavoriteFood", "rateActionMovies" etc.