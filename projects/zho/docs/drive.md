＃ 上传文件
如果您想将文件上传到云端硬盘，可以使用以下代码上传。
````
导入异步

导入小姐

bot = misspy.Bot("mi.example.com", i="token")

异步 def misskeybot():
    将 open(f"./file.png", "rb") 作为 f：
        数据 = 等待 bot.drive_files_create(f)
        打印（数据.id）
        
    
asyncio.run(misskeybot())
````

## 删除文件
如果您想从驱动器中删除文件，可以使用“drive_files_delete”删除它们。
````
导入异步

导入小姐

bot = misspy.Bot("mi.example.com", i="token")

异步 def misskeybot():
    等待 bot.drive_files_delete("fileId")
    
asyncio.run(misskeybot())
````