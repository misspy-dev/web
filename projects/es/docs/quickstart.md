# Inicio rápido

Misspy requiere una dirección de instancia para crear una instancia de una clase.

Además, la dirección de la instancia puede incluir opcionalmente el protocolo URL.
```
importar misspy

bot = misspy.Bot("mi.ejemplo.com")

bot_procotol = misspy.Bot("http://mi.example.com")
```

# usa la ficha
misspy requiere un token al ejecutar métodos como notes_create.
Se puede asignar en el momento de la creación de instancias.
```
importar misspy

bot = misspy.Bot("mi.ejemplo.com", i="token")
```

# correo
Puede crear una nota con la siguiente sintaxis.
También puede contener argumentos adicionales.[Consulte la documentación de misskey para esto.](https://misskey-hub.net/docs/api/endpoints/notes/create.html)
```
importar asincio

importar misspy

bot = misspy.Bot("mi.ejemplo.com")

asíncrono def misskeybot():
    note = await bot.notes_create("¡Hola mundo!")
    imprimir(nota.creadaNota.id)
    
asyncio.run(misskeybot())
```