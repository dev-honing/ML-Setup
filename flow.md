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

이때, 주의할 점은 일반 슬래시(/)가 아닌, 역슬래시(\)여야 한다는 것입니다.

터미널 앞쪽에 (.venv)가 추가되면, 가상 환경 활성화에 성공한 것입니다.

#### 확인

가상 환경에서 세팅된 파이썬 버전을 알아보기 위해 다음 명령을 실행합니다.

명령: `python --version`
