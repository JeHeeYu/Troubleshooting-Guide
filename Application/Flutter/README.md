# Flutter Troubleshooting Guide

<details>
  <summary><h3>VSCode에서 플러터 New Project 시 에러 발생</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : VSCode에서 플러터 New Project 시 에러 발생
<br>
<b>원인</b> : 생성하는 프로젝트 이름이 유효하지 않아 발생
<br>
<b>해결 방안</b> : 생성하는 프로젝트 이름에서 하이픈(-) 제거
<br>
<b>참고 링크 : </b> [링크](https://success206.tistory.com/149)

</details>

<br>

<details>
  <summary><h3>Pub get 시 Expected a key while parsing a block mapping. 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : pubspec.yaml 파일 Pub get 시 오류 발생
<br>
<b>원인</b> : 들여쓰기가 맞지 않아 발생
<br>
<b>해결 방안</b> : 들여쓰기 수정
<br>
<b>참고 링크 : </b> [링크](https://zionh.tistory.com/55)

</details>

<br>

<br>

<details>
  <summary><h3>이미지 추가 후 Exception caught by image resource service 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : pubspec.yaml 파일에 이미지 Path 정상으로 입력하였으나, 오류 발생
<br>
<b>원인</b> : pubspec.yaml 수정 후 pub get 안함
<br>
<b>해결 방안</b> : flutter pub get 명령어 실행
<br>
<b>참고 링크 : </b> X

</details>

<br>

<br>

<details>
  <summary><h3>flutter tts 추가 후 MissingPluginException 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : flutter tts 라이브러리 설치 후 빌드 시 오류 발생
<br>
<b>원인</b> : sdk 버전 오류
<br>
<b>해결 방안</b> : minSdkversion 19에서 21로 변경 후 실행
<br>
<b>참고 링크 : </b> X

</details>

<br>


<br>

<details>
  <summary><h3>화면에 BOTTOM OVERFLOWD BY PIXELS 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : 앱 실행 시 화면에 BOTTOM OVERFLOWD BY PIXELS 오류 표출됨
<br>
<b>원인</b> : 화면에 특정 위젯의 크기가 범위를 벗어나서 발생
<br>
<b>해결 방안</b> : Scaffold에 resizeToAvoidBottomInset : false 속성 추가
<br>
<b>참고 링크 : </b> [링크](https://woongnemonan.tistory.com/entry/%ED%94%8C%EB%9F%AC%ED%84%B0Flutter-Bottom-Overflowed-By-xx-pixels)

</details>

<br>

<br>

<details>
  <summary><h3>Chrome 환경에서 PageView Swipe 동작 안됨</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : Run 후 크롬에서 Swipe 동작 안됨
<br>
<b>원인</b> : 웹 환경에서는 어떤 동작인지 속성 지정 필요
<br>
<b>해결 방안</b> : scrollBehavior 속성 지정
```
class AppScrollBehavior extends MaterialScrollBehavior {
  @override
  Set<PointerDeviceKind> get dragDevices => {
        PointerDeviceKind.touch,
        PointerDeviceKind.mouse,
      };
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    print("Jehee");
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      initialRoute: RoutesName.home,
      onGenerateRoute: Routes.generateRoute,
      scrollBehavior: AppScrollBehavior(),   // scroll 속성 지정
    );
  }
}
```
<br>

<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/69424933/flutter-pageview-not-swipeable-on-web-desktop-mode)

</details>

<br>


<br>

<details>
  <summary><h3>uncaught referenceerror: _flutter is not defined</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : github로 웹 호스팅 시 화면 표출되지 않고 콘솔에서 uncaught referenceerror: _flutter is not defined 오류 발생
<br>
<b>원인</b> : index.html 오류
<br>
<b>해결 방안</b> : script 추가 및 href 수정
```
<base href="./">
<script src="main.dart.js" type="application/javascript"></script>
```



<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/72833719/getting-flutter-is-undefined-in-flutter-web-only-in-production)

</details>

<br>

<details>
  <summary><h3>XMLHttpRequest error</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : 플러터 웹(Chrome) 환경에서 Post 요청 시 에러 발생
<br>
<b>원인</b> : index.html 오류
<br>
<b>해결 방안</b> : flutter_tools.stamp 삭제 및 chrome.dart 수정
<br>
<b>참고 링크 : </b> [링크](https://youngwonhan-family.tistory.com/entry/FlutterDart-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0-Error-XMLHttpRequest-error)

</details>

<br>

<details>
  <summary><h3>Firebase 추가 후 빌드 시 Module was compiled with an incompatible version of Kotlin. The binary version of its metadata is 에러 발생</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : 플러터에서 Firebase 관련 패키지 추가 후 빌드 시 에러 발생
<br>
<b>원인</b> : Kotlin 버전과 Compose 버전이 서로 호환되지 않아 발생
<br>
<b>해결 방안</b> : Kotlin 버전 및 Compose 버전 수정
<br>
<b>참고 링크 : </b> [링크](https://yeons4every.tistory.com/26)

</details>

<br>

<details>
  <summary><h3>Unresolved reference: uppercase</h3></summary>
  
<b>환경</b> : Windows/Visual Stuido Code
<br>
<b>증상</b> : 플러터 빌드 시 Unresolved reference: uppercase 에러 발생
<br>
<b>원인</b> : Kotlin 1.5 버전 이하에서 uppercase() 메소드가 지원되지 않아 발생
<br>
<b>해결 방안</b> : Kotlin 버전을 1.5 이상으로 적용 후 빌드
<br>
<b>참고 링크 : </b> [링크](https://chosunghyun18.tistory.com/2)

</details>

<br>

<details>
  <summary><h3>(Android Studio) Unable to find bundled Java version.</h3></summary>
  
<b>환경</b> : Mac 
<br>
<b>증상</b> : 자바 버전 변경 후 터미널에서 flutter doctor 실행 시 오류 발생
<br>
<b>원인</b> : 안드로이드 스튜디오 JDK 경로 오류
<br>
<b>해결 방안</b> : 안드로이드 스튜디오 JDK 경로 재지정
<br>
<b>참고 링크 : </b> [링크](https://velog.io/@cafefarm-johnny/flutter-doctor-%EC%9D%B4%EC%8A%88-%EB%8C%80%EC%9D%91-%EB%AA%A9%EB%A1%9D)

<b>환경</b> : Windows 11
<br>
<b>증상</b> : 자바 버전 변경 후 터미널에서 flutter doctor 실행 시 오류 발생
<br>
<b>원인</b> : 안드로이드 스튜디오 JDK 경로 오류
<br>
<b>해결 방안</b> : jbr 전체 파일 복사 후 jre 폴더에 복사
<br>
<b>참고 링크 : </b> [링크](https://www.inflearn.com/questions/748519/window%EC%97%90%EC%84%9C-unable-to-find-bundled-java-version-%EC%97%90%EB%9F%AC-%EC%96%B4%EB%96%BB%EA%B2%8C-%ED%95%B4%EA%B2%B0%ED%95%98%EB%82%98%EC%9A%94-%E3%85%A0%E3%85%A0)

</details>

<br>

<details>
  <summary><h3>Could not open settings generic class cache for settings file</h3></summary>
  
<b>환경</b> : Mac 
<br>
<b>증상</b> : Flutter 버전 변경 후 오류 발생
<br>
<b>원인</b> : 자바 버전 호환성으로 인해 발생
<br>
<b>해결 방안</b> : 자바 버전 변경 (21 -> 17)
<br>
<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/67240279/could-not-open-settings-generic-class-cache-for-settings-file)

</details>

<details>
  <summary><h3>cmdline-tools component is missing</h3></summary>

<b>환경</b> : Windows 11
<br>
<b>증상</b> : flutter doctor 시 오류 발생
<br>
<b>원인</b> : 안드로이드 스튜디오에서 cmd tools가 다운로드되어 있지 않아 발생
<br>
<b>해결 방안</b> : cmd tools 다운로드

<img width="728" alt="image" src="https://github.com/JeHeeYu/Troubleshooting-Guide/assets/87363461/bfebf0e3-0db5-4d10-8eb4-66e634c4a065">


<br>
<b>참고 링크 : </b> [링크](https://www.inflearn.com/questions/748519/window%EC%97%90%EC%84%9C-unable-to-find-bundled-java-version-%EC%97%90%EB%9F%AC-%EC%96%B4%EB%96%BB%EA%B2%8C-%ED%95%B4%EA%B2%B0%ED%95%98%EB%82%98%EC%9A%94-%E3%85%A0%E3%85%A0)

</details>

<br>
