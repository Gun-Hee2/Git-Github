# Git

-----------------------------------------------------------------------------------------

git이란 분산 버전 관리 시스템이라고 한다.

* 코드의 히스토리(버전)을 관리하는 도구
* 개발되어온 과정 파악 가능
* 이전 버전과의 변경 사항 비교 및 분석 가능

Git != Github

git은 분산 버전 관리 시스템이며, github는 git 기반의 저장소 서비스이다.

git은 명령어를 통해서 사용한다. (CLI: Command-Line Interface)

* 간단한 Unix/Linux 명령어
  - 현재 위치의 폴더, 파일 목록 보기 : Is
  - 현재 위치 이동하기 : cd \<path\> , cd ..(상위폴더로 이동)
  - 폴더 생성하기 : mkdir \<name\>
  - 파일 생성하기 : touch \<name\>
  - 삭제하기 : rm \<name\> (파일 삭제하기) , rm -r \<name\> (폴더 삭제하기)

## Repository

------------------------------------------------------------------------------------------------------------

특정 디렉토리를 버전 관리하는 저장소

* git init 명령어로 로컬 저장소를 생성
* 생성한 로컬 저장소 .git 디렉토리에 버전 관리에 필요한 모든 것이 들어있다.

## Commit

-------------------------------------------------------------------------------------------------------------------

commit은 특정 버전으로 남기는것을 의미하며 3가지 영역을 바탕으로 동작한다.

* Working Directory : 내가 작업하고 있는 실제 디렉토리
* Staging Area : 커밋(commit)으로 남기고 싶은, 특정 버전으로 관리하고 싶은 파일이 있는 곳
* Repository : 커밋(commit)들이 저장되는 곳

### *  git 명령어(commit)

git status : 현재 git으로 관리되고 있는 파일들의 상태를 알 수 있다.

git add 파일명 : Working Directory에서 추가 하고 싶은 파일을  Staging Area 으로 추가해준다.   

git commit -m "commit 메세지" : Staging Area에서 Repository로 commit을 해주며 commit메세지를 남긴다.   

### * git 명령어

- 이메일 적용 : **git config --global user.email "asd@asd.com"**
- 이름 적용 : **git config --global user.name "user name"**
- Github와 로컬 연결하기 : **git remote add origin {remote_repo}**

- Commit한 이력을 업로드 : **git push -u origin master**

  

- 커밋 했던 기록 :  **git log**

- 저장 했던 내용 비교 :  **git diff**









