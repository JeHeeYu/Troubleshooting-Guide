# MySQL Troubleshooting Guide

<details>
  <summary><h3>my.ini 파일 수정 시 권한 문제로 저장 안됨</h3></summary>

<b>환경</b> : Windows 10
<br>
<b>증상</b> : my.ini 파일 수정 후 저장 시 오류 발생
<br>
<b>원인</b> : 관리자 권한이 없어 파일 저장 불가능
<br>
<b>해결 방안</b> : my.ini 파일에 권한 부여
<br>
<b>참고 링크 : </b> [링크](https://nongue.tistory.com/75)

</details>

<br>

<details>
  <summary><h3>Cannot Connect to Database Server 오류 발생</h3></summary>

<b>환경</b> : Windows 10
<br>
<b>증상</b> : MySQL WorkBench 실행 후 Local instance MySQL80 클릭하니 아래 오류 발생
<br>
![image](https://github.com/JeHeeYu/Troubleshooting-Guide/assets/87363461/489ed7c8-5194-418c-8dac-8eb50f1b1ed8)
<br>
<b>원인</b> : MySQL 버전과 MySQL Workbench 버전이 상이해서 발생
<br>
<b>해결 방안</b> : my.ini 파일에 bind-address 입력 후 저장
<br>
<b>참고 링크 : </b> [링크](https://velog.io/@justdoplzz/mysql%EC%98%A4%EB%A5%98-Your-connection-attempt-failed-for-user-root-to-the-MySQL-server-at-localhost3306-Unable-to-connect-to-localhost-ERROR-10043-08S01-Bad-handshake)

</details>


<br>

<details>
  <summary><h3>could not acquire management access for administration</h3></summary>

<b>환경</b> : Windows 11
<br>
<b>증상</b> : MySQL WorkBench 실행 후 Server Status 클릭하니 아래 오류 발생
<br>
![image](https://github.com/user-attachments/assets/f2194aef-4329-4ec4-9cf2-4ecf6cea47d1)
<br>
<b>원인</b> : Window 환경의 64비트에서 chcp.com 파일을 찾지 못하여 MySQL 서버가 실행되지 못해 발생
<br>
<b>해결 방안</b> : 제어판 - 시스템 로캘 변경에서 UTF-8 설정 
<br>
<b>참고 링크 : </b> [링크](https://velog.io/@su-mmer/MySQL-Workbench-RuntimeError)

</details>
