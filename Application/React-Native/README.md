# React Natvive Troubleshooting Guide

<details>
  <summary><h3>error [Project Name] is not a valid name for a project. Please use a valid identifier name (alphanumeric).</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React Native CLI 프로젝트 생성 시 error 발생함
<br>
<b>원인</b> : 생성하는 프로젝트 이름이 유효하지 않아 발생
<br>
<b>해결 방안</b> : 생성하는 프로젝트 이름에서 하이픈(-) 제거
<br>
<b>참고 링크 : </b> [링크](https://success206.tistory.com/149)

</details>

<br>

<details>
  <summary><h3>error  Failed to install the app. Make sure you have the Android development environment set up</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React Native CLI 프로젝트 빌드 시 error 발생
<br>
<b>원인</b> : 빌드 시 버전 호환성으로 추정
<br>
<b>해결 방안</b> : 프로젝트 루트 경로의 package.json 수정하기
<br>
<b>참고 링크 : </b> [링크](https://pcloud.tistory.com/7)

</details>

<br>

<details>
  <summary><h3>npm ERR! 404 Not Found - GET https://registry.npmjs.org/react-natvie - Not found</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React-Natvie CLI로 프로젝트를 생성하기 위해 npx react-natvie init을 했는데 에러 발생
<br>
<b>원인</b> : React App 관련 Registry에 문제가 생김
<br>
<b>해결 방안</b> : React 제거 후 재설치
<br>
<b>참고 링크 : </b> [링크](https://ninearies.tistory.com/326)

</details>

<br>

<details>
  <summary><h3>Please consider installing 'jetifier' package before running 'jetify' command!</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : npm 빌드 시 해당 오류 발생
<br>
<b>원인</b> : npm 관련 Package가 설치되어 있지 않아 발생
<br>
<b>해결 방안</b> : npm -g install [Package Name]
<br>
<b>참고 링크 : </b> X

</details>


