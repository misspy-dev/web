# Subir archivo
Si desea cargar un archivo en Drive, puede cargarlo con el siguiente código.
```
importar asincio

importar misspy

bot = misspy.Bot("mi.ejemplo.com", i="token")

asíncrono def misskeybot():
    con open(f"./file.png", "rb") como f:
        datos = esperar bot.drive_files_create(f)
        imprimir (datos.id)
        
    
asyncio.run(misskeybot())
```

## eliminar el archivo
Si desea eliminar archivos de su disco, puede eliminarlos con `drive_files_delete`.
```
importar asincio

importar misspy

bot = misspy.Bot("mi.ejemplo.com", i="token")

asíncrono def misskeybot():
    espere bot.drive_files_delete("fileId")
    
asyncio.run(misskeybot())
```