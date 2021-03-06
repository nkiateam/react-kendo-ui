## React Kendo UI

### Examples
https://nkiateam.github.io/react-kendo-ui/examples/

### Getting Started

Just clone the repo and start hacking:

```shell
$ git clone https://github.com/nkiateam/react-kendo-ui.git
$ cd react-kendo-ui
$ npm install                   # Install Node.js components listed in ./package.json
$ npm run build                 # build
$ npm start                     # Compile and launch
```

### How to Build

```shell
$ npm run build                 # or, `gulp`
```

### How to Run

This will start a lightweight development server.

```shell
$ npm start                     # or, `npm start -- release`
```

### Usage

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import * as K from 'react-kendo-ui';

const App = () => (
  <div>
    <K.Grid url="./data/grid_page.json" height="250"
            columns={columns} pageable={true} filterable={true} />
  </div>
);

ReactDOM.render(
  <App />,
  document.getElementById('app')
);
```

### Documentation

  * **General**
    - [React Style Guide](./docs/react-style-guide.md)
    - [How to configure text editors and IDEs](./docs/how-to-configure-text-editors.md)
  * **Questions**
    - [Which module bundler should I use?](https://github.com/kriasoft/react-starter-kit/issues/3)
    - [Which Flux implementation should I use?](https://github.com/kriasoft/react-starter-kit/issues/22)
  * **Recipes**
    - [How to Implement Routing and Navigation](./docs/recipes/how-to-implement-routing.md)
    - [How to Integrate Disqus](./docs/recipes/how-to-integrate-disqus.md)

### Directory Layout

```
.
├── /dist/                      # The folder for compiled output
├── /esdoc/                     # Documentation API for react kendo ui
├── /guide/                     # Documentation guide for Documentation API
├── /examples/                  # Examples for react kendo ui
├── /node_modules/              # 3rd-party libraries and utilities
├── /src/                       # The source code of the application
│   ├── /components/            # React Kendo UI Components
│   ├── /i18n/                  # language configuration
│   ├── /utils/                 # Utility Function for React Kendo UI Components
│   ├── /index.js               # index
│   └── /umd.js                 # umd
├── gulpfile.js                 # gulp config file
├── package.json                # The list of 3rd party libraries and utilities
└── webpack.config.js           # webpack module builder config file
```


### 개발가이드 환경 구축 절차

```
- 사전 설치 프로그램
Git, node js(v4.6.1 LTS), visual studio code

- 절차
1) 소스 다운로드
특정 워크스페이스 폴더 생성후
git clone ssh://dca@cims.nkia.net:29418/react-puf.git

2) 필요한 라이브러리 설치(인터넷이 되는 환경이어야함)
npm install 
package.json에 설정되어 있는 라이브러리 설치됨

3) gulp 명령어를 글로벌하게 사용하기 위해 재설치
npm install gulp -g

4) 빌드
gulp
(빌드설정파일 : gulpfile.js)

5) http-server(웹서버) 실행
npm start

6) 개발 가이드 화면 호출
http://localhost:8080/
```