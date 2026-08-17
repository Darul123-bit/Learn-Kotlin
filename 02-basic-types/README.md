# Types de base

Chaque variable et structure de données en Kotlin possède un type. Les types sont importants car ils indiquent au compilateur ce que vous êtes autorisé à faire avec cette variable ou cette structure de données — autrement dit, les fonctions et propriétés dont elle dispose.

Dans le chapitre précédent, Kotlin a pu déterminer dans l'exemple précédent que `customers` était de type `Int`. La capacité de Kotlin à **déduire** le type s'appelle l'**inférence de type** (*type inference*). Une valeur entière étant assignée à `customers`, Kotlin en déduit que `customers` a un type numérique `Int`. Par conséquent, le compilateur sait que vous pouvez effectuer des opérations arithmétiques avec `customers` :

```kotlin
fun main() {
    var customers = 10

    // Certains clients quittent la file d'attente
    customers = 8

    customers = customers + 3 // Exemple d'addition : 11
    customers += 7            // Exemple d'addition : 18
    customers -= 3            // Exemple de soustraction : 15
    customers *= 2            // Exemple de multiplication : 30
    customers /= 3            // Exemple de division : 10

    println(customers) // 10
}
```

> `+=`, `-=`, `*=`, `/=`, et `%=` sont des opérateurs d'affectation augmentée (*augmented assignment operators*). Pour plus d'informations, consultez la documentation sur les [Augmented assignments](https://kotlinlang.org/docs/operator-overloading.html#augmented-assignments).

Au total, Kotlin possède les types de base suivants :

| Catégorie | Types de base | Exemple de code |
| --- | --- | --- |
| [Entiers](https://kotlinlang.org/docs/numbers.html#integer-types) | `Byte`, `Short`, `Int`, `Long` | `val year: Int = 2020`<br>`val amount: Long = 350_000_000` |
| [Entiers non signés](https://kotlinlang.org/docs/numbers.html#unsigned-integers) | `UByte`, `UShort`, `UInt`, `ULong` | `val score: UInt = 100u` |
| [Nombres à virgule flottante](https://kotlinlang.org/docs/numbers.html#floating-point-types) | `Float`, `Double` | `val currentTemp: Float = 24.5f`<br>`val price: Double = 19.99` |
| [Booléens](https://kotlinlang.org/docs/booleans.html) | `Boolean` | `val isEnabled: Boolean = true` |
