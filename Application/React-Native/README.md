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
<br>

<details>
  <summary><h3>error  Failed to install the app. Make sure you have the Android development environment set up</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React Native CLI 프로젝트 빌드 시 error 발생
<br>
<b>원인</b> : grade build 버전 호환성이 맞지 않아 발생
<br>
<b>해결 방안</b> : gradle-wrapper.properties, build.gradle 에서 버전 수정
<br>
<b>참고 링크 : </b> [링크](https://genie247.tistory.com/m/entry/%EB%A6%AC%EC%95%A1%ED%8A%B8-%EB%84%A4%EC%9D%B4%ED%8B%B0%EB%B8%8C)

</details>
