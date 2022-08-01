### Create Project
React를 직접 해보기 위해 터미널을 열고, 아래와 같이 hello-react 라는 이름의 프로젝트를 만들어 보자. 

```bash
$ npx create-react-app 'hello-react'
Need to install the following packages:
  create-react-app
Ok to proceed? (y) y
npm WARN deprecated tar@2.2.2: This version of tar is no longer supported, and will not receive security updates. Please upgrade asap.

Creating a new React app in C:\Users\ekdud\OneDrive\바탕 화면\lessons\react\react-lesson\hello-react.

Installing packages. This might take a couple of minutes.
Installing react, react-dom, and react-scripts with cra-template...

[#######...........] \ idealTree:webpack-dev-server: sill fetch manif 
```

정상적으로, 프로젝트가 생성이 되었다면 아래와 같이 hello-react 라는 폴더가 보일 것이다.
이 폴더로 이동해서 실제로 프로젝트를 구동해보자. 


```bash
$ cd hello-react
$ ls
 node_modules/  package.json  package-lock.json  public/  README.md  src/

```

hello-react 라는 폴더로 이동하면 위와 같은 구조로 구성이 되어있는데, 
여기서 가장 중요한 파일은 package.json 이다.

package.json은 실제로 프로젝트를 빌드, 시작하기 위한 설정값들이 들어가 있는 파일이다. 

우리는 앞으로 이 package.json 이 있는 위치를 '프로젝트 루트 폴더' 혹은 'workspace' 라고 부를거다.

이제 일단 만들어진 프로젝트를 한번 구동시켜보자. 
Node 기반의 프로젝트에서는 프로젝트를 구동할 때 `npm start` 라는 명령어를 통해 프로젝트를 시작시킨다.

```bash
$ npm start

Compiled successfully!

You can now view hello-react in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://192.168.137.1:3000

Note that the development build is not optimized.
To create a production build, use npm run build.

webpack compiled successfully
```

실행이 되면 자동으로 chrome browser 에서 http://localhost:3000/ 열리며 실행이 될 것 이다.

여기까지 오느라 다들 수고하셨습니다. 
 React 라는 마라톤을 달리기 위한 신발끈 묶기가 끝이 났으니, 본격적으로 달려볼까요?
