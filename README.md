# ML-Setup
## 가상 환경 세팅(Virtual Environment)
### 가상 환경 구성
#### venv 모듈 활용
Python 버전 3 이상부터는 virtualenv라는 외부 패키지 없이 내장된 venv 모듈로 세팅이 가능합니다.

명령: `python -m venv .venv`

.venv 라는 폴더를 생성하고 그 하위에 파일들을 저장하도록 하는 명령입니다.

다른 이름으로 생성해도 상관 없지만, 관행적으로 .venv라는 이름을 쓴다고 합니다.

#### Git ignore 세팅

버전 관리는 필요하지 않으므로, .gitignore 세팅해주면 됩니다.

명령: `echo '.venv/' >> .gitignore`

### 가상 환경 활성화

VS Code의 PowerShell이 아닌, Command Prompt를 이용해 터미널을 열고 아래의 명령으로 실행합니다.

명령: `.venv\Scripts\activate.bat`

이때, 주의할 점은 `슬래시(/)`가 아닌, `역슬래시(\)`여야 한다는 것입니다.

터미널 앞쪽에 (.venv)가 추가되면, 가상 환경 활성화에 성공한 것입니다.

#### 확인

가상 환경에서 세팅된 파이썬 버전을 알아보기 위해 다음 명령을 실행합니다.

명령: `python --version`

### 가상 환경에 패키지 설치

#### 패키지 매니저(pip)

파이썬 패키지 매니저는 pip 명령을 이용해 설치합니다.(Package Installer for Python)

마찬가지로 다음 명령을 실행해 pip 버전도 확인 가능합니다.

명령: `pip --version`

nodejs를 설치하면 npm도 설치되어 사용 가능한 것처럼, Python을 설치하면 pip 매니저도 설치되는 것으로 보입니다.

#### 패키지 설치

다음 명령을 이용해, Express와 유사한 포지션의 Flask를 설치하고, 서빙해보겠습니다.

명령: `pip install flask`

### 서빙하기

#### app.py 

app.py를 작성하고, 아래와 같이 Hello, Flask! 출력을 시도합니다.


```
# app.py

from flask import Flask # Flask 모듈 import

# Flask 애플리케이션 생성
app = Flask(__name__)

# 루트 URL에 대한 핸들러
@app.route('/')
def hello():
    return 'Hello, Flask!'

# 서버 실행
if __name__ == '__main__':
    app.run()
```

#### 가상 환경에서 실행

아래의 명령을 실행해 가상 환경에서 서버를 실행했습니다.

명령: `python app.py`

![스크린샷](image.png)

잘 실행되는 모습입니다.

### 참조
https://www.daleseo.com/python-venv/

https://yeko90.tistory.com/entry/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EA%B8%B0%EC%B4%88-windows-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EA%B0%80%EC%83%81%ED%99%98%EA%B2%BD-%EC%84%A4%EC%A0%95-%EB%B0%A9%EB%B2%95-%EB%B0%B0%EC%9A%B0%EA%B8%B0