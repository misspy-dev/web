# 使用流媒体 API
在misspy中，`misspy.Bot`实现了一个可以使用流API的方法。
## 接收笔记
如果你只想接收笔记，只需以下代码即可实现。
````
导入小姐

StreamingBot 类（misspy.Bot）：

    异步 def on_ready(self):
        等待 self.connect("localTimeline")

    异步 def on_note(self, 消息):
        打印（” -  -  -  -  -  - ”）
        打印（消息.文本）
        打印（” -  -  -  -  -  - ”）

bot = StreamingBot("mi.example.com", i="token")
机器人运行（）
````
## 捕获笔记
misspy 可以捕获 misskey 帖子。
验证码可以通过以下代码实现：
````
导入小姐

StreamingBot 类（misspy.Bot）：

    异步 def on_ready(self):
        等待 self.connect("localTimeline")
        等待 self.subNote("noteId")

    异步定义 on_reacted():
        print("检测到反应")

bot = StreamingBot("mi.example.com", i="token")
机器人运行（）
````
另外，可以通过以下方法取消捕捉。
````
等待 self.unsubNote("noteId")
````