# instalar misspy
## Requisitos previos
misspy es compatible con Python3.8 y superior.

Python2 y Python3.7 y versiones anteriores no son compatibles.
## instalar

!!! Si instalas la versión de desarrollo
    Las nuevas funciones lanzadas en versiones futuras requerirán que se instale la versión de desarrollo hasta que se lance la versión estable.
    ```
    python3 -m pip instalar -U misspy --pre
    ```
    Usuarios de Windows:
    ```
    py -3 -m pip instalar -U misspy --pre
    ```
La biblioteca se puede obtener de PyPI.
```
python3 -m pip instalar -U misspy
```
Usuarios de Windows:
```
py -3 -m pip instalar -U misspy
```

# Concepto basico
misspy es un mecanismo para enviar solicitudes API por método.

Puede comenzar a utilizar misspy especificando al menos la dirección de la instancia.

Lo que devuelve misspy básicamente no es un tipo de diccionario, puede obtener el valor de una manera similar a la notación de puntos de JavaScript.
```
importar misspy

bot = misspy.Bot("mi.ejemplo.com")

meta = bot.meta()

imprimir(meta.nombre)
```