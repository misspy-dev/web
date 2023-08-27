# 빠른 시작

misspy에서는 클래스를 인스턴스화하기 위해 인스턴스 주소가 필요합니다.

또한 인스턴스 주소는 필요에 따라 URL 프로코틀을 포함할 수 있습니다.
``
import misspy

bot = misspy.Bot("mi.example.com")

bot_procotol = misspy.Bot("http://mi.example.com")
``

# 토큰 사용
misspy에서는 notes_create와 같은 메소드를 실행할 때 토큰이 필요합니다.
이것은 인스턴스화시에 대입할 수 있습니다.
``
import misspy

bot = misspy.Bot("mi.example.com", i="token")
``

# 게시
다음 구문으로 메모를 만들 수 있습니다.
또한 추가 인수를 포함할 수 있습니다.[이것은 misskey 문서를 참조하십시오.] (https://misskey-hub.net/docs/api/endpoints/notes/create.html)
``
import asyncio

import misspy

bot = misspy.Bot("mi.example.com")

async def misskeybot():
    note = await bot.notes_create("Hello, World!")
    print(note.createdNote.id)
    
asyncio.run(misskeybot())
``