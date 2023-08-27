＃ 快速开始

Misspy 需要一个实例地址来实例化一个类。

此外，实例地址可以选择包含 URL 协议。
````
导入小姐

bot = misspy.Bot("mi.example.com")

bot_procotol = misspy.Bot("http://mi.example.com")
````

# 使用令牌
misspy在执行notes_create等方法时需要令牌。
它可以在实例化时分配。
````
导入小姐

bot = misspy.Bot("mi.example.com", i="token")
````

＃ 邮政
您可以使用以下语法创建注释。
它还可以包含其他参数。[请参阅 misskey 文档了解这一点。](https://misskey-hub.net/docs/api/endpoints/notes/create.html)
````
导入异步

导入小姐

bot = misspy.Bot("mi.example.com")

异步 def misskeybot():
    note = wait bot.notes_create("你好，世界！")
    打印(note.createdNote.id)
    
asyncio.run(misskeybot())
````