# Node.js Troubleshooting Guide

<details>
  <summary><h3>Router.use() requires a middleware function but got a Object</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : node app 실행 시 오류 발생
<br>
<b>원인</b> : route 모듈을 export 하지 않아 발생
<br>
<b>해결 방안</b> : route 모듈 export
```
module.exports = router;
```
<b>참고 링크 : </b> [링크](https://yourknow.tistory.com/19)

</details>

<br>

<details>
  <summary><h3>pm2 : 이 시스템에서 스크립트를 실행할 수 없으므로 C:\Users\AppData\Roaming\npm\pm2.ps1 파일을 로드할 수 없습니다. 자세한 내용은 about_Execution_Policies(https://go.microsoft.com/fwlink/?LinkID=135170)를 참조하십시오.    
위치 줄:1 문자:1
+ ~~~
    + FullyQualifiedErrorId : UnauthorizedAccess</h3></summary>
  
<b>환경</b> : Windows 10 / node 16.14.0
<br>
<b>증상</b> : pm2 실행 시 오류 발생
<br>
<b>원인</b> : PowerShell의 실행 정책이 스크립트 실행을 차단하고 있기 때문에 발생, Windows PowerShell에서 기본적으로 설정된 실행 정책이 Restricted로 되어 있어 스크립트를 실행할 수 없음
<br>
<b>해결 방안</b> : 실행 정책을 RemoteSigned로 변경, 이는 PowerShell에서 로컬에서 생성된 스크립트를 실행할 수 있도록 허용
```
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```
<b>참고 링크 : </b> GPT

</details>

<br>
