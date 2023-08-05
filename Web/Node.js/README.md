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
