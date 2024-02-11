# React Natvive Troubleshooting Guide

<details>
  <summary><h3>error [Project Name] is not a valid name for a project. Please use a valid identifier name (alphanumeric).</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React Native CLI 프로젝트 생성 시 error 발생함
<br>
<b>원인</b> : 생성하는 프로젝트 이름이 유효하지 않아 발생
<br>
<b>해결 방안</b> : 생성하는 프로젝트 이름에서 하이픈(-) 제거
<br>
<b>참고 링크 : </b> [링크](https://success206.tistory.com/149)

</details>

<br>

<details>
  <summary><h3>error  Failed to install the app. Make sure you have the Android development environment set up</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React Native CLI 프로젝트 빌드 시 error 발생
<br>
<b>원인</b> : 빌드 시 JDK 버전 호환성으로 추정
<br>
<b>해결 방안</b> : JDK 버전 낮춤 (20 -> 11)
<br>
<b>참고 링크 : </b> 

</details>

<br>

<details>
  <summary><h3>npm ERR! 404 Not Found - GET https://registry.npmjs.org/react-natvie - Not found</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : React-Natvie CLI로 프로젝트를 생성하기 위해 npx react-natvie init을 했는데 에러 발생
<br>
<b>원인</b> : React App 관련 Registry에 문제가 생김
<br>
<b>해결 방안</b> : React 제거 후 재설치
<br>
<b>참고 링크 : </b> [링크](https://ninearies.tistory.com/326)

</details>

<br>

<details>
  <summary><h3>Please consider installing 'jetifier' package before running 'jetify' command!</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : npm 빌드 시 해당 오류 발생
<br>
<b>원인</b> : npm 관련 Package가 설치되어 있지 않아 발생
<br>
<b>해결 방안</b> : npm -g install [Package Name]
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>Render Error</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : 코드 실행 시 Render Error Text strings muse be rendered within a <Text> component.
<br>
<b>원인</b> : JSX 컴포넌트 문법 오류로 인해 발생, 태그 뒤에 ; 또는 / 위치 오류
<br>
<b>해결 방안</b> : 문법 수정
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>error Failed to launch emulator. Reason: No emulators found as an output of `emulator -list-avds`.</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : npm run android로 실행 시 오류 발생
<br>
<b>원인</b> : react-native가 시작되지 않아 발생
<br>
<b>해결 방안</b> : npx react-native start 후 npm run android 실행
<br>
<b>참고 링크 : </b> [링크](https://velog.io/@seewon/React-Native-1%EC%9D%BC%EC%B0%A8)

</details>

<br>

<details>
  <summary><h3>Invariant Violation: requireNativeComponent: "RNSScreen" was not found in the UIManager.</h3></summary>
  
<b>환경</b> : Windows React Native v0.76.8 Visual Studio Code
<br>
<b>증상</b> : Bottom Navigation 코드 추가 후 실행 시 오류 발생
<br>
<b>원인</b> : React Navigation 패키지가 설치되어 있지 않아 발생
<br>
<b>해결 방안</b> : React Navigation 패키지 설치
<br>
<b>참고 링크 : </b> [링크](https://talkwithcode.tistory.com/47)

</details>

<br>

<details>
  <summary><h3>Unable to start the daemon process.</h3></summary>
  
<b>환경</b> : Windows11 / React Native v0.73.10 / Visual Studio Code
<br>
<b>증상</b> : npm run start 시 오류 발생
<br>
<b>원인</b> : JVM 메모리가 부족하여 발생
<br>
<b>해결 방안</b> : JVM 메모리 재할당
```
// android\gradle.properties

// before
org.gradle.jvmargs=-Xmx2048m -XX:MaxMetaspaceSize=512m

// after
org.gradle.jvmargs=-Xmx512m -XX:MaxMetaspaceSize=512m
```
<br>

<b>참고 링크 : </b> [링크](https://tlshenm.tistory.com/37)

</details>

<br>

<details>
  <summary><h3>unable to load contents of file list xcfilelist</h3></summary>
  
<b>환경</b> : Mac / React Native v0.72.6 / Visual Studio Code
<br>
<b>증상</b> : npm run start 후 ios 시뮬레이터 실행 시 오류 발생
<br>
<b>원인</b> : pod 잔여 캐시가 클리어 되지 않아 발생
<br>
<b>해결 방안</b> : pod 클리어 후 update
```
cd ios
pod deintegrate
pod update
```
<br>

<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/56160460/error-unable-to-load-contents-of-file-list-target-support-files-pods-xx-pods)

</details>
