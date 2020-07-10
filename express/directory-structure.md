#  Express 디렉토리 구조



```
├── app.js
├── bin
│   └── www
├── package.json
├── public
│   ├── images
│   ├── javascripts
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
└── views
    ├── error.pug
    ├── index.pug
    └── layout.pug
```

###  app.js

- 미들웨어들을 담고 있는 곳

- express 객체를 생성하고, express 객체의 메서드를 통해 환경설정을 함
  - 정적 파일 호스팅
  - express 앱 내 모듈 사용관련 설정(http 요청을 받기위한 모듈, POST 요청 데이터 접근을 위한 모듈 등)

### bin/www

- **http 모듈**에 **express 모듈**을 연결하고, **포트를 지정**하는 부분
- .js 확장자가 붙어 있지 않음

### package.json

- 프로젝트에 필요한 노드 모듈, 프로젝트 관련 정보르 정의하는 파일

### public/

- Css, html 같은 정적 파일

### routes/index.js

- 요청에 대한 응답 처리(라우팅)를 하는 파일
- 응답할 때 웹 문서를 랜더링(res 객체의 render 메서드를 이용, 템플릿엔진 사용)할 수 있음

### views/

- 템플릿 엔진 관련 뷰 파일이 담길 디렉토리
- Routes 파일(routes/index.js)에서 라우팅을 처리, 요청에 대한 뷰 파일(자바스크립트 연산 결과 + 뷰 코드)를 응답

