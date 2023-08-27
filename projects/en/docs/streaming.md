# Use Streaming API
In misspy, `misspy.Bot` implements a method that can use the streaming API.
## Receive notes
If you only want to receive notes, you can implement it with only the following code.
```
import misspy

class StreamingBot(misspy.Bot):

    async def on_ready(self):
        await self.connect("localTimeline")

    async def on_note(self, message):
        print("------------")
        print(message.text)
        print("------------")

bot = StreamingBot("mi.example.com", i="token")
bot.run()
```
## Capturing notes
misspy can capture misskey posts.
Captcha can be implemented with the following code:
```
import misspy

class StreamingBot(misspy.Bot):

    async def on_ready(self):
        await self.connect("localTimeline")
        await self.subNote("noteId")

    async def on_reacted():
        print("reaction detected")

bot = StreamingBot("mi.example.com", i="token")
bot.run()
```
Also, the capture can be canceled with the following method.
```
await self.unsubNote("noteId")
```