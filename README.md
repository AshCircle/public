## Git-Tutorial

### Git 의 작동구조
#### 업로드
* Working directory
  * git add [Filename]
  * git add . (전부 add)
* Staging area
  * git commit -m "MESSAGE"
* Local repository
  * git push
  * git push -f (강제로 push)
* Remote repository (ex. Github)
#### 다운로드
* Remote repository (ex. Github)
  * git clone (프로젝트 통째로 다운로드)
  * git fetch (다른 사람이 작업한 데이터를 Local repository에 반영)
* Local repository
  * git merge (컴퓨터와 Remote repository가 동일하게 구성되도록 함.)
  * git pull (git fetch + git merge)

### Git with etc
* git status (작업중인(?) 파일 현황 확인)
* git restore [Filename] (파일 복구)
* git log (지금까지 로그 확인. Enter로 줄바꿈, q로 중단)
* git reset --hard [Hash] (특정 로그 이후를 삭제 후 그 전으로 돌아감. soft, mixed 옵션도 존재)
* git commit amend-- (unix 에디터로 commit 메시지 수정)
  * a (insert mode)
  * ESC (end insert mode)
  * :wq! (save and quit)

### Git with branch
* git branch (어떤 branch가 있는지 확인)
  * git branch [Branchname] (branch 생성)
  * git branch -d [Branchname] (branch 삭제)
* git switch [Branchname] (branch 변경)
* git merge [Branchname] (해당 branch를 master/main 브랜치에 병합)

### Git with Remote repository
* git remote (현재 등록된 원격 저장소 표시)
  * git remote show [Name] (특정 원격 저장소 정보 자세히 확인)
  * git remote add [Name] [Address] (새 원격 저장소 등록)
  * git remote -v (전체 원격 저장소 목록 확인)
  * git remote rename [CurrentName] [ChangeName] (원격 저장소 이름 변경)
  * git remote rm [Name] (원격 저장소 삭제)
* git log [RemoteRepo]/[Branch] (특정 원격저장소 지정 가능)
* git merge [RemoteRepo]/[Branch] (특정 원격저장소 지정 가능)
