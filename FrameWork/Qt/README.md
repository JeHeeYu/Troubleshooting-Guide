# Qt Troubleshooting Guide

<details>
  <summary><h3>Build or Run 시 error: undefined reference to `vtable for [File] 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : 코드 수정 후 Build 시 오류 발생하여 Build Fail 발생
<br>
<b>원인</b> : 새로운 파일 추가 후 moc 파일이 생성되지 않음. 즉 .pri 또는 .pro 파일의 변경 사항이 적용되지 않음
<br>
<b>해결 방안</b> : Clean - Run qmake 후 작업 진행
<br>
<b>참고 링크 : </b> [링크](https://codingcoding.tistory.com/320)

</details>

<br>

<details>
  <summary><h3>:No rule to make target [QML File Name], needed by 'qrc_qml.cpp'. Stop.</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : Build 시 오류 발생하여 Build Fail 발생
<br>
<b>원인</b> : 실제 폴더 및 파일 내용이 qml.qrc 안에 정의되어 있는 File Path와 상이하여 발생
<br>
<b>해결 방안</b> : qml.qrc와 실제 폴더 및 파일 내용 동일하게 수정
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>:[qml File Name + Code Line]: Duplicate method name</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : Run 시 qml 파일 로드되지 않음
<br>
<b>원인</b> : qml 내 function 중복 정의로 발생
<br>
<b>해결 방안</b> : function 중복 정의하지 않도록 수정
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>qt.network.ssl tls initialization failed 오류 발생</h3></summary>
  
<b>환경</b> : Windows 10, Qt5.12
<br>
<b>증상</b> : HTTP(GET) Method 호출 시 SSL Fail 오류 발생
<br>
<b>원인</b> : Qt - Open SSL 환경 변수 추가되지 않아 발생
<br>
<b>해결 방안</b> : Qt - Open SSL Path 추가
<br>

![image](https://github.com/JeHeeYu/Troubleshooting-Guide/assets/87363461/bf1ad91c-5cdb-4bbb-93e9-84b4a7c920e6)


<br>

<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/58625924/qt-error-message-qt-network-ssl-qsslsocketconnecttohostencrypted-tls-initia)

</details>

<br>

<details>
  <summary><h3>3DES 암호화 코드 추가 후 Build 시 qt undefined reference to symbol des_set_key@@openssl_1.0.2.d 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : <openssl/des.h> Header 추가 및 3DES 암호화 코드 추가 시 빌드 오류 발생
<br>
<b>원인</b> : .pro 파일에 LIB 추가하지 않아 발생
<br>
<b>해결 방안</b> : .pro 파일에 lcrypto 추가

```
LIBS += -lcrypto
```

<br>

<b>참고 링크 : </b> [링크](https://forum.qt.io/topic/72493/qt-and-openssl-compilation-undefined-reference/3)

</details>

<br>

<details>
  <summary><h3>QAbstractItemModel 클래스 상속 후 Build 시 invalid cast to abstract class type [Class Name] 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : 프로그램 Build 시 오류 발생
<br>
<b>원인</b> : QAbstractItemModel 상속 후 필수 메서드 Overriding 하지 않아서 발생
<br>
<b>해결 방안</b> : rowCount, data 메서드 재정의
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>QSqlDatabase 객체 사용 시 "Driver not loaded" 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 16.04, Qt5.12
<br>
<b>증상</b> : QSqlDatabase 객체 사용 시 오류 발생
<br>
<b>원인</b> : Database 타입을 지정하지 않아 발생
<br>
<b>해결 방안</b> : sql 변수 데이터베이스 타입 지정
```
QSqlDatabase::addDatabase("QSQLITE") 
```
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>Build 시 "cannot run compiler 'clang++'. output" 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 22.04, Qt5.12
<br>
<b>증상</b> : Windows에서 작업 하던 프로젝트를 Ubuntu에서 빌드 시 오류 발생
<br>
<b>원인</b> : clang이 설치 되어 있지 않아 발생
<br>
<b>해결 방안</b> : clang 설치
```
sudo apt-get install clang
```
<b>참고 링크 : </b> [링크](https://forum.qt.io/topic/99294/project-error-cannot-run-compiler-clang-output/8)

</details>

<br>

<details>
  <summary><h3>Run 시 "qt unknown module quick" 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 22.04, Qt5.12
<br>
<b>증상</b> : Windows에서 작업 하던 프로젝트를 Ubuntu에서 빌드 시 오류 발생
<br>
<b>원인</b> : qt dev 패키지가 설치 되어 있지 않아 발생
<br>
<b>해결 방안</b> : qt dev 패키지 설치 
```
sudo apt install qtdeclarative5-dev
```
<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/32052814/unknown-modules-in-qt-qml-quick)

</details>


<br>

<details>
  <summary><h3>Run 시 "plugin cannot be loaded for module "QtQuick.Controls": Cannot protect module QtQuick.Controls 2 as it was never registered" 오류 발생</h3></summary>
  
<b>환경</b> : Ubuntu 22.04, Qt5.12
<br>
<b>증상</b> : QtQuick.Controls import 부분에서 오류 발생
<br>
<b>원인</b> : qt dev 패키지가 설치 되어 있지 않아 발생
<br>
<b>해결 방안</b> : qt dev 패키지 설치 
```
sudo apt install qml-module-qtquick-controls2
```
<b>참고 링크 : </b> [링크](https://stackoverflow.com/questions/53374106/how-to-solve-module-qtquick-controls-version-2-0-is-not-installed-on-mac)

</details>


