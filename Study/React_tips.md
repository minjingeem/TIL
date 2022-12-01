<h1>React 실행 및 Tips!</h1>

들어가기 앞서..



**React / Angular / Vue 사용하는 이유?**

Web-app을 쉽게 만들 수 있다.



**Web-app** 이란?

: 모바일 App처럼 스무스하게 동작하는 웹 ( 새로고침 없이 웹 탐색이 가능하다. )

: 모바일 앱으로 발행이 쉽다.

: 앱처럼 UX가 뛰어나다.

: 일반 웹사이트보다 구매율이 높아지는 비즈니스적 장점이 있다.



<h3 style = "color:orange">React 실행하기 전 준비 사항!</h3>

- **Node.js** 다운 

  - npm 툴을 통해 create-react-app 라이브러리를 사용할 수 있다.
  - **npm** 이란? jquery나 bootstrap 같은 라이브러리를 쉽게 설치할 수 있도록 도와주는 툴.

- ***npm***  :

  - Node.js 다운 받으면 자동 설치 되어 있음.

- ***npx*** 설치 

  ```java
  $ npm install npx -g
    
    또는
  
  $ sudo npm install npx -g
  ```



<h3>React 프로젝트 생성</h3>

``` java
// 프로젝트를 만들고 싶은 곳으로 경로 이동 후
$ npx create-react-app {project-title-here}

// {project-title-here} = 프로젝트 이름
```



<h3>React 프로젝트 실행</h3>

```java
$ npm start
```



<h3>파일 구조 둘러보기</h3>



***Index.html***

- 프로젝트에서 /public 에 위치한 기본 생성 파일로 , 이 곳에서 HTML 템플릿 , JavaScript의 컴포넌트를 조합하고 랜더링을 하여 화면상에 표시한다.

  

***index.js***

- 외부 모듈을 import하여 로드하는 곳.



***App.js***

- App.js는 실제로 화면에 표시되는 내용을 정의하는 공간이라고 생각하면 된다.
- App이라는 화살표 함수 내에서 사용자에게 보여질 변수 , 함수 그리고 랜더링할 엘리먼트 등을 정의하며 사용자에게 원하는 화면을 보여줄 수 있다.
- JSX 코드 작성.





<h3>VS Code 사용할때</h3>

- React Snippet Extension 인스톨

![Screen Shot 2022-11-23 at 16.06.51](/Users/minjinkim/Library/Application Support/typora-user-images/Screen Shot 2022-11-23 at 16.06.51.png)