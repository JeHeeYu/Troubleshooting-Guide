# GitHub Troubleshooting Guide

<details>
  <summary><h3>error: failed to push some refs to [Git Link]</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : git push 명령어 실행 시 에러 발생
<br>
<b>원인</b> : 원격 저장소와 로컬 저장소의 상태가 서로 상이해서 발생
<br>
<b>해결 방안</b> : git pull 진행 후 push
<br>
<b>참고 링크 : </b> [링크](https://sosoeasy.tistory.com/406)

</details>

<br>

<details>
  <summary><h3>error: commit [Commit ID] is a merge but no m option was given revert</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : git revert [Commit ID] 입력 시 오류 발생
<br>
<b>원인</b> : 병합 커밋을 실제로 의미하는 것이 모호하여 git에서 거부하여 발생
<br>
<b>해결 방안</b> : git cat-file -p [Commit ID], git revert [Commit ID]  -m 1 or 2
```
got cat-file -p b13368f
git revert b13368f -m 1
```
<b>참고 링크 : </b> [링크](https://dev-syhy.tistory.com/44)

</details>

<br>

<details>
  <summary><h3>error: The following untracked working tree files would be overwritten by merge</h3></summary>
  
<b>환경</b> : Windows
<br>
<b>증상</b> : git pull 시 오류 발생
<br>
<b>원인</b> : origin branch와 local branch가 상이하여 발생
<br>
<b>해결 방안</b>
```
git add -A
git stash
git pull
```
<b>참고 링크 : </b> [링크](https://velog.io/@t1dmlgus/The-following-untracked-working-tree-files-would-be-overwritten-by-merge)

</details>

<br>

<details>
  <summary><h3>error: git authentication failed</h3></summary>
  
<b>환경</b> : Ubuntu 22.04
<br>
<b>증상</b> : git push 시 오류 발생
<br>
<b>원인</b> : token 등록이 되지 않아 발생
<br>
<b>해결 방안</b> : access token 등록
<b>참고 링크 : </b> [링크](https://wotres.tistory.com/entry/Github-%EC%97%90%EB%9F%AC-%ED%95%B4%EA%B2%B0%EB%B2%95-Authentication-failed-for-use-a-personal-access-token-instead)

</details>

<br>

<details>
  <summary><h3>unable to access [Project URL]: The requested URL returned error: 403</h3></summary>
  
<b>환경</b> : Ubuntu 22.04
<br>
<b>증상</b> : git push 시 오류 발생
<br>
<b>원인</b> : 링크에 권한이 없어 발생
<br>
<b>해결 방안</b> : access token 등록
<b>참고 링크 : </b> [링크](https://beagle-dev.tistory.com/244)

</details>

<br>

<details>
  <summary><h3>open(".vs/[프로젝트명]/v16/Browse.VC.opendb"): Permission denied</h3></summary>
  
<b>환경</b> : Windows 11
<br>
<b>증상</b> : git push 시 오류 발생
<br>
<b>원인</b> : Visual Studio 설정 문제로 인해 발생
<br>
<b>해결 방안</b> : Visual Studio 환경 설정 변
<b>참고 링크 : </b> [링크](https://songacoding.tistory.com/42)

</details>

<br>

<details>
  <summary><h3>error: object file .git/objects/52/fbac1a2981e0925b6fd0dd546a6cc35d9ae4cc is empty</h3></summary>
  
<b>환경</b> : Linux(Raspberry Pi)
<br>
<b>증상</b> : git pull 시 오류 발생
<br>
<b>원인</b> : git object 오류
<br>
<b>해결 방안</b> : git object 삭제 후 pull
<b>참고 링크 : </b> [링크](https://tyeolrik.github.io/git/2021/12/29/git-1-when-git-said-object-file-is-empty.html)

</details>

<br>

<details>
  <summary><h3>fatal: Not possible to fast-forward, aborting.</h3></summary>
  
<b>환경</b> : Linux(Raspberry Pi)
<br>
<b>증상</b> : git pull 시 오류 발생
<br>
<b>원인</b> : 리모트와 로컬의 브랜치가 fast-forward 관계가 아니어서 발생
<br>
<b>해결 방안</b> : git pull --rebase
<b>참고 링크 : </b> [링크](https://velog.io/@eunddodi/Not-possible-to-fast-forward-aborting.-%EC%97%90%EB%9F%AC-%ED%95%B4%EA%B2%B0)

</details>
