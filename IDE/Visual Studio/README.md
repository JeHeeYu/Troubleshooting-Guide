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


<details>
  <summary><h3>Visual Studio에서 빌드 시 빌드 도구 오류 발생</h3></summary>
  
<b>환경</b> : Windows11 / Visual Studio 2019
<br>
<b>증상</b> : Visual Studio에서 빌드 시 아래 오류 발생
```
v143에 대한 빌드 도구(플랫폼 도구 집합 = 'v143')를 찾을 수 없습니다. v143 빌드 도구를 사용하여 빌드하려면 v143 빌드 도구를 설치하십시오.  [프로젝트] 메뉴를 선택하거나 솔루션을 마우스 오른쪽 단추로 클릭한 다음 "솔루션 대상 변경"을 선택하여 현재 Visual Studio 도구로 업그레이드할 수도 있습니다.

```
<b>원인</b> : Visual Studio 에서 플랫폼 도구 집합이 설치되지 않은 버전이어 발생
<br>
<b>해결 방안</b> : 플랫폼 버전 도구 집합 버전 변경
<br>
<b>참고 링크 : </b> [링크](https://enjoy-coding-together.tistory.com/13)

</details>

<br>


<details>
  <summary><h3>openssl/ssl.h No such file or directory</h3></summary>
  
<b>환경</b> : Windows11 / Visual Studio 2019
<br>
<b>증상</b> : Visual Studio에서 빌드 시 ssl이 없다는 오류 발생
<br>
<b>원인</b> : Visual Studio 에서 openssl 환경설정이 되어 있지 않아 발생
<br>
<b>해결 방안</b> : Project 속성에 openssl 설정 추가
<br>
<b>참고 링크 : </b> [링크](https://playground10.tistory.com/188)

</details>

<br>
