# Visual Studio Code Troubleshooting Guide

<details>
  <summary><h3>VSCode에서 플러터 Chrome Run 시 crbug/1173575, non-JS module files deprecated. 에러 발생</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : VSCode에서 플러터 Chrome Run 시 crbug/1173575, non-JS module files deprecated. 에러 발생
<br>
<b>원인</b> : index.html의 path가 맞지 않아 발생
<br>
<b>해결 방안</b> : launch.json 파일에서 url 주석 후 경로 지정
```
    "version": "0.2.0",
    "configurations": [
        {
            "type": "chrome",
            "request": "launch",
            "name": "localhost에 대해 Chrome 시작",
            // "url": "http://localhost:8080",
            // "webRoot": "${workspaceFolder}"
            "file": "${workspaceFolder}/web/index.html"
        }
    ]
```
<br>

<b>참고 링크 : </b> [링크](https://m.blog.naver.com/kch8246/222648137463)

</details>

<br>
