# misspy 설치
## 전제 조건
misspy는 Python3.8 이상을 지원합니다.

Python2 또는 Python3.7 이전에는 지원되지 않습니다.
## 설치

!!! 개발 버전을 설치하는 경우
    향후 버전에서 릴리스되는 새로운 기능은 안정 버전이 릴리스될 때까지 개발 버전을 설치해야 합니다.
    ``
    python3 -m pip install -U misspy --pre
    ``
    Windows를 사용하는 경우 :
    ``
    py -3 -m pip install -U misspy --pre
    ``
라이브러리는 PyPI에서 얻을 수 있습니다.
``
python3 -m pip install -U misspy
``
Windows를 사용하는 경우 :
``
py -3 -m pip install -U misspy
``

# 기본 개념
misspy는 API 요청을 메소드로 보내는 메커니즘입니다.

최소한 인스턴스 주소를 지정하면 misspy 사용을 시작할 수 있습니다.

misspy로 반환되는 것은 기본적으로 사전 형식이 아니며 javascript의 점 표기법과 같은 방법으로 값을 얻을 수 있습니다.
``
import misspy

bot = misspy.Bot("mi.example.com")

meta = bot.meta()

print(meta.name)
``