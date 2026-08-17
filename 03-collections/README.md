# Collections

En programmation, il est utile de pouvoir regrouper des données dans des structures pour les traiter plus tard. Kotlin fournit des collections exactement à cet effet.

Kotlin dispose des collections suivantes pour regrouper des éléments :

| Type de collection | Description |
| --- | --- |
| **Lists** | Collections ordonnées d'éléments |
| **Sets** | Collections non ordonnées d'éléments uniques |
| **Maps** | Ensembles de paires clé-valeur où les clés sont uniques et ne s'associent qu'à une seule valeur |

Chaque type de collection peut être mutable ou en lecture seule.

---

## List

Les listes stockent les éléments dans l'ordre dans lequel ils sont ajoutés et autorisent les doublons.

Pour créer une liste en lecture seule (`List`), utilisez la fonction [`listOf()`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/list-of.html).

Pour créer une liste mutable (`MutableList`), utilisez la fonction [`mutableListOf()`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/mutable-list-of.html).

Lors de la création de listes, Kotlin peut inférer le type des éléments stockés. Pour déclarer le type explicitement, ajoutez le type entre chevrons `<>` après la déclaration de la liste :

```kotlin
fun main() {
    // Liste en lecture seule
    val readOnlyShapes = listOf("triangle", "square", "circle")
    println(readOnlyShapes)
    // [triangle, square, circle]

    // Liste mutable avec déclaration explicite du type
    val shapes: MutableList<String> = mutableListOf("triangle", "square", "circle")
    println(shapes)
    // [triangle, square, circle]
}
```


> Pour éviter les modifications indésirables, vous pouvez créer une vue en lecture seule d'une liste mutable en l'assignant à une `List` :
>
> ```kotlin
> val shapes: MutableList<String> = mutableListOf("triangle", "square", "circle")
> val shapesLocked: List<String> = shapes
> ```
>
> Ceci est également appelé le **transtypage** (*casting*).

Les listes étant ordonnées, pour accéder à un élément d'une liste, utilisez l'opérateur d'accès indexé (*indexed access operator*) `[]` :

```kotlin
fun main() {
    val readOnlyShapes = listOf("triangle", "square", "circle")
    println("The first item in the list is: ${readOnlyShapes[0]}")
    // The first item in the list is: triangle
}
```
Pour obtenir le premier ou le dernier élément d'une liste, utilisez respectivement les fonctions `.first()` et `.last()` :


```kotlin
fun main() {
    val readOnlyShapes = listOf("triangle", "square", "circle")
    println("The first item in the list is: ${readOnlyShapes.first()}")
    // The first item in the list is: triangle
}
```

>Les fonctions `.first()` et `.last()` sont des exemples de fonctions d'extension. Pour appeler une fonction d'extension sur un objet, écrivez le nom de la fonction après l'objet, séparé par un point ..
Les fonctions d'extension sont abordées en détail dans le parcours intermédiaire. Pour l'instant, vous avez seulement besoin de savoir comment les appeler`.`
