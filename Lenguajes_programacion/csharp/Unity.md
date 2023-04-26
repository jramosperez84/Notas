## Awake

El método Awake es un método especial en C# que se llama una vez cuando un objeto se crea en una escena de Unity. Este método se utiliza comúnmente para inicializar variables y realizar otras tareas de configuración necesarias antes de que se ejecute el objeto. Aquí te presento un ejemplo de cómo definir y utilizar el método Awake en C#:

```csharp
using UnityEngine;

public class MiScript : MonoBehaviour
{
    void Awake()
    {
        Debug.Log("El objeto se ha creado en la escena.");
    }
}
```

En este ejemplo, se ha definido el método Awake en la clase "MiScript". El método simplemente muestra un mensaje en la consola utilizando el método "Debug.Log". El método Awake se llamará automáticamente una vez que se haya creado un objeto de la clase "MiScript" en la escena.

Es importante tener en cuenta que el método Awake se llama antes del método Start, que es otro método especial utilizado en Unity para iniciar un objeto. En general, se recomienda utilizar el método Awake para inicializar cualquier variable que necesite estar lista antes de que se ejecute el objeto, y utilizar el método Start para realizar cualquier tarea de configuración adicional que pueda ser necesaria.

Aquí hay un ejemplo de cómo utilizar el método Awake y el método Start juntos en una clase de Unity:

```csharp
using UnityEngine;

public class MiScript : MonoBehaviour
{
    public int ValorInicial;
    private int _valorActual;
    
    void Awake()
    {
        _valorActual = ValorInicial;
        Debug.Log("El objeto se ha creado con un valor inicial de " + _valorActual);
    }
    
    void Start()
    {
        _valorActual += 5;
        Debug.Log("El valor actual del objeto es " + _valorActual);
    }
}
```

En este ejemplo, se ha definido una clase "MiScript" que tiene una propiedad pública "ValorInicial" y una variable privada "_valorActual". En el método Awake, se establece el valor inicial de la variable "_valorActual" utilizando el valor de la propiedad "ValorInicial". Luego, se muestra un mensaje en la consola que indica el valor inicial. En el método Start, se agrega 5 al valor actual de la variable "_valorActual", y se muestra un mensaje en la consola que indica el nuevo valor actual.

### La importancia del método Awake en las llamadas entre scripts:

Cuando necesitas llamar a un método de un script desde otro script, lo primero que debes hacer es obtener una referencia al script que contiene el método que deseas llamar. Esta referencia se puede obtener de varias formas, como se mencionó anteriormente, pero si decides utilizar el método `Awake()`, podrías hacer lo siguiente:

1. En el script que desea llamar al método, crea una variable para almacenar la referencia al script que contiene el método que se desea llamar:

```csharp
private ScriptDelObjetoConElScript scriptDelObjetoConElScript;
```

2. En el método `Awake()` del script que realiza la llamada, obtén la referencia al script del objeto que contiene el método que deseas llamar:

```csharp
void Awake() {
    scriptDelObjetoConElScript = objetoConElScript.GetComponent<ScriptDelObjetoConElScript>();
}
```

3. Una vez que tienes la referencia, puedes llamar al método que deseas desde cualquier método del script que realiza la llamada:

```csharp
void MetodoQueLlamaAlMetodoDelOtroScript() {
    scriptDelObjetoConElScript.MetodoDelOtroScript();
}
```

De esta manera, puedes llamar a un método de otro script y asegurarte de que la referencia al script esté disponible antes de realizar la llamada.

Es importante tener en cuenta que el método `Awake()` se llama una sola vez, antes del método `Start()`, por lo que debes asegurarte de que las referencias que necesites para llamar a los métodos estén disponibles en ese momento. Además, debes asegurarte de que el objeto que contiene el script al que deseas llamar ya exista en la escena para que puedas obtener la referencia.

#### Instance

Cuando queremos hacer estas llamadas, por ejemplo a un script llamado `Record.cs` nos aseguramos de definir una variable estática pública llamada `Instance` en la clase `Record`. Esta variable estática es una instancia única de la clase `Record` que se puede acceder y utilizar en otros scripts sin la necesidad de crear una nueva instancia de la clase.

El modificador `public` indica que la variable estática `Instance` se puede acceder desde cualquier otro script en tu proyecto. El modificador `static` indica que esta variable estática pertenece a la clase `Record` y no a una instancia particular de la clase.

En otras palabras, cuando la clase `Record` se carga en la memoria al inicio del juego (lo cual ocurre antes del método `Awake()`), la variable estática `Instance` también se carga y se asigna a un valor inicial de `null`.

Dentro del método `Awake()`, es común que se establezca el valor de la variable estática `Instance` a la instancia actual de la clase `Record`. Esto se hace de la siguiente manera:

```csharp
void Awake() {
    if (Instance == null) {
        Instance = this;
    }
}
```

Esta línea de código comprueba si la variable estática `Instance` es igual a `null`. Si es así, establece el valor de `Instance` en la instancia actual de la clase `Record` (`this`).

Al establecer la variable estática `Instance` en la instancia actual de la clase `Record`, cualquier otro script en tu proyecto puede acceder a la instancia actual de la clase `Record` utilizando la variable estática `Record.Instance`. Esto es útil cuando necesitas acceder a métodos o variables públicas de la clase `Record` desde otros scripts sin tener que crear una nueva instancia de la clase.