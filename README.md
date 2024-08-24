# How-to-set-up-Git
깃을 설정하는 방법을 정리해놨습니다.

> 명령어 정리 : https://beam-maru.tistory.com/116<br>
> 마크다운 정리 : https://abled.tistory.com/39<br>
> 리드미 꾸미기 : https://zzsza.github.io/development/2020/07/10/make-github-profile-readme/
---
![git_init](https://github.com/user-attachments/assets/b23c18f0-2db8-4467-84d2-610e995babe5)<br>
* 설치하고자 하는 폴더에 <strong>`[git init]`</strong> 을 한 후 <strong>`[user.name]`</strong>과 <strong>`[user.email]`</strong>을 작성하기<br>
---
![git_remote changeBranch_1](https://github.com/user-attachments/assets/3997918e-b358-44d1-9356-9c1b3ead03a9)<br>
* 연결하고자 하는 원격저장소를 remote한다 <em>(단, 브랜치 이름이 다르다면 브랜치 이름을 맞춰줘야함)</em><br>
  - `git remote add [이름][URL]` => 등록된 원격 저장소의 이름을 변경<br>
  - `git remote add origin 'URL'` => <strong>origin</strong>이라는 이름으로 URL에 대한 원격 저장소 연결<br>
<mark>위에 최초 커밋을 진행하지 않아 브랜치 생성이 되지 않음</mark><br>
---
![git_remote changeBranch_2](https://github.com/user-attachments/assets/60b1ff60-10fd-4a13-b2bf-e3b80de0677a)<br>
* 브랜치 생성을 위해 커밋을 진행<br>
---
![git_remote changeBranch_3](https://github.com/user-attachments/assets/2f0b9ba6-660d-4d92-b2b5-fb3c687158b1)<br>
* 커밋 완료 후 원격 저장소와 맞춰줄 브랜치 생성<br>
  - `git branch main` => <strong>main</strong>이라는 브랜치 생성<br>
  - `git branch` => 브랜치 확인<br>
  - `git checkout main` => <strong>main</strong>으로 브랜치 변경<br>
---
![git_push](https://github.com/user-attachments/assets/9c353a0a-1bae-4ed8-a7ba-0edaadc400e4)<br>
* 푸쉬하는 순서는 add -> commit -> push <br>
  - `git add [파일 혹은 디렉토리 경로]` => [파일 혹은 디렉토리]를 스테이징 영역으로 이동<br>
  - `git commit -m '[메모]'` => 스테이징 영역으로 이동한 파일들에 대한 변경사항을 남김<br>
  - `git push [remote] [branch]` => 로컬 저장소에서 원격 저장소로 이동  *-f : 강제실행<br>
---
![git_fetch pull](https://github.com/user-attachments/assets/7960f404-364a-4465-b493-60a5bb98fa86)<br>
* 원격 저장소에서 로컬 저장소로 가져올 때에는 fetch와 pull이 있다.<br>
  - `git fetch` => fetch는 원격 저장소에서 변경된 정보를 확인할 뿐 가져오지는 않는다.<br>
  - `git pull [remote] [branch]` => 원격 저장소에 변경된 내용 뿐 만 아니라 최신 정보도 로컬 저장소로 가져옴<br>
