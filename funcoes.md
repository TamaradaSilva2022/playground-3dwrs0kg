# Funções

Neste capítulo, discutiremos sobre as funções Kotlin, tanto as funções da biblioteca Kotlin quanto as funções definidas pelo usuário. As funções são usadas para quebrar um código monolítico enorme em pedaços de código menores que são reutilizáveis. Idealmente, devemos criar uma função para uma única tarefa. As funções também aumentam a reutilização do código, pois uma vez escrito, a função pode ser chamada várias vezes sempre que necessário.

As funções podem ser de dois tipos:

- Funções de biblioteca padrão (também chamadas de funções predefinidas)
- Funções definidas pelo usuário

# Funções predefinidas

As funções predefinidas são fornecidas pela biblioteca padrão Kotlin e podem ser usadas diretamente. Já usamos muitas funções de biblioteca padrão como: print(), println(), main(), arrayOf() etc. Você pode explorar mais sobre a biblioteca padrão Kotlin na documentação da linguagem [aqui](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.jvm/). Agora, veremos como criar funções definidas pelo usuário.

# Funções definidas pelo usuário

Como o nome sugere, as funções definidas pelo usuário são criadas pelos usuários. As funções no Kotlin são criadas usando a palavra-chave `fun`.

**Sintaxe**

```kotlin
fun <nome_da_função>(<nome_do_parâmetro>: <tipo_de_dados_do_argumento>):<tipo_do_returno>{
    // corpo da função
}
```

Na sintaxe:

- **<nome_da_função>**: É o nome dado à função.

- **<nome_do_parâmetro>**: representa o nome do parâmetro.

- **<tipo_de_dados_do_parâmetro>**: representa o tipo de dado do parâmetro.

- **<tipo_do_returno>**: representa o tipo de dado do valor retornado pela função.

# Chamando uma função

Para chamar uma função em Kotlin, escreva o nome da função seguido por dois parênteses ().

No exemplo a seguir, criaremos uma função chamada `elevaAoQuadrado()` e a chamaremos na `main()` para elevar um número ao quadrado quando for chamada:

```kotlin runnable
fun elevaAoQuadrado(numero: Int): Int {
    return numero * numero
}

fun main() {
    val quadradoDeNove = elevaAoQuadrado(9)
    println("O quadrado de 9 é: $quadradoDeNove")
}
```

# Parâmetros de função

Os dados podem ser passados para funções como parâmetro.

Os parâmetros são especificados após o nome da função, dentro dos parênteses. Você pode adicionar quantos parâmetros quiser, basta separá-los com uma vírgula. Apenas observe que você deve especificar o tipo de cada parâmetro (Int, String, etc).

O exemplo a seguir tem uma função que recebe uma String chamada `primeiroNome` como parâmetro. Quando a função é chamada, passamos um primeiro nome, que é usado dentro da função para imprimir o nome completo:

```kotlin runnable
fun minhaFuncao(primeiroNome: String) {
  println(primeiroNome + " Doe")
}

fun main() {
  minhaFuncao("João")
  minhaFuncao("Jane")
  minhaFuncao("Jorge")
}
```

Quando um parâmetro é passado para a função, ele é chamado de argumento. Então, do exemplo acima: `fname` é um parâmetro, enquanto "John", "Jane" e "George" são argumentos.

# Função com vários parâmetros

Você pode ter quantos parâmetros quiser nas funções que criar.

**Exemplo:**

```kotlin runnable
fun minhaFuncao(primeiroNome: String, idade: Int) {
  println(primeiroNome + " tem " + idade)
}

fun main() {
  minhaFuncao("João", 35)
  minhaFuncao("Jane", 32)
  minhaFuncao("Jorge", 15)
}
```

> Nota: Ao trabalhar com vários parâmetros, a chamada da função deve ter o mesmo número de argumentos que tem nos parâmetros e os argumentos devem ser passados na mesma ordem.

# Retornando valores

No exemplo acima, usamos funções para mostrar um valor na tela. No exemplo a seguir, usaremos uma função para retornar um valor e atribuí-lo a uma variável.

Para retornar um valor, use a palavra-chave `return` e especifique o tipo de retorno após os parênteses da função.

**Exemplo: Uma função com um parâmetro `Int` e tipo de retorno `Int`:**

```kotlin runnable
fun minhaFuncao(x: Int): Int {
  return (x + 5)
}

fun main() {
  var resultado = minhaFuncao(3)
  println(resultado)
}
```

O próximo exemplo usa dois parâmetros.

**Exemplo: Uma função com dois parâmetros `Int` e um retorno do tipo `Int`:**

```kotlin runnable
fun minhaFunção(x: Int, y: Int): Int {
  retorno (x + y)
}

divertido main() {
  var resultado = minhaFunção(3, 5)
  println(resultado)
}
```

# Sintaxe mais curta para valores de retorno

Há também uma sintaxe mais curta para retornar valores. Você pode usar o operador = em vez de return sem especificar o tipo de retorno. Kotlin é inteligente o suficiente para descobrir automaticamente o que é.

**Exemplo**

```kotlin runnable
fun minhaFunção(x: Int, y: Int) = x + y

fun main() {
  var resultado = minhaFunção(3, 5)
  println(resultado)
}
```

```
Fonte:
https://www.w3schools.com/kotlin/kotlin_functions.php
https://www.studytonight.com/kotlin/kotlin-userdefined-functions
```
