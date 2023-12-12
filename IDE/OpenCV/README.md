# OpenCV Troubleshooting Guide

<details>
  <summary><h3>opencv_world[version].lib was not found</h3></summary>
  
<b>환경</b> : Windows11, Visual Studio 2019
<br>
<b>증상</b> : opencv 프로젝트 빌드 시 오류 발생
<br>
<b>원인</b> : 프로젝트 실행 시 dll 파일이 없어서 발생
<br>
<b>해결 방안</b> : 프로젝트 - 속성 - 링커 - 일반 - 추가 라이브 디렉터리에 opencv lib 경로 추가
```
경로 : C:\opencv\build\install\x64\vc16\lib
```
<b>참고 링크 : </b> X

</details>

<br>
