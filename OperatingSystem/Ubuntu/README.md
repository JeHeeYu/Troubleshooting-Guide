# Ubuntu Troubleshooting Guide

<details>
  <summary><h3>부팅 시 initramfs 표출 되며 부팅 안됨</h3></summary>

<b>환경</b> : Ubuntu 16.04 (Virtual Box)
<br>
<b>증상</b> : Virtual Box에서 기존 사용하던 우분투 부팅 하였으나 CLI 화면에서 부팅 되지 않음
<br>
<b>원인</b> : 시스템 종료 시 잘못된 종료로 인해 배드 블럭이 생김. 이 경우 리눅스 파티션이 날아가서 부팅하는 과정이 멈춰버린 것으로 추정
<br>
<b>해결 방안</b> : fsck 명령어로 부팅 파티션 경로 설정
```
// fsck -y [부팅 경로]
fsck -y /dev/sda1
```
<b>참고 링크 : </b> [링크](https://velog.io/@reveloper-1311/%EC%9A%B0%EB%B6%84%ED%88%AC-%EB%B6%80%ED%8C%85%EC%97%90%EB%9F%AC-initramfs)

</details>

<br>

<details>
  <summary><h3>Failed to fetch [URL] Hash error</h3></summary>

<b>환경</b> : Ubuntu 22.04, Docker Container
<br>
<b>증상</b> : 도커 컨테이너 환경에서 apt-get update 시 오류 발생
<br>
<b>원인</b> : apt cache가 남아 있어서 발생하는 것으로 추정
<br>
<b>해결 방안</b> : apt cache 삭제
```
rm -rf /var/lib/apt/lists/
apt-get clean
apt-get update
```
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>fatal error: json/json.h: No such file or directory</h3></summary>

<b>환경</b> : Ubuntu 22.04
<br>
<b>증상</b> : 리눅스 환경에서 json.h를 찾지 못함
<br>
<b>원인</b> : json 라이브러리 링크가 되어있지 않아 발생
<br>
<b>해결 방안</b> : json 라이브러리 링크
```
sudo ln -s /usr/include/jsoncpp/json/ /usr/include/json
```

<b>참고 링크 : </b> [링크](https://github.com/stardust95/TinyCompiler/issues/2)

</details>
