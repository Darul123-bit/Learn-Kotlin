# HELLO WORLD

Voici un programme simple qui affiche "Hello, Magnus!":


```kotlin

    fun main() {
        println("Hello, Magnus!")
    }
```
En Kotlin :

* `fun` est utilisé pour déclarer une fonction
* La fonction `main()` est le point de départ de votre programme
* Le corps d'une fonction est écrit entre accolades `{}`
* Les fonctions [`println()`](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin.io/println.html) et [`print()`]() affichent leurs arguments sur la sortie standard

Une fonction est un ensemble d'instructions qui exécute une tâche spécifique. Une fois créée, vous pouvez utiliser cette fonction dès que vous devez accomplir cette tâche, sans avoir à réécrire toutes les instructions. Les fonctions sont abordées plus en détail dans les chapitres suivants. D'ici là, tous les exemples utiliseront la fonction `main()`.

**Variables**

Tous les programmes doivent pouvoir stocker des données, et les variables permettent de le faire. En Kotlin, vous pouvez déclarer :

* Des variables en lecture seule avec `val`
* Des variables mutables avec `var`

> Vous ne pouvez pas modifier une variable en lecture seule une fois qu'une valeur lui a été attribuée.

Pour attribuer une valeur, utilisez l'opérateur d'affectation `=`.

Par exemple :

```kotlin
fun main() {
    val popcorn = 5     // Il y a 5 boîtes de popcorn
    val hotdog = 7      // Il y a 7 hot-dogs
    var customers = 10  // Il y a 10 clients dans la file d'attente

    // Certains clients quittent la file d'attente
    customers = 8
    println(customers)
    // 8
}
```

> Les variables peuvent être déclarées en dehors de la fonction `main()` au début de votre programme. Les variables déclarées de cette manière sont dites déclarées au **niveau supérieur** *`top level`*.

Comme `customers` est une variable mutable, sa valeur peut être réassignée après sa déclaration.

> Nous vous recommandons de déclarer toutes les variables en lecture seule (`val`) par défaut. N'utilisez des variables mutables (`var`) que si vous en avez réellement besoin. De cette façon, vous risquez moins de modifier accidentellement une valeur qui n'était pas censée changer.



### **String templates**

Il est utile de savoir comment afficher le contenu des variables sur la sortie standard. Vous pouvez le faire grâce aux **string templates** (modèles de chaînes). 

Vous pouvez utiliser des expressions de modèle pour accéder aux données stockées dans des variables et d'autres objets, puis les convertir en chaînes de caractères. Une valeur de chaîne est une séquence de caractères entre guillemets doubles `"`. Les expressions de modèle commencent toujours par le symbole dollar `$`.

Pour évaluer un morceau de code dans une expression de modèle, placez le code entre accolades `{}` après le symbole dollar `$`.

Par exemple :

```kotlin
fun main() {
    val customers = 10
    println("There are $customers customers")
    // There are 10 customers

    println("There are ${customers + 1} customers")
    // There are 11 customers
}
```

Pour plus d'informations, consultez la documentation sur les [String templates.]()

Vous remarquerez qu'aucun type n'a été explicitement déclaré pour les variables. Kotlin a inféré le type lui-même : `Int`. Ce parcours détaille les différents types de base de Kotlin et leur déclaration dans le [chapitre suivant](02-basic-types/README.md).

## Practice

### Exercise

Complétez le code pour que le programme affiche `"Mary is 20 years old"` sur la sortie standard :

```kotlin
fun main() {
    val name = "Mary"
    val age = 20
    // Écrivez votre code ici
}
```

```kotlin
fun main() {
    val name = "Mary"
    val age = 20
    println("$name is $age years old")
}
```
[Prochaine étape](../02-basic-types/README.md)
