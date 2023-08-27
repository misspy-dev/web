# 安装小姐
## 先决条件
misspy支持Python3.8及以上版本。

不支持 Python2 和 Python3.7 及更早版本。
＃＃ 安装

!!! 如果你安装的是开发版
    未来版本发布的新功能将需要安装开发版本，直到稳定版本发布。
    ````
    python3 -m pip install -U misspy --pre
    ````
    Windows 用户：
    ````
    py -3 -m pip install -U misspy --pre
    ````
该库可以从 PyPI 获取。
````
python3 -m pip install -U misspy
````
Windows 用户：
````
py -3 -m pip install -U misspy
````

＃ 基本概念
misspy是一种通过方法发送API请求的机制。

您可以通过至少指定实例地址来开始使用 misspy。

misspy返回的基本上不是字典类型，你可以通过类似javascript点表示法的方式获取值。
````
导入小姐

bot = misspy.Bot("mi.example.com")

元 = bot.meta()

打印（元名称）
````