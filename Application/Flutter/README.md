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
