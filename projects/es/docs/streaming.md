# Usar API de transmisión
En misspy, `misspy.Bot` implementa un método que puede usar la API de transmisión.
## Recibir notas
Si solo desea recibir notas, puede implementarlo solo con el siguiente código.
```
importar misspy

clase StreamingBot(misspy.Bot):

    asíncrono def on_ready(yo):
        await self.connect("localTimeline")

    async def on_note(self, mensaje):
        imprimir("------------")
        imprimir (mensaje.texto)
        imprimir("------------")

bot = StreamingBot("mi.ejemplo.com", i="token")
bot.ejecutar()
```
## Capturando notas
misspy puede capturar publicaciones misskey.
Captcha se puede implementar con el siguiente código:
```
importar misspy

clase StreamingBot(misspy.Bot):

    asíncrono def on_ready(yo):
        await self.connect("localTimeline")
        espera self.subNote("noteId")

    asíncrono def on_reacted():
        imprimir("reacción detectada")

bot = StreamingBot("mi.ejemplo.com", i="token")
bot.ejecutar()
```
Además, la captura se puede cancelar con el siguiente método.
```
espera self.unsubNote("noteId")
```