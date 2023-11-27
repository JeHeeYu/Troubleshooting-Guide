# CMake Troubleshooting Guide

<details>
  <summary><h3>error in configuration process project files may be invalid</h3></summary>
  
<b>환경</b> : Windows 11
<br>
<b>증상</b> : CMake에서 Visual Studio 및 OpenCV 설정 시 오류 발생
<br>
<b>원인</b> : index.html의 path가 맞지 않아 발생
<br>
<b>해결 방안</b> : .vscode/launch.json 파일 삭제
<br>
<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/67561515/crbug-1173575-non-js-module-files-deprecated-error-in-flutter)

</details>

<br>
