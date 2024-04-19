
# <abbr title="C Sharp">C#</abbr>

## Editor Recomentado

Aunque podemos trabajar con múltiples **editores** para programar en <abbr title="C Sharp">C#</abbr> como **Visual Studio Code** remomendamos el  <abbr title="integrated development environment ">IDE</abbr> [Visual Studio Community](https://visualstudio.microsoft.com/es/vs/community/) pues a a larga nos ofrece m

# Enlaces de interés


# Tabla de contenidos

- [Depuración](#depuración-de-código)
- [Sentencias y comentarios](#sentencias-y-comentarios)
- [Variables](#variables)
- [Estructuras de control y ciclos](#estructuras-de-control)
- [Funciones](#funciones)
- [Errores](#errores)

## Depuración de código

```c
Debug.Log("El objeto Log lo utilizamos para depurar código");
```

## Sentencias y comentarios

>Las sentencias siempre han de terminar en punto y coma. Ejemplo:

```c
Debug.Log("Hello World");
```

```c

// Los comentarios se escriben con la doble barra o slash //

/* También podemos realizar comentarios multilínea, por ejemplo, si a lo mejor tenemos un problema a la hora de escribir una función o solucionar un "bug", comento cómo he llegado a esa solución o comento el "link" al vídeo, al tutorial o al "post" donde he encontrado la solución. También utilizo comentarios para señalar bloques de código en scripts que son muy grandes.
*/
```

## Variables

<abbr title="C Sharp">C#</abbr> es un lenguaje **fuertemente tipado**, por lo tanto, siempre siempre se ha de indicar el **tipo** de dato.

### string

>:warning: En **PHP** o **JavaScript** hemos visto que los *string* o *cadenas de texto* se podían rodear de comillas dobles o simples. En <abbr title="C Sharp">C#</abbr> los String llevan SIEMPRE comillas dobles

```c
 string myName = "Xurxo"; // Declaración e inicialización de la variable
 Debug.Log("Hello " + myName);
```


### int

```c
 int edad = 51;
```

### float

```c
 /* Para indicar que el número es decimal en el valor del dato 
 es necesario añadir una f */ 
 float estatura = 1.68f; 
```

### Arrays

```c
// Array con nombres.Length (2 nombres)
string[] nombres = { "Xurxo", "Andrés"}; 

// Inicializar un array notas.Length (1 elemento) pero sin valor.
int[] notas = new int[1];  

Debug.Log(nombres[0] + " tiene " + notas.Length + " notas.");
```

>:warning: Cuidado si te vas fuera del array

```c
// Siguiendo con el ejemplo anterior
Debug.Log(notas[2]);
```

![Error: Index out of range exception](/assets/index-out-of-range-exception.webp)

## Estructuras de control

Aquí no comento nada pues no hay diferencia con **JavaScript**.

## Funciones

>:eyes: El nombre de la funciones utilizado en Unity es en PascalCase en vez de CamelCase

```c
// Start is called before the first frame update
void Start() // Esta función no devuelve nada
{
     Debug.Log(DimeTuEdad(3));   
}

// Fíjate donde va el tipado de string para indicar el valor devuelto
string DimeTuEdad (int edad) 
{
    if (edad >= 18)
    {
        return "Eres mayor de edad";
    } else
    {
        return "Eres menor de edad";
    }
}
```

## Errores

>:warning: Los **scripts** nunca funcionan a no ser que no se encuentren asociados a la lógica de un **GameObject**

### Operadores relacionales

>:warning: Operadores como <code>===</code>, <code>!==</code> no se pueden utilizar en <abbr title="C Sharp">C#</abbr>

```c
 Debug.Log(true === true);
```

![Error: Invalid expression term '='](/assets/invalid-expression.webp)

