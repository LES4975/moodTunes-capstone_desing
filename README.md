# capstone-design-project-team_005

## 프로젝트 구조

프로젝트는 크게 `backend/`와 `frontend/`로 나뉘어져 있습니다.

- `backend/` : FastAPI 를 사용해 AI 모델을 서빙하는 서버
- `frontend/` : React 를 사용해 사용자와 상호작용하는 웹 페이지

```
capstone-design-project-team_005/
│
├── backend
│         ├── ai
│         └── model
├── frontend
│         ├── public
│         │         └── images
│         └── src
│             └── components
│                 ├── auth
│                 ├── home
│                 ├── layout
│                 ├── main
│                 └── mood-tunes
└── images
```

## 프로젝트 실행 방법

### backend

> 백엔드 프로젝트는 Python 과 FastAPI 를 사용합니다.
> 아래의 단계 수행 전, Python 이 설치되어 있어야 합니다.

`backend/` 디렉토리로 이동한 후 다음 명령어를 실행하여 가상 환경을 생성합니다.

```bash
$ python -m venv venv
```

그러면, `venv/` 디렉토리가 생성됩니다. 이제 가상 환경을 활성화합니다.

```bash
# windows 환경
$ venv\Scripts\activate

# macOS 또는 Linux 환경
$ source venv/bin/activate
```

가상 환경이 활성화되면, 다음 명령어를 실행하여 필요한 패키지를 설치합니다.

```bash
$ pip install -r requirements.txt
```

모든 패키지가 설치되면, 다음 명령어를 실행하여 서버를 실행합니다.

```bash
$ uvicorn main:app --reload
```

`http://127.0.0.1:8000/docs` 에 접속하여 API 문서를 확인할 수 있습니다.

![docs-example.png](docs-example/swagger.png)


### frontend

`frontend/` 디렉토리로 이동한 후 다음 명령어를 실행합니다.

```bash
$ npm install
$ npm start
```

`http://localhost:3000` 에 접속하여 웹 페이지를 확인할 수 있습니다.

![img.png](docs-example/fe-main.png)

## 프로젝트 기능

- AI 모델을 사용해 사용자의 감정을 분석합니다.
- 분석된 감정에 따라 음악을 추천합니다.
- 좋아요한 음악을 저장하고, 내 좋아요 목록을 확인할 수 있습니다.

![img_1.png](docs-example/recognition-and-recommend.png)

![img_2.png](docs-example/check-likes.png)

