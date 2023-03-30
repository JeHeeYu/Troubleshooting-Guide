# Qt Troubleshooting Guide

<details>
  <summary><h3>Build or Run 시 error: undefined reference to `vtable for [File] 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : 코드 수정 후 Build 시 오류 발생하여 Build Fail 발생
<br>
<b>원인</b> : 새로운 파일 추가 후 moc 파일이 생성되지 않음. 즉 .pri 또는 .pro 파일의 변경 사항이 적용되지 않음
<br>
<b>해결 방안</b> : Clean - Run qmake 후 작업 진행
<br>
<b>참고 링크 : </b> [링크](https://codingcoding.tistory.com/320)

</details>

<br>

<details>
  <summary><h3>:No rule to make target [QML File Name], needed by 'qrc_qml.cpp'. Stop.</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : Build 시 오류 발생하여 Build Fail 발생
<br>
<b>원인</b> : 실제 폴더 및 파일 내용이 qml.qrc 안에 정의되어 있는 File Path와 상이하여 발생
<br>
<b>해결 방안</b> : qml.qrc와 실제 폴더 및 파일 내용 동일하게 수정
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>:[qml File Name + Code Line]: Duplicate method name</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : Run 시 qml 파일 로드되지 않음
<br>
<b>원인</b> : qml 내 function 중복 정의로 발생
<br>
<b>해결 방안</b> : function 중복 정의하지 않도록 수정
<br>
<b>참고 링크 : </b> X

</details>
