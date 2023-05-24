# Android Troubleshooting Guide

<details>
  <summary><h3>Manifest에서 다른 파일 조회 및 검색 안됨</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : Manifest에서 Activity 파일 조회 시 검색 안됨
<br>
<b>원인</b> : 적용할 Activity 파일에 package 등록 안됨
<br>
<b>해결 방안</b> : 적용할 Activity 파일에 package 등록
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>빌드 시 checkDebugDuplicateClasses 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : 빌드 시 checkDebugDuplicateClasses, duplicate class found 에러 발생
<br>
<b>원인</b> : 외부 라이브러리 사용 시 enableJetifier = true 등록이 안되어 발생
<br>
<b>해결 방안</b> : gradle.properties 에 enableJetifier=true 추가
<br>
<b>참고 링크 : </b> [링크](https://meoru-tech.tistory.com/22)

</details>
