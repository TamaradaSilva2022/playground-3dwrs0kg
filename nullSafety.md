# Null Safety (segurança nula)

Neste capítulo vamos discutir sobre um dos recursos mais importantes do Kotlin: Null Safety. No mundo da programação, quando uma variável não se refere a nada, ela é considerada nula. Se tentarmos usar essa variável, obteremos `NullPointerException` ou *NPE*.

`NullPointerException` é considerado um [erro de bilhões de dólares](https://en.wikipedia.org/wiki/Tony_Hoare#Apologies_and_retractions), pois leva ao encerramento de um programa abruptamente. O `NullPointerException` pode ocorrer em qualquer lugar do código devido à negligência.

Kotlin aborda esse problema fornecendo um mecanismo para lidar com `NullPointerException`. Kotlin visa remover o NPE de todo o nosso código. Vamos discutir sobre a funcionalidade dada para ele.

# Referências anuláveis e não-anulável

Em Kotlin, o sistema de tipos diferencia dois tipos de referências:

- **Referência anulável**: esse tipo de referência pode conter valores nulos.

- **Referência não-anulável**: esse tipo de referência não pode conter valores nulos.

Essas referências são interpretadas pelo compilador em tempo de compilação. O compilador por padrão considera todas as variáveis como referência não-anuláveis.

**Exemplo:**

```kotlin runnable
fun main() {
    var name : String = null
}
```

Aqui, por padrão, o compilador considera a variável `name` como uma referência não nula. Portanto, não podemos atribuir `null` a ela. Assim, o compilador remove as chances de obter uma exceção de ponteiro nulo (`NullPointerException`) mais tarde quando usamos essa variável `name`.

Para permitir que uma variável também mantenha valores nulos usamos `?` após o tipo de dados da variável.

**Exemplo:**

```kotlin runnable
fun main() {
    var name:String? = null
}
```

Aqui nós deliberadamente permitimos que a variável `name` mantivesse valores nulos. Mas agora ela pode lançar uma exceção de ponteiro nulo quando tentarmos usá-la. O Kotlin também cuidará das referências anuláveis. Se tentarmos usá-lo como:

```kotlin runnable
fun main() {
    var name:String? = "Ninja"
    println(name.length) 
}
```

O compilador não nos permitirá encontrar o comprimento da String diretamente porque pode lançar uma exceção de ponteiro nulo.

Agora, para chamar as propriedades e funções em referências anuláveis, podemos fazer o seguinte:

1. Verificação de `null` nas condições

2. Chamadas seguras

3. O operador Elvis

4. O operador !!

Vamos discutir esses métodos em detalhes e ver como eles nos permitem usar referências anuláveis e também cuidar do NPE.

# Verificação de `null` nas condições

Se quisermos chamar uma função ou usar uma propriedade em uma referência anulável (como usar name.length na variável name), podemos verificar a condição nula primeiro e depois usá-la:

divertido main() {
    var nome:String? = "Ninja"
    if (nome != null)
        println(nome.comprimento)
}

5

Agora o compilador não dará nenhum erro, pois já verificamos a condição nula primeiro. É a maneira mais básica de lidar com referência anulável. Mas, ao mesmo tempo, é tedioso usá-lo em todos os lugares do programa.

Chamadas seguras
E se quisermos:

name.length para retornar o comprimento do nome, se o nome não for nulo.

Ou retorne nulo se o nome for nulo


Podemos conseguir isso usando um operador de chamada seguro (?.). Vamos usá-lo no mesmo exemplo:

divertido main() {
    var nome:String? = "Ninja"
    println("O comprimento do nome é ${nome?.comprimento}")

    nome = null
    println("O comprimento do nome é ${nome?.comprimento}")
}

O comprimento do nome é 5
O comprimento do nome é nulo

O operador de chamada segura é semelhante a:

if(nome != null)
    // retorna o comprimento
senão
    // retorna nulo
O Operador Elvis
O operador de chamada segura retornará nulo se a variável usada for nula. Suponha que queremos:

name.length para retornar o comprimento do nome se o nome não for nulo.

Ou dado um valor específico se o nome for nulo.

Podemos conseguir isso usando o operador Elvis (?:):

divertido main() {
    var nome:String? = "Ninja"
    println("O comprimento do nome é ${name?.length ?: -1}")

    nome = null
    println("O comprimento do nome é ${name?.length ?: -1}")
}

O comprimento do nome é 5
O comprimento do nome é -1

Aqui combinamos o operador de chamada segura e o operador elvis.

O !! operador
O !! O operador nos permite alterar uma referência anulável para uma referência não nula. Agora ele lançará uma exceção de ponteiro nulo se tentarmos usá-lo. O compilador Kotlin não cuidará mais disso.

Então, se tentarmos usá-lo neste caso:

divertido main() {
    var nome:String? = "Ninja"
    println("O comprimento do nome é ${nome!!.comprimento}") // imprime 5
}
Vai funcionar bem. Mas se tentarmos usá-lo neste caso:

divertido main() {
    var nome:String? = null
    println("O comprimento do nome é ${name!!.length}") // Lança NullPointerException
}
Então o !! operador deve ser evitado tanto quanto possível.
