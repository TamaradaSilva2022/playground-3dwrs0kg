# Funções Lambda

Funções ou expressões lambda não são novas no Kotlin e existem em muitas outras linguagens como Python, Java e Javascript.

A função Lambda é semelhante a uma função anônima. Uma função anônima é uma função que não tem um nome. Basicamente, a expressão Lambda é uma forma de criar funções de forma concisa e passá-las como argumento, retorná-las, etc. Podemos chamá-las como chamamos funções simples.

Uma expressão Lambda pode ser tratada como uma variável . Isso significa que podemos passá-lo como argumentos para funções , retorná-lo de funções etc.

Expressão Kotlin Lambda
A sintaxe da expressão lambda em Kotlin é:

val nameOfLambda : DataType = { argruments -> bodyOfLambdaFunction }
Em lambdas:

Os argumentos são mencionados no lado esquerdo de ->. O ->pode ser eliminado se nenhum argumento estiver presente à esquerda (veremos no Exemplo 1).

O corpo de lambda está presente depois ->e não pode estar vazio .


A última expressão de lambda é considerada como a instrução de retorno (veja o Exemplo 2).

Se nenhum valor for retornado ou o tipo de retorno não for mencionado, Unittype será considerado como tipo de retorno, como explicamos em Kotlin user-defined functions .

As funções lambda são chamadas usando o invoke()método ou apenas adicionando ()após o nome lambda (com argumentos).

Isso é bastante semelhante às funções de seta do Javascript .

Vamos dar alguns exemplos de código.

Expressão Kotlin Lambda - Exemplo 1:
Vamos começar criando um lambda simples que imprime uma string:

fun main() {
    // lambda expression with no argument
    val lambda = { println("Lambdas are awesome!")}
    // Calling lambda function using ()
    lambda()
    // Calling lambda function using invoke() function
    lambda.invoke()
}

Lambdas são incríveis! 
Lambdas são incríveis!

Neste exemplo, os argumentos e o tipo de retorno foram eliminados.


Expressão Kotlin Lambda - Exemplo 2:
Vamos criar outro exemplo para encontrar a área de um retângulo:

fun main() {
    val area = {length: Int, breadth: Int -> length*breadth} 
/*    
    This lambda is same as:
    fun area(length: Int, breadth: Int){
        return length*breadth
    }
*/
    println("Area of rectangle of dimension 4 and 5 is: ${area(4,5)}")
}

A área do retângulo de dimensão 4 e 5 é: 20

Aqui o tipo de retorno é automaticamente inferido como Int.

na expressão Kotlin Lambda
Se houver apenas um argumento presente na expressão lambda, ele poderá ser substituído pela palavra- itchave. É uma abreviação usada em Kotlin e muito útil. A itpalavra-chave representará o único argumento passado para a função lambda.

Vamos criar um array e imprimir quadrados dos elementos nele usando forEachloop:

fun main() {
    val array = arrayOf(10,2,3)
    // Long way
    array.forEach { num -> println(num * num) }
    // Shorthand
    array.forEach { println(it*it) }
}

100 
4 
9 
100 
4 
9

A itpalavra-chave se refere ao elemento atual quando usamos um loop forEach em um array.
