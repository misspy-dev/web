# StreamingAPI 활용
misspy에서는, streamingAPI를 이용할 수 있는 메소드가 `misspy.Bot`에 구현되고 있습니다.
## 노트 수신
노트를 받기만 하면 다음 코드로만 구현할 수 있습니다.
``
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
``
## 노트 캡처
misspy를 사용하면 misskey의 게시물을 캡처 할 수 있습니다.
캡처는 다음 코드로 구현할 수 있습니다.
``
import misspy

class StreamingBot(misspy.Bot):

    async def on_ready(self):
        await self.connect("localTimeline")
        await self.subNote("noteId")

    async def on_reacted():
        print("reaction detected")

bot = StreamingBot("mi.example.com", i="token")
bot.run()
``
또한 캡처는 다음 방법으로 해제할 수 있습니다.
``
await self.unsubNote("noteId")
``