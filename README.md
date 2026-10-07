<img width="200" height="200" alt="texto" src="https://github.com/user-attachments/assets/57fd0ce3-8d39-4c46-9d11-cff31b91dcd1" />

# Lenguaje de programación Zinc. 
- creado con Python.
- Sigue en desarrollo.
- Sintaxis medianamente sencilla 
- Y un único .exe.
  
# Caracteristicas.
- Archivos .zn
- Más o menos legible.
- Hecho para adentrarse en la programación y aprender un poco.
- Interprete incluido con el .exe.

# Instalación.
Puedes descargarlo con el .cmd que está disponible en cada relase.
Una vez instalado, puedes hacer estas cosas. (Por ahora)


``` 
zinc --ayuda
zinc --numero atomico
zinc --version
zinc archivo.zn
zinc
```

# Ejemplos:
- como normalmente es el primer programa:

```
decir "Hola Mundo" 
```

- Luego están las variables:
  
```
var Hola es "Feliz Jueves"
var Adios es 33
preg(variablesstr[str])
preg(vriableint[int])
```

No hay nada más interesante, solo las funciones (``` fun(Hola es decir "Hola ":: decir "mundo!") ```) y que hay dos tipos de separación de comandos:

1: con ;; para las intrucciones normales 
``` 
decir "Hola";; decir " ";; decir "Mundo";; decir "." 
```
2: con :: para dentro de las funciones
``` 
fun(Hola es decir "Hola ":: decir "mundo!") 
```

# Cosas interesantes

- Se puedes hacer variables con espacios. 
``` 
var Hola Mundo es "Feliz Jueves"
```

- Puedes dejar la variables de preg vacia.
```
preg([str])
```

- Decir pone texto en la misma linea. Por si no se entiende: decir
```
"Hola";; decir "Mundo"
```
da: 
```
HolaMundo
```
Para separar, se usa "^". 

```
decir "Hola^";; decir "Mundo"
```
da:
```
Hola
Mundo
```

Y creo que ya está.

# Archivos
Zinc, usa los archivos .zn.

# Desarrollo
Zinc se va a quedar en desarrollo por mucho tiempo.
No creo que esté actualizando frecuentemente.

# Versión actual
Es la v-0.1.
