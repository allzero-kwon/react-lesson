# React 프로젝트 구조 잡기 
## CRA 구조 
create-react-app 후 폴더 구조를 한번 살펴보자.

### node_modules
Node modules 은 설치한 npm package 들, 즉 프로젝트에서 사용하는 패키지들이 설치되는 폴더다.
이 node_modules 은 삭제하더라도, package.json 에 잘 정리되어 있다면 npm install 을 통하여 다시 생성할 수 있다. 

### Package.json
모든 node 프로젝트에서는 이 package.json 이 하나씩 존재하는데 이 package.json은 한마디로 "프로젝트의 모든 정보" 가 들어있는 파일이다. 
package.json 내부를 한번 살펴보자.

1) dependencies 
CRA 기본 패키지 외에 추가로 설치할 라이브러리(패키지) 정보
npm install 시, 여기에 기록한 패키지들이 버전에 맞게 설치된다. 버전이 없으면 최신 버전으로 설치된다. 

2) scripts 
말그대로 명령어 모음집이다. 기본적으로 start, build, test가 있는데 이는 사용자가 원하는대로 추가, 수정, 삭제 할 수 있다.

scripts의 명령어는 아래와 같이 사용할 수 있다. 
```npm {key} {args} (ex. npm start )``` 


### public 
우리가 브라우저에 접속했을 때 가장 먼저 보이는 index.html 을 포함하는 폴더로, 실제로 우리가 React App을 배포했을 때 배포되는 폴더이다. 
public에서는 Virtual DOM 을 담을 수 있는 틀을 세팅해두면 된다. 

### src
실제로 Virtual DOM 을 만들고 화면을 그리는 소스 폴더로, index.js 를 포함하고 있다. 진정한 React 코드들은 여기에 들어있다. 

1) assets 
Assets는 이미지, 비디오 등 리소스 파일들이 들어있는 폴더이다. 

2) components
이 폴더는 header, footer, nav와 같은 공통 컴포넌트를 관리하는 폴더이다.

3) pages 
Page 단위의 컴포넌트 폴더이다. Page와 컴포넌트를 헷갈릴 수 있는데, Page는 말그대로 사용자에게 **보여지는** 단위이고, 컴포넌트는 이 Page View를 구성하는 것 요소로써 보통 여러 페이지에서 반복적으로 사용될 경우 component 폴더로 옮겨 관리한다. 

### App.js
화면에 보여지고 있는 초기 컴포넌트로 react router를 설치하면 컴포넌트가 최상위 컴포넌트로 app.js 컴포넌트 자리에 위치하게 된다. 


### Styles
style 폴더는 말그대로 css 에서 적용할 수 있는 style 혹은 theme 들의 모음집이다. 

sass 사용시, reset.scss 에서 css를 초기화하고 common.scss 를 통해 공통으로 사용하는 css를 정의하는데 
이 때 sass(scss, syntatically awesome style sheets) 라고 css 코드를 효율적으로 작성할 수 있도록 도와주는 css 확장언어다.

styled component 사용시, 
GlobalStyle.js 로 css를 초기화하고, theme.js 를 통해 공통으로 사용하는 css 속성을 정의하면 된다. 

### Services 
js module 폴더 

### Utils
공통 함수, 유틸 등을 담는 폴더 

### context
context api 

### hoc 
함수형 컴포넌트들의 custom hooks 

### store 
관리할 정보가 많은 대형 프로젝트에서는 redux와 같은 전역상태 관리 라이브러리를 많이 사용하는데 store 폴더에 이를 저장하고 모듈화해서 관리하는 폴더라 생각하면 된다. 

일반적으로 actions, reducers, types 세가지 주요 부분으로 구성한다. 
Redux는 다음 스텝에서 배울거니 지금은 redux에서 쓴다! 정도만 알아놓으면 된다. 

