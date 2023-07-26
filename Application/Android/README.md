# Android Troubleshooting Guide

<details>
  <summary><h3>Manifest에서 다른 파일 조회 및 검색 안됨</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : Manifest에서 Activity 파일 조회 시 검색 안됨
<br>
<b>원인</b> : 적용할 Activity 파일에 package 등록 안됨
<br>
<b>해결 방안</b> : 적용할 Activity 파일에 package 등록
<br>
<b>참고 링크 : </b> X

</details>

<br>

<details>
  <summary><h3>빌드 시 checkDebugDuplicateClasses 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : XML에서 ConstraintLayout안에 LinearLayout 추가 시 오류 발생
<br>
<b>원인</b> : 외부 라이브러리 사용 시 enableJetifier = true 등록이 안되어 발생
<br>
<b>해결 방안</b> : gradle.properties 에 enableJetifier=true 추가
<br>
<b>참고 링크 : </b> [링크](https://meoru-tech.tistory.com/22)

</details>

<br>

<details>
  <summary><h3>This view is not constrained. It only has designtime positions, so it will jump to (0,0) at runtime unless you add the constraints 오류 발생</h3></summary>
  
<b>환경</b> : Windows/Android Studio
<br>
<b>증상</b> : ConstraintLayout의의 자식 뷰가 제약 조건이 없어 발생
<br>
<b>원인</b> : ConstraintLayout의 자식 뷰들은 최소 하나의 수평 또는 수직 제약 조건 필수
<br>
<b>해결 방안</b> : 아래와 같이 제약 조건 추가
```
app:layout_constraintTop_toBottomOf="parent"
app:layout_constraintStart_toStartOf="parent"
```
<b>참고 링크 : </b> X

</details>
