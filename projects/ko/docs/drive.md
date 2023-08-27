# 파일 업로드
드라이브에 파일을 업로드하는 경우 다음 코드로 업로드할 수 있습니다.
``
import asyncio

import misspy

bot = misspy.Bot("mi.example.com", i="token")

async def misskeybot():
    with open(f"./file.png", "rb") as f:
        data = await bot.drive_files_create(f)
        print(data.id)
        
    
asyncio.run(misskeybot())
``

## 파일 삭제
드라이브에서 파일을 삭제하려면 `drive_files_delete`로 삭제할 수 있습니다.
``
import asyncio

import misspy

bot = misspy.Bot("mi.example.com", i="token")

async def misskeybot():
    await bot.drive_files_delete("fileId")
    
asyncio.run(misskeybot())
``