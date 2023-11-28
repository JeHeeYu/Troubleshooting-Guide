# Android Troubleshooting Guide


<details>
  <summary><h3>Visual Studio에서 Darknet 빌드 시 오류 발생</h3></summary>
  
<b>환경</b> : Windows11 / Visual Studio 2022
<br>
<b>증상</b> : Visual Studio에서 빌드 시 아래 오류 발생
```
가져온 프로젝트 "C:\Program Files\Microsoft Visual Studio\2022\Community\MSBuild\Microsoft\VC\v170\BuildCustomizations\CUDA 11.1.props"을(를) 찾을 수 없습니다. Import 선언 "C:\Program Files\Microsoft Visual Studio\2022\Community\MSBuild\Microsoft\VC\v170\\BuildCustomizations\CUDA 11.1.props"의 식이 올바르고 디스크에 파일이 있는지 확인하세요.
```
<b>원인</b> : Visual Studio 에서 빌드할 때 Extention이 없어서 발생
<br>
<b>해결 방안</b> : CUDA 11.1.props 파일을 Visual Studio 경로에 복사
<br>
<b>참고 링크 : </b> [링크](https://ctkim.tistory.com/entry/yolo-v3v4-window-CUDA-100-props-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EB%A5%BC-%EC%B0%BE%EC%9D%84-%EC%88%98-%EC%97%86%EC%8A%B5%EB%8B%88%EB%8B%A4)

</details>

<br>


