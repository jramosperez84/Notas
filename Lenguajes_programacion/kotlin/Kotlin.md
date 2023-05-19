## Descripción:

Kotlin es un lenguaje de programación moderno que se ejecuta en la plataforma de Java Virtual Machine (JVM) y que también puede ser compilado a código nativo. Fue desarrollado por JetBrains y lanzado en 2011. Kotlin está diseñado para ser seguro, conciso, expresivo y compatible con Java, lo que significa que puedes usar bibliotecas de Java en tu código Kotlin sin problemas. Kotlin es ampliamente utilizado para el desarrollo de aplicaciones móviles Android, así como para aplicaciones de servidor, aplicaciones web y más.

## Tipos de datos:

### Variables de tipo entero:

-   Tipos de datos: Byte, Short, Int, Long
-   Ejemplo de declaración:

```kotlin
val myByte: Byte = 10
val myShort: Short = 100
val myInt: Int = 1000
val myLong: Long = 1000000000L
```

### Variables de tipo flotante:

-   Tipos de datos: Float, Double
-   Ejemplo de declaración:

```kotlin
val myFloat: Float = 3.14f 
val myDouble: Double = 3.14159265359
```

### Variables de tipo booleano:

-   Tipos de datos: Boolean
-   Ejemplo de declaración:

```kotlin
val isTrue: Boolean = true 
val isFalse: Boolean = false
```

### Variables de tipo carácter:

-   Tipos de datos: Char
-   Ejemplo de declaración:

```kotlin
val myChar: Char = 'A'
```

### Variables de tipo cadena:

-   Tipos de datos: String
-   Ejemplo de declaración:

```kotlin
val myString: String = "Hola, Mundo!"
```

### Además, en Kotlin también existen variables de tipo nulo, que permiten que una variable contenga un valor nulo:

-   Tipo de datos: Any?, String?, Int?, etc.
-   Ejemplo de declaración:

```kotlin
var myString: String? = null
```

En la declaración de variables en Kotlin, se utiliza la palabra clave "val" para definir una variable de solo lectura, cuyo valor no puede ser modificado una vez asignado, y la palabra clave "var" para definir una variable mutable, cuyo valor puede ser cambiado en cualquier momento.

## Operadores:

1.  Operadores aritméticos:
    
    -   Suma: +
    -   Resta: -
    -   Multiplicación: *
    -   División: /
    -   Módulo: %
    
2.  Operadores de comparación:
    
    -   Igualdad: ==
    -   Desigualdad: !=
    -   Mayor que: >
    -   Menor que: <
    -   Mayor o igual que: >=
    -   Menor o igual que: <=
    
3.  Operadores lógicos:
    
    -   Y: &&
    -   O: ||
    -   Negación: !
    
4.  Operadores de asignación:
    
    -   Asignación: =
    -   Suma y asignación: +=
    -   Resta y asignación: -=
    -   Multiplicación y asignación: *=
    -   División y asignación: /=
    -   Módulo y asignación: %=
    
5.  Otros operadores: 

- Operador de rango: ..

El operador de rango se utiliza para crear rangos de valores de manera concisa y legible. Por ejemplo:

```kotlin
val numbers = 1..10 // crea un rango que incluye los números del 1 al 10
for (i in numbers) {
    println(i)
}
```

En este ejemplo, se crea un rango de valores del 1 al 10 utilizando el operador de rango ".." y se utiliza un bucle "for" para imprimir cada valor del rango.

- Operador de acceso seguro: ?.

El operador de acceso seguro se utiliza para acceder a un valor de una variable o propiedad solo si esta no es nula. Si la variable es nula, la expresión completa devuelve nulo sin generar una excepción de tipo "NullPointerException". Por ejemplo:

```kotlin
val myString: String? = null
val length = myString?.length
```

En este ejemplo, la variable "myString" es de tipo "String?" (nullable), por lo que se utiliza el operador de acceso seguro "?.", seguido de la propiedad "length", para obtener su longitud solo si la variable no es nula.

- Operador de elvis: ?:

El operador de elvis se utiliza para proporcionar un valor predeterminado en caso de que una expresión sea nula. Por ejemplo:

```kotlin
val myString: String? = null 
val length = myString?.length ?: 0
```

En este ejemplo, se utiliza el operador de acceso seguro "?.", seguido del operador de elvis "?:", para proporcionar un valor predeterminado de cero si la expresión "myString?.length" es nula.

- Operador de no-nulo: !!

El operador de no-nulo se utiliza para indicar al compilador que una expresión no puede ser nula. Si la expresión es nula en tiempo de ejecución, se produce una excepción de tipo "NullPointerException". Este operador se utiliza en situaciones en las que se sabe que una expresión no puede ser nula y se quiere evitar la verificación de nulabilidad. Por ejemplo:

```kotlin
val myString: String? = "Hola, Mundo!"
val length = myString!!.length
```

En este ejemplo, se utiliza el operador de no-nulo "!!" para indicar al compilador que la variable "myString" no puede ser nula. Si la variable es nula en tiempo de ejecución, se produce una excepción de tipo "NullPointerException".

- Operador de referencia: ::

El operador de referencia se utiliza para hacer referencia a una función o propiedad sin llamarla o evaluarla. Por ejemplo:

```kotlin
fun sayHello(name: String) {
    println("Hola, $name!")
}

val greeting = ::sayHello
greeting("Juan")
```

En este ejemplo, se utiliza el operador de referencia "::" para hacer referencia a la función "sayHello" sin llamarla o evaluarla. La variable "greeting" se convierte en una referencia a la función "sayHello" y se puede llamar como una función normal.

Es importante tener en cuenta que la mayoría de los operadores tienen una precedencia y asociatividad específica, lo que determina el orden en que se realizan las operaciones. Para evitar confusiones, es recomendable utilizar paréntesis para agrupar las operaciones de acuerdo a la precedencia deseada.

## Condicionales:

1. Sentencia "if":

```kotlin
val age = 18
if (age >= 18) {
    println("Eres mayor de edad")
}
```

En este ejemplo, la sentencia "if" verifica si la variable "age" es mayor o igual a 18 y, si es así, muestra el mensaje "Eres mayor de edad".

2. Sentencia "if-else":

```kotlin
val score = 85
if (score >= 90) {
    println("Tu calificación es A")
} else if (score >= 80) {
    println("Tu calificación es B")
} else if (score >= 70) {
    println("Tu calificación es C")
} else {
    println("Tu calificación es D")
}
```

En este ejemplo, la sentencia "if-else" verifica el valor de la variable "score" y muestra un mensaje correspondiente según el rango en el que se encuentre.

3. Sentencia "when":

```kotlin
val dayOfWeek = 3
when (dayOfWeek) {
    1 -> println("Lunes")
    2 -> println("Martes")
    3 -> println("Miércoles")
    4 -> println("Jueves")
    5 -> println("Viernes")
    else -> println("Fin de semana")
}
```

En este ejemplo, la sentencia "when" verifica el valor de la variable "dayOfWeek" y muestra el nombre del día de la semana correspondiente. Si el valor no coincide con ninguno de los casos especificados, se ejecuta el bloque "else".

### También es posible utilizar operadores lógicos como "&&" (and) y "||" (or) para combinar múltiples condiciones en una sentencia "if". Por ejemplo:

```kotlin
val age = 21
val hasLicense = true

if (age >= 18 && hasLicense) {
    println("Puedes conducir")
} else {
    println("No puedes conducir")
}
```

En este ejemplo, la sentencia "if" verifica si la variable "age" es mayor o igual a 18 y si la variable "hasLicense" es verdadera. Si ambas condiciones se cumplen, se muestra el mensaje "Puedes conducir". Si alguna de las condiciones no se cumple, se muestra el mensaje "No puedes conducir".

## Bucles:

1. Bucle "for":

```kotlin
val numbers = listOf(1, 2, 3, 4, 5)
for (number in numbers) {
    println(number)
}
```

En este ejemplo, se utiliza un bucle "for" para recorrer una lista de números y se utiliza la variable "number" para representar cada elemento de la lista. En cada iteración del bucle, se imprime el valor de "number".

2. Bucle "while":

```kotlin
var count = 0
while (count < 5) {
    println("Contador: $count")
    count++
}
```

En este ejemplo, se utiliza un bucle "while" para imprimir un mensaje de contador cinco veces. La variable "count" se utiliza para realizar un seguimiento del número de iteraciones, y se incrementa en cada iteración del bucle.

3. Bucle "do-while":

```kotlin
var guess: Int
var secretNumber = 7

do {
    print("Adivina el número secreto: ")
    guess = readLine()?.toIntOrNull() ?: 0
} while (guess != secretNumber)

println("¡Adivinaste!")
```

En este ejemplo, se utiliza un bucle "do-while" para pedir al usuario que adivine un número secreto. La variable "guess" se inicializa fuera del bucle y se actualiza con la entrada del usuario en cada iteración del bucle. El bucle se sigue ejecutando hasta que la suposición del usuario sea igual al número secreto. Después de salir del bucle, se imprime un mensaje de felicitación.

Además, en Kotlin, es posible utilizar bucles "for" con rangos y expresiones cuando para realizar operaciones en una serie de valores o elementos que cumplen ciertas condiciones. Por ejemplo:

```kotlin
for (i in 1..10) {
    println(i)
}

val fruits = listOf("manzana", "banana", "kiwi", "naranja")
for (fruit in fruits.filter { it.startsWith("m") }) {
    println(fruit)
}
```

En el primer ejemplo, se utiliza un bucle "for" para imprimir números del 1 al 10 utilizando un rango. En el segundo ejemplo, se utiliza un bucle "for" para imprimir solo las frutas que comienzan con la letra "m" utilizando la función "filter" en una lista de frutas.

## Funciones:

En Kotlin, se utilizan funciones para agrupar un conjunto de instrucciones relacionadas en una unidad reutilizable y modular. Aquí te muestro un ejemplo de cómo se define y utiliza una función en Kotlin:

```kotlin
fun sum(a: Int, b: Int): Int {
    return a + b
}

val result = sum(5, 10)
println("El resultado es $result")
```

En este ejemplo, se define una función llamada "sum" que toma dos parámetros de entrada de tipo "Int" y devuelve un resultado de tipo "Int". La función simplemente suma los dos números y devuelve el resultado.

Luego, se llama a la función "sum" con dos argumentos (5 y 10) y se almacena el resultado en la variable "result". Finalmente, se imprime el resultado en la consola.

Además, en Kotlin, es posible definir funciones con parámetros opcionales y con valores predeterminados. Por ejemplo:

```kotlin
fun greet(name: String, message: String = "Hola") {
    println("$message, $name!")
}

greet("Juan")
greet("Pedro", "Buenos días")
```

En este ejemplo, se define una función llamada "greet" que toma dos parámetros de entrada: "name" y "message". El parámetro "message" tiene un valor predeterminado de "Hola". La función simplemente imprime un mensaje de saludo utilizando los dos parámetros.

Luego, se llama a la función "greet" dos veces: la primera vez solo con el parámetro "name" (en cuyo caso se utilizará el valor predeterminado para "message") y la segunda vez con ambos parámetros especificados.

También es posible definir funciones que devuelvan valores nulos. Para ello, se utiliza el operador "?" después del tipo de dato devuelto en la definición de la función. Por ejemplo:

```kotlin
fun findMax(numbers: List<Int>): Int? {
    if (numbers.isEmpty()) {
        return null
    }

    var max = numbers[0]
    for (number in numbers) {
        if (number > max) {
            max = number
        }
    }

    return max
}

val numbers = listOf(1, 3, 5, 2, 4)
val maxNumber = findMax(numbers)

if (maxNumber != null) {
    println("El número máximo es $maxNumber")
} else {
    println("La lista está vacía")
}
```

En este ejemplo, se define una función llamada "findMax" que toma una lista de números como entrada y devuelve el número máximo en la lista. Si la lista está vacía, la función devuelve nulo.

Luego, se llama a la función "findMax" con una lista de números y se almacena el resultado en la variable "maxNumber". Se utiliza una expresión "if" para comprobar si el resultado es nulo antes de imprimir el número máximo en la consola.

## Clases:

En Kotlin, las clases son la base para la programación orientada a objetos. A continuación, te muestro un ejemplo de cómo se define y utiliza una clase en Kotlin:

```kotlin
class Person(val name: String, var age: Int) {
    fun greet() {
        println("Hola, mi nombre es $name y tengo $age años")
    }
}

val person = Person("Juan", 30)
person.greet()
person.age = 31
person.greet()
```

En este ejemplo, se define una clase llamada "Person" con dos propiedades: "name" de solo lectura (inicializada en el constructor) y "age" de lectura y escritura. La clase también tiene un método llamado "greet" que imprime un mensaje de saludo utilizando las propiedades de la clase.

Luego, se crea una instancia de la clase "Person" con el nombre "Juan" y la edad 30, y se almacena en la variable "person". Se llama al método "greet" de la instancia "person" para imprimir el mensaje de saludo en la consola.

Finalmente, se actualiza la propiedad "age" de la instancia "person" a 31 y se llama de nuevo al método "greet" para imprimir el mensaje actualizado.

1. Constructores: Los constructores son métodos especiales que se utilizan para inicializar una instancia de una clase. En Kotlin, es posible definir uno o varios constructores en una clase, utilizando la palabra clave "constructor". Por defecto, si no se define un constructor, se utiliza el constructor predeterminado sin argumentos. Por ejemplo:

```kotlin
class Person(val name: String, var age: Int) {
    constructor(name: String) : this(name, 0)
}
```

En este ejemplo, se define una clase "Person" con dos propiedades: "name" de solo lectura y "age" de lectura y escritura. También se define un constructor adicional que toma solo el parámetro "name" y llama al constructor principal pasando "name" y un valor predeterminado de cero para "age".

2. Getters y Setters: En Kotlin, las propiedades de una clase se pueden definir con getters y setters personalizados utilizando los identificadores "get" y "set". Si se omiten estos identificadores, se utilizarán los getters y setters predeterminados que se generan automáticamente para las propiedades de lectura y escritura, respectivamente. Por ejemplo:

```kotlin
class Person(val name: String, var age: Int) {
    var isAdult: Boolean
        get() = age >= 18
        set(value) {
            age = if (value) 18 else 0
        }
}
```

En este ejemplo, se define una propiedad de solo escritura llamada "isAdult" que se basa en la propiedad "age". Se define un getter personalizado que devuelve verdadero si la edad es mayor o igual a 18 y un setter personalizado que establece la edad en 18 si se establece la propiedad en verdadero o en 0 si se establece en falso.

3. Otros métodos: En Kotlin, se pueden definir métodos adicionales en una clase para realizar diversas operaciones y funcionalidades. Por ejemplo:

```kotlin
class Person(val name: String, var age: Int) {
    fun greet() {
        println("Hola, mi nombre es $name y tengo $age años")
    }

    fun haveBirthday() {
        age++
    }
}
```

En este ejemplo, se definen dos métodos adicionales en la clase "Person": "greet", que imprime un mensaje de saludo utilizando las propiedades de la clase, y "haveBirthday", que incrementa la edad de la persona en uno.

También es posible definir clases con métodos y propiedades estáticas utilizando la palabra clave "companion object". Por ejemplo:

```kotlin
class MathUtils {
    companion object {
        fun sum(a: Int, b: Int): Int {
            return a + b
        }

        fun multiply(a: Int, b: Int): Int {
            return a * b
        }
    }
}

val result1 = MathUtils.sum(5, 10)
val result2 = MathUtils.multiply(5, 10)
println("La suma es $result1 y el producto es $result2")
```

En este ejemplo, se define una clase llamada "MathUtils" con un objeto "companion" que contiene dos métodos estáticos: "sum" y "multiply". Los métodos simplemente realizan una suma y una multiplicación de dos números enteros y devuelven el resultado.

Luego, se llama a los métodos "sum" y "multiply" de la clase "MathUtils" para realizar las operaciones y se almacenan los resultados en las variables "result1" y "result2". Finalmente, se imprime un mensaje en la consola que muestra los resultados.

[Volver](/Lenguajes_de_programacion.md)