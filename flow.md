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
