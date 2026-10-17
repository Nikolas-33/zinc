<img width="200" height="200" alt="texto" src="https://github.com/user-attachments/assets/69554d76-3af7-4823-966b-796ead7642d6" />

# Zinc

**Zinc** es un lenguaje de programación interpretado, desarrollado en Python. Incluye variables, funciones, condiciones, bucles y un módulo propio para interactuar con el sistema.

## Características

- Variables numéricas y de texto.
- Entrada de datos mediante `preg([])`.
- Salida de texto con `decir()`.
- Funciones personalizadas con `fun()`.
- Condiciones numéricas con `sin()` y `non()`.
- Bucles con `repe()`.
- Ejecución de código mediante `ejec()`.
- Eliminación de variables y funciones con `elim`.
- Módulo `tor` para controlar algunas funciones del sistema.
- Modo interactivo.
- Ejecución de archivos `.zn`.

## Uso

### Ejecutar un archivo

```bash
zinc programa.zn
```

Los programas de Zinc solo utilizan la extensión `.zn`.

### Consultar la versión

```bash
zinc --version
```

### Mostrar la ayuda

```bash
zinc --ayuda
```

### Consultar el número atómico (me aburro mucho, por eso está aquí)

```bash
zinc --numero.atomico
```

### Modo interactivo

Ejecuta `zinc` sin argumentos para entrar en el intérprete interactivo:

```text
Zinc

>>> decir "Hola, mundo!"
Hola, mundo!
```

## Sintaxis básica

En Zinc, las instrucciones se separan con `;; `.
```zinc
>>> decir "Hola";; decir "Mundo"
HolaMundo
```

### Mostrar texto

```zinc
>>> decir "Hola, mundo!"
Hola, mundo!
```

Para introducir un salto de línea dentro del texto, utiliza `^`.

```zinc
>>> decir "Hola^Mundo"
Hola
Mundo
```

### Variables

Las variables se crean con `var` y se asignan mediante `es`.

```zinc
>>> var Nombre es "Nikolas"

>>> var Edad es 15

>>> decir Nombre
Nikolas
>>> decir Edad
15
```

Zinc distingue entre variables de texto y variables numéricas.

### Entrada de datos

Para leer texto:

```zinc
>>> preg(Nombre[tex])
```

Para leer un número entero:

```zinc
>>> preg(Edad[num])
```

### Funciones

Las funciones se definen con `fun` y sus instrucciones se separan mediante `:: `.

```zinc
>>> fun(saludar es decir "Hola^":: var Buenos Dias es "Feliz Jueves":: Buenos Dias)

>>> saludar
Hola
Feliz Jueves
```

### Condiciones

`sin` ejecuta las instrucciones si dos valores numéricos son iguales.

```zinc
>>> var Edad es 18

>>> sin(Edad es 18 hacer decir "Mayor de edad")
Mayor de edad
```

`non` ejecuta las instrucciones si los valores son distintos.

```zinc
>>> non(Edad es 18 hacer decir "La edad es distinta")
```

### Bucles

`repe` permite repetir instrucciones un número determinado de veces (Se separa con ¡¡ ).

```zinc
>>> repe(3, decir "Hola^"¡¡ decir "Adios^")
Hola
Adios
Hola
Adios
Hola
Adios
```

También admite variables numéricas como contador.

```zinc
>>> var X es 3
>>> repe(X, decir "Hola^"¡¡ decir "Adios^")
Hola
Adios
Hola
Adios
Hola
Adios
```

**Importante: (mas o menos)** en la implementación actual, `repe(0, ...)` ejecuta un bucle infinito.

### Ejecutar código almacenado

```zinc
>>> ejec("decir 'Hola desde ejec'")
```

También puedes ejecutar código almacenado en una variable de texto. (se separa con && )

### Eliminar elementos

```zinc
>>> elim tex: texto
>>> elim num: numero
>>> elim fun: funcion
```

## Módulo `tor`

El módulo `tor` proporciona funciones adicionales. Para utilizarlo, primero debes importarlo:

```zinc
>>> importar tor
```

### Esperar

Pausa la ejecución durante un número de segundos, con un numero entero o con una variable num.

```zinc
>>> tor.esperar(2)
>>> var x es 2
>>> tor.esperar(x)
```

### Cambiar el título de la terminal con texto o una variable tex

```zinc
>>> tor.titulo("Mi programa")
>>> var x es "Feliz Jueves"
>>> tor.titulo(x)
```

### Controlar el sistema de errores

```zinc
>>> tor.sae(S)
>>> tor.sae(N)
```

`S` activa la salida del programa al producirse un error de Zinc; `N` la desactiva.

### Limpiar la terminal

```zinc
>>> tor.limpiar
```

### Ejecutar comandos del sistema

```zinc
>>> tor.cmd("comando")
```

Esta instrucción ejecuta un comando del sistema operativo. Utilízala únicamente con comandos de confianza.

## Errores

Zinc dispone de varios códigos de error:

| Código | Significado |
|---|---|
| `E001` | Tipo o nombre incorrecto |
| `E002` | Sintaxis incorrecta |
| `E003` | Valor incorrecto |
| `E004` | Archivo no encontrado |
| `E005` | Extensión de archivo no admitida |
| `E006` | Elemento inexistente |
| `E007` | Módulo no importado |

### Version

**Zinc v0.1** — Lenguaje en desarrollo, creado en Python.
