# React

- React 공식 사이트 : https://reactjs.org/
- React 베타 문서 : https://beta.reactjs.org/
- Create React App : https://create-react-app.dev/
- HTML을 JSX로 변환 : https://transform.tools/html-to-jsx
- Box Shadow CSS : https://cssgenerator.org/box-shadow-css-generator.html

<hr/>

<details>
<summary>1. 리액트(React)</summary>
<div markdown="1">

## 개요
- 2013년도 페이스북에서 UI를 빠르게 만들고 사용자 이벤트에 즉각적으로 반응해서 UI를 업데이트하고 간편하게 어플리케이션을 만들기 위해 고안됨
- 심플한 정적 사이트부터 복잡한 규모까지 웹, 모바일앱을 손쉽게 만들 수 있음
- 유저 인터페이스를 만들기 위한 자바스크립트 라이브러리

1. SPA(Single Page Application)
- 사용자가 버튼을 클릭했을 때, 다른 페이지를 다운받아서 깜빡거리면서 리프레시 되는 것이 아니라 한 어플리케이션에서 컴포넌트를 보여주고 숨기는 방식으로 페이지 내에서 자유자재로 네비게이션하는 것

2. SCR(Client Server Rendering)
- 사용자가 웹 어플리케이션에 접속했을 때, 즉각적으로 html을 보여주는 것이 아니라, 우리가 작성한 코드 js뿐만 아니라 React 라이브러리도 함께 다운받아서 사용자 화면에 UI가 표기되기 때문에 Client측에서 리액트가 렌더링 됨
- React와 Gatsby 또는 Next.js 프레임워크를 함께 사용하면 SSG(Static Site Generation)과 SSR을 함께 구현할 수도 있음

### 리액트 철학
> Renders UI and responds to(Reacts to) events
> UI를 표기·보여주고나서 이벤트에 반응

### 라이브러리와 프레임워크

| 프레임워크                                                                         | 라이브러리                                                   |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| 개발하기 위해 필요한 모든 것들을 제공(UI, Routing, HTTP Clients, State management) | 큰 골격과 규칙이 정해지지 않고 작은 솔루션 단위              |
| 프레임워크에서 규정하고 있는 모든 것을 익여야 함                                   |                                                              |
| 자율성이 떨어짐                                                                    | 필요할 때 마다 원하는 것만 골라서 사용할 수 있는 자율성 보장 |

</div>
</details>

<details>
<summary>2. 컴포넌트(Components)</summary>
<div markdown="1">

## 2. 컴포넌트란?

> 다른 컴포넌트들과는 연결되어 있지 않은 독립적인 응집도가 높은 UI 블록 </br>
> 독립적(independent), 고립적(isolated), 재사용성(resuable)

### 2.1. 컴포넌트 단위

- 재사용성DRY(Don't Repeat Yourself)
- 단일책임SR(Single Responsibility): 비록 재사용할 확률은 낮더라도 한 컴포넌트 안에 너무 많은 UI나 로직 등 정보가 많다면 작은 단위로 한 UI에서는 하나의 도메인을 담당해서 보여줄 수 있도록 분리

### 2.2. 컴포넌트 정의

        1) 함수 형태로 만드는 컴포너트를 함수형 컴포넌트
        2) 함수 반환 값으로 html처럼 생긴 마크업을 반환, 이것을 JSX(JavaScript XML)
        3) 컴포넌트가 가지고 있는 데이터(상태)는 useState라는 함수를 사용해서 변수형태로 상태값을 저장
        4) 외부에서 전달되는 값은 props(properties)라는 함수의 인자로 전달됨
        5) State  : 컴포넌트의 내부 상태
           Props  : 외부로 전달받은 상태
           Render : 두가지를 표기, 나타냄

### 2.3. 컴포넌트 개발시 주의사항

1. 컴포넌트는 한 개 이상의 요소(태그)를 반환해야 함
2. 다수의 태그를 반환하고 싶다면 부모태그로 감싸야 함
3. JSX에서의 요소의 클래스명은 className
4. 값에 접근하거나 자바스크립트 코드를 작성할 때는 중괄호{} 사용
5. 컴포넌트일 경우 확장자명을 jsx로 하여 js파일과 구분 가능

</div>
</details>

<details>
<summary>3. 훅(Hooks)</summary>
<div markdown="1">

## 3. 리액트의 훅(Hooks)

> - 리액트의 State와 Life Cycle에 관련된 기능을 '갈고리'처럼 연결할 수 있는 재사용 가능한 로직들 </br>
> - Hooks은 재사용 가능한 함수를 뜻함(대개 use로 시작함 ex: useState, useEffect…)</br>
> - Hooks(함수들)의 목적은 값의 재사용이 아닌 로직의 재사용을 위한 것

</div>
</details>

<details>
<summary>4. 툴(Tools)</summary>
<div markdown="1">

## 4. 툴(Tools)

### 4.1. 프로젝트 구조

| 제목            | 내용                                                       |
| --------------- | ---------------------------------------------------------- |
| .yarn           | yarn을 실행하는 데 필요한 모듈                             |
| node_modules    | npm을 이용해서 설치하는 라이브러리                         |
| pnp             | yarn에서 도입한 프로젝트 버전정보, PC 설치정보 등          |
| yarn.lock       | 라이브러리 버전 파일 정보                                  |
| └ index.html    | react app에서 사용하는 head정보, root요소                  |
| └ manifest.json | pwa에 필요한 정보들                                        |
| └ robots.txt    | 배포했을 때, 크롤링하는 로봇들에게 사이트에 대한 정보 명시 |
| public          | static한 resources                                         |
| src             | 동적으로 코드를 작성하는 곳                                |

### 4.2. 중요한 툴

    1. Webpack: (어플리케이션코드+리액트코드)코드를 잘 포장해서 사용자들에게 배포하는 모듈 번들러
    2. ESLint: 코드를 올바르게 작성하고 있는지 체크
    3. Jest: Unit 테스트를 작성하고 테스팅을 할 수 있는 프레임워크
    4. PostCSS: JS로 CSS를 변환하는 툴

### 4.3. 브라우저 준비 및 익스텐션

#### 4.3.1. 크롬 확장프로그램

    - React Developer Tools: 개발자 도구에서 컴포넌트 단위로 요소 확인 가능

#### 4.3.2. VSCode Extention

    1. Material Theme: 현재 사용하고 있는 테마(dark)
    2. Material Icon Theme: 현재 사용하고 있는 아이콘
    3. Auto Import: 자동으로 import
    4. Prettier - Code formatter: 코드를 이쁘게 포맷
    5. CSS Modules: 나중에 PostCSS 쓸때 유용

#### 4.2.3. 기타 HTML&CSS 관련 익스텐션

    1. IntelliSense for CSS class names in HTML
    2. HTML to CSS autocompletion
    3. HTML CSS Support
    4. CSS Peek
    5. Auto Rename Tag

#### 4.2.4. 리액트 Snippets

[Ctrl + P] → [>Snippets: Configure User Snippets] → [New Global Snippets file...] → file name: [global.code-snippets.json]

```
{
  "reactFunction": {
    "prefix": "rfc",
    "body": "import React from 'react';\n\nexport default function ${1:${TM_FILENAME_BASE}}() {\n\treturn (\n\t\t<div>\n\t\t\t\n\t\t</div>\n\t);\n}\n\n",
    "description": "Creates a React Function component"
  },
  "reactStatelessImplicitReturn": {
    "prefix": "rsi",
    "body": "import React from 'react';\n\nexport const ${1:${TM_FILENAME_BASE}} = (props) => (\n\t\t\t$0\n\t);",
    "description": "Creates a React Function component"
  },
  "Import Module CSS": {
    "prefix": "si",
    "body": ["import styles from './$TM_FILENAME_BASE.module.css'"],
    "description": "Import PostCSS"
  },
  "ClassName": {
    "prefix": "cn",
    "body": ["className={styles.$1}"],
    "description": "Adding className"
  }
}

```

</div>
</details>

<details>
<summary>5. Virtual DOM Tree</summary>
<div markdown="1">

> - HTML 코드를 작성 후 실행하면 브라우저에서는 웹 페이지 구조를 DOM Tree 형태로 잡음
> - 리액트는 곧바로 부라우저 DOM Tree를 건드리는 것이 아니라 가상의 Virtual DOM Tree를 가지고 어떤 상태 값이 변경되어 업데이트가 될 때, 바로 DOM Tree에 업데이트 하지 않고, 이 전의 Previous Tree와 비교 후 다른 점에 대해서만 브라우저에 DOM Tree에 업데이트를 진행
> - 그래서 어플리케이션에서 State를 아무리 많이 변경시킨다 하더라도 브라우저에서는 최종적으로 업데이트 되는 노드만 진행하기 때문에 리액트가 조금 더 효율적이며 빠름
> - 상태가 변경될 때 마다 re-render
> - 실제로 변경된 부분만 화면에 업데이트

</div>
</details>
