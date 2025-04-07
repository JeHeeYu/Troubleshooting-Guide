# CMake Troubleshooting Guide

<details>
  <summary><h3>CUDA_ARCHITECTURES is empty for target [Project Name]</h3></summary>
  
<b>환경</b> : Ubuntu 22.04
<br>
<b>증상</b> : CMake 빌드 시 오류 발생
<br>
<b>원인</b> : CUDA_ARCHITECTURES가 지정되어 있지 않아 발생
<br>
<b>해결 방안</b> : CMake 명령 시 인자 추가 또는 CUDA_ARCHITECTURES Set 추가
<br>
<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/67966258/cuda-architectures-is-empty-for-target-cmtc-28d80)

</details>

<br>
