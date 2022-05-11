# Variáveis Kotlin
Variáveis são contêineres para armazenar valores de dados.

Para criar uma variável, use `var` ou `val` e atribua um valor a ela com o sinal de igual `=`:

### Sintaxe
```
var variableName = value
val variableName = value
```

### Exemplo
```kotlin runnable
fun main(String[] args) {
  var name = "John"
  val birthyear = 1975
  
  println(name)
  println(birthyear)
}
```