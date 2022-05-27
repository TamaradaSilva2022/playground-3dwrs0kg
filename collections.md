# Collections (coleções)

Neste capítulo, apresentaremos uma breve introdução às coleções (collections) em Kotlin. 
O conceito de coleções não é uma novidade do Kotlin, esse conceito já está presente em muitas outras linguagens de programação. 
A biblioteca padrão Kotlin fornece um conjunto de ferramentas para criar e gerenciar coleções.

### O que são coleções?

Uma coleção (collection) é um grupo de objetos do mesmo tipo. 
Os objetos dentro de uma coleção são conhecidos como elementos ou itens.

### Tipos de coleções

Existem três tipos de coleções em Kotlin:

1. Listas
2. Set
3. Map

A biblioteca padrão Kotlin fornece métodos para criar os objetos de list (lista), set e map. 
De acordo com o requisito, cada um deles pode ser uma:

1. Coleção imutável (somente leitura)
2. Coleção Mutável (tanto leitura quanto escrita)

### Coleção imutável

Coleções imutáveis são herdadas da interface `Collection<T>` que não fornece funcionalidade para adicionar ou remover elementos. 
Em coleções imutáveis, um elemento não pode ser adicionado , removido ou alterado após a declaração. 
Após definir a coleção imutável, podemos apenas ler seus elementos.

A coleção imutável é simplesmente conhecida como coleção também.

### Coleção Mutável

Como o nome sugere, as coleções mutáveis permitem operações de escrita e leitura. 
Em coleções mutáveis podemos adicionar, remover e alterar os valores dos elementos.

As coleções mutáveis são herdadas da interface `MutableCollection<T>` que fornece funcionalidade para ler e alterar elementos. 
Elas também herdam funcionalidades básicas das interfaces de coleção correspondentes.

# Listas

Listas (lists) são:

- Uma coleção ordenada de elementos.
- A ordem é mantida através de índices (como acontece com os arrays).
- Um elemento pode ocorrer mais de uma vez em uma lista.
- A lista mutável pode ser considerada um array dinâmico cujo tamanho pode ser alterado.

Em Kotlin podemos ter uma lista mutável e uma lista imutável.

### Lista imutável

Listas imutáveis são criadas usando a interface `List`. A interface `List` herda a interface `Collection<T>`. 
Ela contém muitas funções úteis como `contains()`, `indexOf()`, `isEmpty()`, etc. 

Em Kotlin, podemos criar uma lista imutável usando funções `listOf()` e `listOf<T>()`. 
A função `listOf()` é usada para criar uma lista geral que pode ter qualquer objeto como Integers, Strings, Floats etc. 
A função `listOf<T>()` é usada para criar uma lista de tipo específico.

Vamos criar uma lista usando essas duas funções no exemplo abaixo.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var genericList = listOf("Ninja", 10, 1.05f, 'a')
    var specificList = listOf<String>("Ninja", "Study", "tonight")
    println("Imprimindo $genericList")
    println("Imprimindo $specificList")
}
```

No exemplo anterior criamos duas listas: uma de tipo genérico e outra de Strings.

### Percorrer uma lista:

Para percorrer uma lista podemos utilizar o `for`, como no exemplo abaixo.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val list = listOf<String>("Ninja", "Study", "tonight", "Ninja", "Kotlin")
    // printing list
    for (element in list)
        println(element)
}
```

### Funções e propriedades da lista

Algumas funções e propriedades importantes fornecidas na interface `List` são:

**Propriedades:**

- `size`: representa o número de elementos presentes na lista.
- `lastIndex`: representa o índice do último elemento da lista.

**Funções:**

- `get(index)`: Retorna o elemento no índice especificado na lista ou lança `IndexOutOfBoundsException`.
- `contains(element)`: Retorna verdadeiro se o elemento existir na lista ou retorna falso.
- `indexOf(element)`: Retorna o índice da primeira ocorrência do elemento especificado na lista, ou -1 se o elemento especificado não estiver contido na lista.
- `lastIndexOf(element)`: Retorna o índice da última ocorrência do elemento especificado na lista, ou -1 se o elemento especificado não estiver contido na lista.
- `first()`: Retorna o primeiro elemento na lista ou lança `NoSuchElementException` se a lista estiver vazia.
- `last()`: Retorna o último elemento da lista ou lança `NoSuchElementException` se a lista estiver vazia.
- `isEmpty()`: Retorna verdadeiro se a lista estiver vazia, senão falso.
- `subList(start, end)`: Retorna uma sublista entre o início (inclusivo) e o final (exclusivo).

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val list = listOf<String>("Ninja", "Study", "tonight", "Ninja", "Kotlin")
    // Propriedades
    println("O tamanho da lista é: ${list.size}")
    println("O índice do último elemento é: ${list.lastIndex}")

    // Funções
    println("O elemento no índice 2 é: ${list.get(2)}")
    println("O elemento no índice 3 é: ${list[3]}")     // Other way to get an element

    println("Ninja existe na lista? ${list.contains("Ninja")}")
    println("Existe Hatori na lista? ${list.contains("Hatori")}")

    println("O primeiro índice de Ninja é: ${list.indexOf("Ninja")}")
    println("O primeiro índice de Hatori é: ${list.indexOf("Hatori")}")

    println("O último índice de Ninja é: ${list.lastIndexOf("Ninja")}")
    println("O último índice de Hatori é: ${list.lastIndexOf("Hatori")}")

    println("Primeiro elemento da lista: ${list.first()}")
    println("Último elemento da lista: ${list.last()}")

    println("A lista está vazia? ${list.isEmpty()}")

    println("Sublista do índice 1 a 3 ${list.subList(1,3)}")

}
```

### Lista Mutável

As listas mutáveis são criadas usando a interface `MutableList`. A interface `MutableList` também herda a interface `Collection`. 
As listas mutáveis são dinâmicas por natureza. Podemos adicionar ou remover elementos da lista mutável após sua declaração. 
Portanto, o tamanho da lista mutável não é fixo.

Semelhante às listas imutáveis, as listas mutáveis são criadas usando as funções `mutableListOf()` e `mutableListOf<T>()`. 
A função `mutableListOf()` é usada para criar uma lista geral que pode ter qualquer objeto como Integers, Strings, Floats etc. 
A função `mutableListOf<T>()` é usada para criar uma lista de tipo específico.

Vamos criar listas mutáveis usando estes métodos no exemplo abaixo.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    var genericList = mutableListOf("Ninja", 10, 1.05f, 'a')
    var specificList = mutableListOf<String>("Ninja", "Study", "tonight")
    println("Imprimindo $genericList")
    println("Imprimindo $specificList")
}
```

Todas as propriedades e métodos que estão presentes em listas imutáveis também estão presentes nas listas mutáveis, mas as listas mutáveis têm algumas funções extras para suportar a mutabilidade:

- `add(element)`: Adiciona o elemento especificado ao final da lista.
- `add(index, element)`: Insere um elemento na lista no índice especificado.
- `remove(element)`: Remove a primeira ocorrência do elemento da lista.
- `removeAt(index)`: Remove um elemento no índice especificado da lista.
- `set(index, element)`: Substitui o elemento no índice especificado nesta lista pelo elemento especificado.
- `clear()`: remove todos os elementos da lista.

**Exemplo usando estes métodos:**

```kotlin runnable
fun main(args: Array<String>) {
    val list = mutableListOf<String>("Ninja", "Study", "tonight", "Ninja", "Kotlin")
    // New Functions
    list.add("Java")
    println(list)
    list.add(2, "C++")
    println(list)
    list.remove("Ninja")
    println(list)
    list.removeAt(1)
    println(list)
    list.set(1, "PHP")
    println(list)
    list.clear()
    println(list)
}
```

# Set

Sets (ou conjuntos) são:

- Uma coleção desordenada de elementos.
- Elementos duplicados não são permitidos nos sets.

Em Kotlin podemos ter um set (conjunto) mutável e um set (conjunto) imutável.

### Set imutável Kotlin

Sets imutáveis são criados usando a interface `Set`. A interface `Set` herda a interface `Collection`.

Em Kotlin, podemos criar sets imutáveis usando as funções `setOf()` e `setOf<T>()`. 
A função `setOf()` é usada para criar um set geral que pode ter qualquer objeto como Integers, Strings, Floats etc. 
A função `setOf<T>()` é usada para criar um set de tipo específico.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val genericSet = setOf("Hello", 1, "Bye", 'A', "Hello")
    val specificSet = setOf<String>("C++", "Maths", "English")
    println(genericSet)
    println(specificSet)
}
```

No exemplo anterior criamos dois sets: um de tipo genérico e outro de strings.

Para percorrer um set podemos utilizar um `for`, como no exemplo a seguir.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val genericSet = setOf("Hello", 1, "Bye", 'A', "Hello")
    for (item in genericSet)
        println(item)
}
```

### Propriedades e funções dos sets

Algumas funções e propriedades importantes fornecidas na interface `Set` são:

**Propriedades:**

- `size`: representa o número de elementos presentes no conjunto.

Funções :

- `elementAt(index)`: Retorna o elemento no índice especificado no set ou lança `IndexOutOfBoundsException`.
- `contains(element)`: Retorna `true` se o elemento existe no set ou retorna `false`.
- `indexOf(element)`: Retorna o índice do elemento especificado no set, ou -1 se o elemento especificado não estiver presente no set.
- `lastIndexOf(element)`: Retorna o índice da última ocorrência (ou a única ocorrência) do elemento especificado no set, ou -1 se o elemento especificado não estiver presente no set.
- `first()`: Retorna o primeiro elemento no set ou lança `NoSuchElementException` se o set estiver vazio.
- `last()`: Retorna o último elemento do set ou lança `NoSuchElementException` se o set estiver vazio.
- `isEmpty()`: Retorna `true` se o set estiver vazio, se não estiver retorna `false`.
- `count()`: Retorna o número de elementos nesta coleção.
- `max()`: Retorna o maior elemento ou `null` se não houver elementos.
- `min()`: Retorna o menor elemento ou `null` se não houver elementos.
- `sum()`: Retorna a soma de todos os elementos desta coleção.
- `average()`: Retorna a média de todos os elementos nesta coleção.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val languages = setOf<String>("Kotlin", "C++", "C", "Java", "Angular", "Kotlin")
    val marks = setOf<Int>(95,96,94,90)

    // Propriedades
    println("O tamanho do set é: ${languages.size}")

    // Funções
    println("Java existe no set? ${languages.contains("Java")}")
    println("PHP existe no set? ${languages.contains("PHP")}")
    println("Elemento no índice 1: ${languages.elementAt(1)}")

    println("O índice do Kotlin é: ${languages.indexOf("Kotlin")}")
    println("O índice do PHP é: ${languages.indexOf("PHP")}")

    println("O último índice do Kotlin é: ${languages.lastIndexOf("Kotlin")}")

    println("Primeiro elemento no set: ${languages.first()}")
    println("Último elemento no set: ${languages.last()}")

    println("O set está vazio? ${languages.isEmpty()}")

    // Funções matemáticas
    println("Número de elementos no set: ${marks.count()}")
    println("Maior elemento no set: ${marks.max()}")
    println("Menor elemento no set: ${marks.min()}")
    println("Soma dos elementos no set: ${marks.sum()}")
    println("Média de elementos no set: ${marks.average()}")
}
```

### Set Mutável

Sets mutáveis são criados usando a interface `MutableSet`. A interface `MutableSet` também herda a interface `Collection`. 
Sets mutáveis são dinâmicos por natureza. Podemos adicionar ou remover elementos do set mutável após sua declaração. 
Portanto, o tamanho do set mutável não é fixo.

Semelhante aos sets imutáveis, os sets mutáveis são criados usando as funções `mutableSetOf()` e `mutableSetOf<T>()`. 
A função `mutableSetOf()` é usada para criar um set geral enquanto `mutableSetOf<T>()` é usada para criar um set de tipo específico.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val generalSet = mutableSetOf("Kotlin", 10, 1.0f, 'A', "Kotlin")
    val specificSet = mutableSetOf<String>("Kotlin", "C++", "C", "Java", "Angular", "Kotlin")
    println(generalSet)
    println(specificSet)
}
```

Todas as propriedades e métodos que estão presentes em sets imutáveis também estão presentes no caso de sets mutáveis, mas os sets mutáveis têm algumas funções extras para suportar a mutabilidade:

- `add(element)`: Adiciona o elemento especificado ao set. Retorna `true` se o elemento foi adicionado, `false` se o elemento já está contido no set.
- `remove(element)`: Remove o elemento do set.
- `clear()`: Remove todos os elementos do set.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val languages = mutableSetOf<String>("Kotlin", "C++", "C", "Java", "Kotlin")
    println(languages)
    languages.add("Angular")
    println(languages)
    languages.remove("Java")
    println(languages)
    languages.clear()
    println(languages)
}
```

# Map

Os maps são usados para armazenar pares de chave e valor. Tanto a chave quanto o valor são definidos pelo usuário. Em um map:

- A chave deve ser exclusiva e apenas um valor pode ser armazenado para cada chave exclusiva.
- Os valores podem ser duplicados.
- A chave e o valor podem ser de tipos de dados diferentes.
- A palavra-chave `to` é usada para mapear uma chave para um valor.
- Um par chave-valor também é conhecido como uma entrada.

Em Kotlin podemos ter um map mutável e um map imutável.

### Map imutável Kotlin

Maps imutáveis são criados usando a interface `Map<K, V>`. A partir de maps imutáveis, só podemos fazer leitura.

Em Kotlin, maps imutáveis são criados usando funções `mapOf()` e `mapOf<K, V>()`. Semelhante às listas, a função `mapOf()` é usada para criar um map geral onde a chave e o valor podem ser de qualquer tipo de dados. 
O `mapOf<K, V>()` é usado para criar um mapa específico com chaves e valores dos tipos de dados K e V, respectivamente.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val generalMap = mapOf("Rank" to 1, 1 to "Primeiro", 'A' to "Excelente")
    val specificMap = mapOf<String, Int>("Física" to 80, "Matemática" to 97, "C++" to 89)
    println(generalMap)
    println(specificMap)
}
```

É possível percorrer esses maps usando `for` e `forEach`:

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val generalMap = mapOf("Rank" to 1, 1 to "Primeiro", 'A' to "Excelente")
    val specificMap = mapOf<String, Int>("Física" to 80, "Matemática" to 97, "C++" to 89)
    for ((k,v) in generalMap) {
        println("A Chave é $k e o Valor é $v")
    }
    specificMap.forEach { (k, v) ->
        println("A chave é $k e o Valor é $v")
    }
}
```

### Propriedades e funções do map

Algumas funções e propriedades importantes fornecidas na interface Map são:

**Propriedades:**

- `size`: Retorna o tamanho do map.
- `entries`: retorna o conjunto de todos os pares de chave-valor no map.
- `keys`: Retorna o conjunto de todas as chaves no map.
- `values`: Retorna o conjunto de todos os valores no map.

**Funções:**

- `get(key)`: Retorna o valor da chave correspondente. Se a chave estiver ausente, retornará `null`.
- `getValue(key)`: Retorna o valor para a chave fornecida ou lança `NoSuchElementException` se não houver tal chave no map.
- `contains(key)`: Retorna `true` se o map contiver a chave especificada senão retorna `false`.
- `containsKey(key)`: Retorna `true` se o map contiver a chave especificada senão retorna `false`. Esta função é a mesma que a anterior.
- `containsValue(value)`: Retorna `true` se houver uma ou mais chaves para o valor especificado presente no map.
- `getOrDefault(key, defaultValue)`: Retorna o valor correspondente à chave, ou `defaultValue` se tal chave não estiver presente no map.

**Exemplo:**

```kotlin runnable
package collections

fun main(args: Array<String>) {
    val marks = mapOf<String, Int>("Física" to 80, "Matemática" to 97, "C++" to 89, "Química" to 95)
    
    // Propriedades
    println("Tamanho do map: ${marks.size}")
    println("Conjunto de entradas: ${marks.entries}")
    println("Conjunto de chaves: ${marks.keys}")
    println("Conjunto de valores: ${marks.values}")

    // Funções
    println("Notas em Física: ${marks.get("Physics")}")
    println("Notas em Inglês: ${marks["English"]}")
    println("Notas em Matemática: ${marks.getValue("Maths")}")

    println("O map contém Física? ${marks.containsKey("Physics")}")
    println("O map contém C++? ${marks.contains("C++")}")
    println("O map contém Química? ${"Chemistry" in marks}")

    println("Alguma matéria tem notas 100? ${marks.containsValue(100)}")

    println("Notas em inglês: ${marks.getOrDefault("English",0)}")
}
```

### Map Mutável

Os maps mutáveis são criados usando a interface `MutableMap`. Os maps mutáveis suportam a natureza dinâmica. 
Podemos adicionar ou remover ou atualizar entradas do map mutável após sua declaração. Portanto, o tamanho do map mutável não é fixo.


Maps mutáveis são criados usando funções `mutableMapOf()` e `mutableMapOf<K, V>()`. 
A função `mutableMapOf()` é usada para criar um mapa generalizado e a `mutableMapOf<K, V>()` é usada para criar um map de chave e valor de tipos específicos.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val generalMap = mutableMapOf("Rank" to 1, 1 to "Primeiro", 'A' to "Excelente")
    val specificMap = mutableMapOf<String, Int>("Física" to 80, "Matemática" to 97, "C++" to 89)
    println(generalMap)
    println(specificMap)
}
```

Podemos percorrer maps mutáveis da mesma forma que percorremos maps imutáveis.

Todas as propriedades e funções que estão presentes em maps imutáveis também estão presentes no caso de maps mutáveis. 
Os maps mutáveis têm algumas funções extras para suportar a natureza dinâmica. Elas são:

- `put(key, value)`: adiciona o par chave-valor especificado ao map. Se a chave já existir, o valor desse novo par substituirá o valor antigo.
- `putIfAbsent(key, value)`: adiciona o par chave-valor especificado ao map somente se a chave não existir anteriormente.
- `replace(key, newValue)`: Substitui o valor da chave especificada pelo novo valor.
- `replace(key, oldValue, newValue)`: substitui o valor antigo pelo novo valor para a chave especificada somente se o par key e oldValue existir.
- `remove(key)`: Remove a entrada com a chave especificada do map.
- `remove(key, value)`: Remove a entrada do map se existir uma entrada com a chave e o valor especificados.
- `clear()`: remove todas as entradas do map.

**Exemplo:**

```kotlin runnable
fun main(args: Array<String>) {
    val marks = mutableMapOf<String, Int>("Física" to 80, "Matemática" to 97, "C++" to 89, "Química" to 95)

    marks.put("C++", 92)
    println(marks)
    marks["Química"] = 93
    println(marks)
    marks.putIfAbsent("Inglês", 95)
    marks.putIfAbsent("Física", 0)
    println(marks)
    marks.replace("Matemática", 70)
    println(marks)
    marks.replace("Matemática", 70, 95)
    println(marks)
    marks.remove("C++")
    println(marks)
    marks.remove("Matemática", 95)
    println(marks)
    marks.clear()
    println(marks)
}
```