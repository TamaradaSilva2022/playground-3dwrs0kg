# Funções Lambda

Funções lambda não são novas no Kotlin e existem em muitas outras linguagens como Python, Java e Javascript.

A função Lambda é semelhante a uma função anônima. Uma função anônima é uma função que não tem um nome. Basicamente, a função Lambda é uma forma de criar funções de forma concisa e passá-las como argumento, retorná-las, etc. Podemos chamá-las como chamamos funções simples.

Uma função Lambda pode ser tratada como uma variável. Isso significa que podemos passá-lo como argumentos para funções , retorná-la de funções etc.

# funçaõ Lambda em Kotlin

A sintaxe da função lambda em Kotlin é:

```kotlin
val nomeDaLambda : TipoDeDados = { argrumentos -> corpodaFunçãoLambda }
```

Nas função lambdas:

- Os argumentos são mencionados no lado esquerdo da `->`. A `->` pode ser eliminada se nenhum argumento estiver presente à esquerda.
- O corpo da função lambda está presente depois da `->` e não pode estar vazio.
- A última expressão de lambda é considerada como a instrução de retorno.
- Se nenhum valor for retornado ou o tipo de retorno não for mencionado, o tipo `Unit` será considerado como tipo de retorno.
- As funções lambda são chamadas usando o método `invoke()` ou apenas adicionando `()` após o nome lambda (com argumentos).

Isso é bastante semelhante às arrow functions do Javascript.

Vamos dar alguns exemplos de código.

**Exemplo 1: Vamos começar criando um lambda simples que imprime uma string:**

```kotlin runnable
fun main() {
    // função lambda sem argumento
    val lambda = { println("Lambdas são incríveis!")}
    
    // Chamando a função lambda usando ()
    lambda()
    
    // Chamando a função lambda usando a função invoke()
    lambda.invoke()
}
```

No Exemplo 1, os argumentos e o tipo de retorno foram eliminados.


**Exemplo 2: Vamos criar outro exemplo, dessa vez para encontrar a área de um retângulo:**

```kotlin runnable
fun main() {
    val area = {altura: Int, largura: Int -> altura*largura} 
/*    
    Esta lambda é o mesmo que:
    fun area(altura: Int, largura: Int){
        return altura*largura
    }
*/
    println("A área do retângulo de dimensão 4 e 5 é: ${area(4,5)}")
}
```

No Exemplo 2 o tipo de retorno é automaticamente inferido como `Int`.

# `it` na função Lambda

Se houver apenas um argumento presente na função lambda, ele poderá ser substituído pela palavra-chave `it`. Essa é uma abreviação usada em Kotlin e é muito útil. A palavra-chave `it` representará o único argumento passado para a função lambda.

Vamos criar um array e imprimir os quadrados dos números nele usando `forEach`:

```kotlin runnable
fun main() {
    val array = arrayOf(10,2,3)
    
    // Forma longa
    array.forEach { num -> println(num * num) }
    
    // Forma curta
    array.forEach { println(it*it) }
}
```

A palavra-chave `it` se refere ao elemento atual quando usamos um loop `forEach` em um array.
