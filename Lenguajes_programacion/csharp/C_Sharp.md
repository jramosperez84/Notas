## C# 

## Descripción:

C#, también conocido como C Sharp. Es un lenguaje de programación orientado a objetos desarrollado por Microsoft. Es uno de los lenguajes de programación más populares y se utiliza comúnmente para el desarrollo de aplicaciones de escritorio, aplicaciones web y juegos. C# también se utiliza para el desarrollo de aplicaciones móviles en plataformas como Xamarin y Unity.

## Tipos de datos mas usados:

1. Int

```csharp
int numero = 10;
```

2. String

```csharp
string nombre = "Juan";
```

3. Bool

```csharp
bool esMayorDeEdad = true;
```

4. Double

```csharp
double precio = 9.99;
```

5. Char

```csharp
char inicial = 'J';
```

6. Decimal

```csharp
decimal saldo = 100.50m;
```

7. Float

```csharp
float altura = 1.75f;
```

8. Long

```csharp
long numeroGrande = 10000000000;
```

9. Byte

```csharp
byte edad = 25;
```

10. Short

```csharp
short codigo = 1234;
```

11. Object

```csharp
object objetoGenerico = new object();
```

A continuación, te presento una lista de todos los tipos de variables disponibles en C#:

-   sbyte
-   byte
-   short
-   ushort
-   int
-   uint
-   long
-   ulong
-   char
-   float
-   double
-   decimal
-   bool
-   object
-   string
-   DateTime
-   TimeSpan
-   Guid
-   Enum
-   Nullable
-   dynamic

## Operadores:

1.  Operadores aritméticos:

-   Suma (+)
-   Resta (-)
-   Multiplicación (*)
-   División (/)
-   Módulo (%)

2.  Operadores de asignación:

-   Asignación (=)
-   Asignación de suma (+=)
-   Asignación de resta (-=)
-   Asignación de multiplicación (*=)
-   Asignación de división (/=)
-   Asignación de módulo (%=)
-   Asignación de AND (&=)
-   Asignación de OR (|=)
-   Asignación de XOR (^=)
-   Asignación de desplazamiento a la izquierda (<<=)
-   Asignación de desplazamiento a la derecha (>>=)

3.  Operadores de comparación:

-   Igual que (==)
-   Distinto que (!=)
-   Menor que (<)
-   Menor o igual que (<=)
-   Mayor que (>)
-   Mayor o igual que (>=)

4.  Operadores lógicos:

-   AND lógico (&&)
-   OR lógico (||)
-   NOT lógico (!)

5.  Operadores de incremento y decremento:

-   Incremento (++)
    
-   Decremento (--)
    

6.  Operadores de desplazamiento:

-   Desplazamiento a la izquierda (<<)
-   Desplazamiento a la derecha (>>)

7.  Operadores de bits:

-   AND a nivel de bits (&)
-   OR a nivel de bits (|)
-   XOR a nivel de bits (^)
-   NOT a nivel de bits (~)

8.  Operadores condicionales:

-   Operador ternario condicional ( ? : )
-   Null coalescing operator ( ?? )

9.  Operador de fusión de nulos:

-   Null Propagation Operator ( ?. )

## Condicionales:

En C# existen varias estructuras condicionales que te permiten ejecutar diferentes bloques de código en función de ciertas condiciones. Las estructuras condicionales más comunes en C# son el if, el if-else, el if-else if y el switch.

1. if: Esta estructura se utiliza para ejecutar un bloque de código si una condición es verdadera. Si la condición es falsa, el bloque de código no se ejecuta. Aquí hay un ejemplo de cómo se usa el if:

```csharp
if (edad >= 18) 
{
    Console.WriteLine("Eres mayor de edad");
}
```

2. if-else: Esta estructura se utiliza para ejecutar un bloque de código si la condición es verdadera, y otro bloque de código si la condición es falsa. Aquí hay un ejemplo de cómo se usa el if-else:

```csharp
if (edad >= 18) 
{
    Console.WriteLine("Eres mayor de edad");
}
else 
{
    Console.WriteLine("Eres menor de edad");
}
```

3. f-else if: Esta estructura se utiliza para evaluar múltiples condiciones y ejecutar diferentes bloques de código en función de la primera condición verdadera encontrada. Aquí hay un ejemplo de cómo se usa el if-else if:

```csharp
if (edad >= 18) 
{
    Console.WriteLine("Eres mayor de edad");
}
else if (edad >= 13) 
{
    Console.WriteLine("Eres un adolescente");
}
else 
{
    Console.WriteLine("Eres un niño");
}
```

4. switch: Esta estructura se utiliza para evaluar una variable y ejecutar diferentes bloques de código en función del valor de la variable. Aquí hay un ejemplo de cómo se usa el switch:

```csharp
switch (diaDeLaSemana) 
{
    case 1:
        Console.WriteLine("Lunes");
        break;
    case 2:
        Console.WriteLine("Martes");
        break;
    case 3:
        Console.WriteLine("Miércoles");
        break;
    case 4:
        Console.WriteLine("Jueves");
        break;
    case 5:
        Console.WriteLine("Viernes");
        break;
    case 6:
        Console.WriteLine("Sábado");
        break;
    case 7:
        Console.WriteLine("Domingo");
        break;
    default:
        Console.WriteLine("Día de la semana no válido");
        break;
}
```

## Funciones:

En C#, puedes crear funciones utilizando la sintaxis "public static [tipo de retorno] [nombre de la función](https://chat.openai.com/c/%5Bpar%C3%A1metros%5D)". Aquí te presento un ejemplo de cómo crear una función que calcule la suma de dos números:

```csharp
public static int Sumar(int num1, int num2)
{
    int resultado = num1 + num2;
    return resultado;
}
```

En este ejemplo, la función se llama "Sumar" y toma dos parámetros de tipo entero, "num1" y "num2". Dentro de la función, se calcula la suma de los dos números y se guarda en una variable llamada "resultado". Finalmente, la función devuelve el valor de la variable "resultado".

Para hacer uso de esta función, puedes llamarla desde otro método en tu programa. Aquí hay un ejemplo de cómo llamar a la función "Sumar" desde el método "Main":

```csharp
static void Main(string[] args)
{
    int resultado = Sumar(5, 10);
    Console.WriteLine("El resultado es: " + resultado);
}
```

En este ejemplo, se llama a la función "Sumar" con los argumentos 5 y 10. El valor de retorno de la función se guarda en una variable llamada "resultado", que luego se muestra en la consola utilizando el método "WriteLine".

## Clases:

En C#, las clases se utilizan para definir objetos y encapsular datos y comportamientos relacionados en un solo lugar. Aquí te presento un ejemplo de cómo crear una clase simple en C#:

```csharp
public class Persona
{
    public string Nombre;
    public int Edad;
    
    public void Presentarse()
    {
        Console.WriteLine("Hola, mi nombre es " + Nombre + " y tengo " + Edad + " años.");
    }
}
```

En este ejemplo, la clase se llama "Persona" y tiene dos propiedades públicas: "Nombre" y "Edad". También tiene un método público llamado "Presentarse", que muestra un saludo en la consola.

Para hacer uso de esta clase, puedes crear una instancia de la misma en tu programa y acceder a sus propiedades y métodos. Aquí hay un ejemplo de cómo crear una instancia de la clase "Persona" y llamar a su método "Presentarse":

```csharp
static void Main(string[] args)
{
    Persona persona1 = new Persona();
    persona1.Nombre = "Juan";
    persona1.Edad = 25;
    persona1.Presentarse();
}
```

En este ejemplo, se crea una instancia de la clase "Persona" llamada "persona1". Luego, se establecen los valores de las propiedades "Nombre" y "Edad" de la instancia. Finalmente, se llama al método "Presentarse" de la instancia, lo que muestra un saludo en la consola.

Este es solo un ejemplo básico de cómo crear y usar una clase en C#. Las clases pueden tener muchas más propiedades y métodos, y pueden ser utilizadas para construir programas muy complejos y sofisticados.

### Constructor:

En C# las clases pueden tener constructores que se utilizan para inicializar los objetos de la clase con valores iniciales. Los constructores son métodos especiales que tienen el mismo nombre que la clase y no tienen un tipo de retorno explícito. Aquí te presento un ejemplo de cómo declarar y utilizar un constructor en C#:

```csharp
public class Persona
{
    public string Nombre;
    public int Edad;
    
    public Persona(string nombre, int edad)
    {
        Nombre = nombre;
        Edad = edad;
    }
    
    public void Presentarse()
    {
        Console.WriteLine("Hola, mi nombre es " + Nombre + " y tengo " + Edad + " años.");
    }
}
```

En este ejemplo, se ha agregado un constructor a la clase "Persona" que toma dos parámetros, "nombre" y "edad". Dentro del constructor, se establecen los valores de las propiedades "Nombre" y "Edad" con los valores de los parámetros.

Para utilizar este constructor, puedes crear una instancia de la clase y pasarle los valores de los parámetros al constructor. Aquí hay un ejemplo de cómo crear una instancia de la clase "Persona" utilizando el constructor:

```csharp
static void Main(string[] args)
{
    Persona persona1 = new Persona("Juan", 25);
    persona1.Presentarse();
}
```

En este ejemplo, se crea una instancia de la clase "Persona" llamada "persona1" utilizando el constructor que toma los parámetros "nombre" y "edad". Se pasan los valores "Juan" y 25 como argumentos al constructor. Luego, se llama al método "Presentarse" de la instancia, lo que muestra un saludo en la consola.

Es importante tener en cuenta que las clases pueden tener varios constructores, cada uno con un número diferente de parámetros. También es posible sobrecargar constructores en C#, lo que significa que puedes tener varios constructores con el mismo nombre, pero con diferentes parámetros. Esto te permite crear objetos de la clase con diferentes conjuntos de valores iniciales.

### Getters y Setters:

En C# es posible definir métodos Getters y Setters para acceder y modificar los valores de las propiedades de una clase de forma controlada. En C#, estos métodos se conocen como propiedades, y se definen utilizando la sintaxis "public [tipo de dato] [nombre de propiedad] { get; set; }". Aquí te presento un ejemplo de cómo definir una propiedad en C#:

```csharp
public class Persona
{
    private string _nombre;
    private int _edad;
    
    public string Nombre 
    { 
        get { return _nombre; } 
        set { _nombre = value; } 
    }
    
    public int Edad 
    { 
        get { return _edad; } 
        set { _edad = value; } 
    }
    
    public void Presentarse()
    {
        Console.WriteLine("Hola, mi nombre es " + Nombre + " y tengo " + Edad + " años.");
    }
}
```

En este ejemplo, se han definido dos propiedades para la clase "Persona": "Nombre" y "Edad". Cada propiedad tiene un método Getter y un método Setter definido en su cuerpo. El método Getter se utiliza para obtener el valor de la propiedad, mientras que el método Setter se utiliza para establecer el valor de la propiedad.

Es importante tener en cuenta que las propiedades pueden tener modificadores de acceso, lo que te permite controlar el nivel de acceso que tiene el código a las propiedades de la clase. En este ejemplo, las propiedades "Nombre" y "Edad" se han definido como públicas, lo que significa que cualquier código puede acceder a ellas. Sin embargo, también es posible definir propiedades como privadas o protegidas, lo que limita su acceso a ciertos miembros de la clase.

Para utilizar las propiedades en una instancia de la clase, puedes utilizar la sintaxis de punto para acceder a ellas. Aquí hay un ejemplo de cómo utilizar las propiedades "Nombre" y "Edad" de una instancia de la clase "Persona":

```csharp
static void Main(string[] args)
{
    Persona persona1 = new Persona();
    persona1.Nombre = "Juan";
    persona1.Edad = 25;
    persona1.Presentarse();
}
```

En este ejemplo, se crea una instancia de la clase "Persona" llamada "persona1". Luego, se establecen los valores de las propiedades "Nombre" y "Edad" de la instancia utilizando la sintaxis de punto. Finalmente, se llama al método "Presentarse" de la instancia, lo que muestra un saludo en la consola.

[Volver](Indice.md)