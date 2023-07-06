# Flutter Troubleshooting Guide

<details>
  <summary><h3>VSCode에서 플러터 New Project 시 에러 발생</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : VSCode에서 플러터 New Project 시 에러 발생
<br>
<b>원인</b> : 생성하는 프로젝트 이름이 유효하지 않아 발생
<br>
<b>해결 방안</b> : 생성하는 프로젝트 이름에서 하이픈(-) 제거
<br>
<b>참고 링크 : </b> [링크](https://success206.tistory.com/149)

</details>

<br>

<details>
  <summary><h3>Pub get 시 Expected a key while parsing a block mapping. 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : pubspec.yaml 파일 Pub get 시 오류 발생
<br>
<b>원인</b> : 들여쓰기가 맞지 않아 발생
<br>
<b>해결 방안</b> : 들여쓰기 수정
<br>
<b>참고 링크 : </b> [링크](https://zionh.tistory.com/55)

</details>

<br>

<br>

<details>
  <summary><h3>이미지 추가 후 Exception caught by image resource service 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : pubspec.yaml 파일에 이미지 Path 정상으로 입력하였으나, 오류 발생
<br>
<b>원인</b> : pubspec.yaml 수정 후 pub get 안함
<br>
<b>해결 방안</b> : flutter pub get 명령어 실행
<br>
<b>참고 링크 : </b> X

</details>

<br>

<br>

<details>
  <summary><h3>flutter tts 추가 후 MissingPluginException 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : flutter tts 라이브러리 설치 후 빌드 시 오류 발생
<br>
<b>원인</b> : sdk 버전 오류
<br>
<b>해결 방안</b> : minSdkversion 19에서 21로 변경 후 실행
<br>
<b>참고 링크 : </b> X

</details>

<br>


<br>

<details>
  <summary><h3>화면에 BOTTOM OVERFLOWD BY PIXELS 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : 앱 실행 시 화면에 BOTTOM OVERFLOWD BY PIXELS 오류 표출됨
<br>
<b>원인</b> : 화면에 특정 위젯의 크기가 범위를 벗어나서 발생
<br>
<b>해결 방안</b> : Scaffold에 resizeToAvoidBottomInset : false 속성 추가
<br>
<b>참고 링크 : </b> [링크](https://woongnemonan.tistory.com/entry/%ED%94%8C%EB%9F%AC%ED%84%B0Flutter-Bottom-Overflowed-By-xx-pixels)

</details>

<br>