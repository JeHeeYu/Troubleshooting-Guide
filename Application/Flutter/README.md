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

</details>

<details>
  <summary><h3>sdk does not contain 'libarclite' at the path</h3></summary>

<b>환경</b> : Mac / Visual Studio Code / Flutter 3.7.10
<br>
<b>증상</b> : Run 시 오류 발생
<br>
<b>원인</b> : Xcode 버전 업이 되면서 충돌 발생
<br>
<b>해결 방안</b> : Target 버전 명시

```
// 기존
post_install do |installer|
  installer.pods_project.targets.each do |target|
    flutter_additional_ios_build_settings(target)
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '5.0'  # required by simple_permission
      config.build_settings['ENABLE_BITCODE'] = 'NO'
      config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] ||= [
        '$(inherited)',
        ## dart: PermissionGroup.calendar
        'PERMISSION_EVENTS=0',

        ## dart: PermissionGroup.reminders
        'PERMISSION_REMINDERS=0',

        ## dart: PermissionGroup.contacts
        'PERMISSION_CONTACTS=0',

        ## dart: PermissionGroup.camera
        'PERMISSION_CAMERA=1',

        ## dart: PermissionGroup.microphone
        'PERMISSION_MICROPHONE=1',

        ## dart: PermissionGroup.speech
        'PERMISSION_SPEECH_RECOGNIZER=0',

        ## dart: PermissionGroup.photos
        'PERMISSION_PHOTOS=0',

        ## dart: [PermissionGroup.location, PermissionGroup.locationAlways, PermissionGroup.locationWhenInUse]
        'PERMISSION_LOCATION=0',

        ## dart: PermissionGroup.notification
         'PERMISSION_NOTIFICATIONS=0',

        ## dart: PermissionGroup.mediaLibrary
         'PERMISSION_MEDIA_LIBRARY=0',

        ## dart: PermissionGroup.sensors
         'PERMISSION_SENSORS=0',

        ## dart: PermissionGroup.bluetooth
        'PERMISSION_BLUETOOTH=0',
      ]
    end
  end
end


// 타겟 버전 추가
post_install do |installer|
  installer.pods_project.targets.each do |target|
    flutter_additional_ios_build_settings(target)
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
      config.build_settings['SWIFT_VERSION'] = '5.0'  # required by simple_permission
      config.build_settings['ENABLE_BITCODE'] = 'NO'
      config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] ||= [
        '$(inherited)',
        ## dart: PermissionGroup.calendar
        'PERMISSION_EVENTS=0',

        ## dart: PermissionGroup.reminders
        'PERMISSION_REMINDERS=0',

        ## dart: PermissionGroup.contacts
        'PERMISSION_CONTACTS=0',

        ## dart: PermissionGroup.camera
        'PERMISSION_CAMERA=1',

        ## dart: PermissionGroup.microphone
        'PERMISSION_MICROPHONE=1',

        ## dart: PermissionGroup.speech
        'PERMISSION_SPEECH_RECOGNIZER=0',

        ## dart: PermissionGroup.photos
        'PERMISSION_PHOTOS=0',

        ## dart: [PermissionGroup.location, PermissionGroup.locationAlways, PermissionGroup.locationWhenInUse]
        'PERMISSION_LOCATION=0',

        ## dart: PermissionGroup.notification
         'PERMISSION_NOTIFICATIONS=0',

        ## dart: PermissionGroup.mediaLibrary
         'PERMISSION_MEDIA_LIBRARY=0',

        ## dart: PermissionGroup.sensors
         'PERMISSION_SENSORS=0',

        ## dart: PermissionGroup.bluetooth
        'PERMISSION_BLUETOOTH=0',
      ]
    end
  end
end

```


<br>

<b>참고 링크 : </b> [링크](https://thoonk.tistory.com/103)

</details>

<br>


<br>

<details>
  <summary><h3>cocoapods did not set the base configuration</h3></summary>
  
<b>환경</b> : Mac 
<br>
<b>증상</b> : pod install 시 경고 발생
<br>
<b>원인</b> : *.xcconfig 파일이 현재 프로젝트 설정에 적용되어 있지 않기 때문에 CocoaPods가 적용되지 않았기 때문
<br>
<b>해결 방안</b> : ios > Flutter > Release.xcconfig 내용 추가

```
#include "Pods/Target Support Files/Pods-Runner/Pods-Runner.release.xcconfig"
#include "Pods/Target Support Files/Pods-Runner/Pods-Runner.profile.xcconfig"
```

<br>

<b>참고 링크 : </b> [링크](https://kim0617.tistory.com/314)

</details>

<br>


<br>

<details>
  <summary><h3>Archive 후 배포 시 Version 명 변경되지 않음</h3></summary>
  
<b>환경</b> : Mac 
<br>
<b>증상</b> : XCode에서 Identity - Version 명 변경해도 Archives 에서 버전 명 변경되지 않음
<br>
<b>원인</b> : X
<br>
<b>해결 방안</b> : Info.plist 에서 CFBundleShortVersionString, CFBundleVersion 수정

```
// 기존
	<key>CFBundleShortVersionString</key>
	<string>$(FLUTTER_BUILD_NAME)</string>

	<key>CFBundleVersion</key>
	<string>$(FLUTTER_BUILD_NUMBER)</string>

// 수정 후
	<key>CFBundleShortVersionString</key>
	<string>$(MARKETING_VERSION)</string>

	<key>CFBundleVersion</key>
	<string>$(CURRENT_PROJECT_VERSION)</string>
```

<br>

<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/74083027/flutter-ios-app-version-and-build-number-not-updating-when-archiving-in-xcode)

</details>

<br>

<details>
  <summary><h3> Error: Type 'UnmodifiableUint8ListView' not found. Error: Method not found: 'UnmodifiableUint8ListView'</h3></summary>

<b>환경</b> : Mac OS, flutter 3.27
<br>
<b>증상</b> : run 시 오류 발생
<br>
<b>원인</b> : UnmodifiableUint8ListView가 Dart 버전에 따라 사용되지 않음으로 인하여 발생
<br>
<b>해결 방안</b> : win32를 사용하지 않아 pubspec.lock 삭제 후 재실행

<br>

<b>참고 링크 : </b> [링크](https://studiodoc.tistory.com/182)

</details>

