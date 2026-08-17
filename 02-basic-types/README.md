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
