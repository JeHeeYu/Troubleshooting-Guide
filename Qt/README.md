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
