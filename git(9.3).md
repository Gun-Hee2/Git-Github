## git pull

-----------------------------

* git pull origin master : github의 레포지터리(repository)에서 수정되거나 새로 만들어진 파일(폴더)를 로컬저장소로 가져올 수 있다.

-> 로컬저장소에서 github의 레포지터리에 push를 하고 싶은데  github의 수정된 파일이나 새로운 파일이 있을 면 push가 안되므로 반드시 pull을 먼저 해주고 push를 해주어야 한다.

## .gitignore

-------

* .gitignore으로 원하지않는 파일은 제외를 할 수 있다.
  * 파일명.확장자 \# 특정 파일
  * 폴더명/  \# 특정 폴더
  * *.확장자 \# 특정 확장자
  * !파일명.확장자 \# 파일명에 해당되는 확장자를 제외하고 확장자에 해당되는 모든 파일은 제외한다.

## branch

------------

브랜치는 나뭇가지, 분기된 흐름을 뜻하며 git내에서는 특정 커밋을 가리키는 '포인터'로 생각하면 좋다.  

보통 브랜치는 마스터 브랜치는 두고 따로 브랜치를 생성해서 개발하고 나중에 마스터 브랜치와 merge해준다.

### Branch basic commands

* 1.브랜치 생성

  `(master) $ git branch 브랜치명`

* 2.브랜치 이동

  `(master) $ git checkout 브랜치명`

* 3.브랜치 생성 및 이동

  `(master) $ git checkout -b 브랜치명`

* 4.브랜치 목록

  `(master) $ git branch`

* 5.브랜치 삭제

  `(master) $ git branch -d 브랜치명`

## Branch merge

------------------

각 branch에서 작업을 한 이후 메인 브랜치와 이력을 합치기 위해서는 일반적으로 merge 명령어를 사용한다.

병합을 진행할 때,  만약 서로 다른 commit에서 동일한 파일을 수정한 경우 conflict(충돌)이 발생할 수 있다.

이 경우에는 반드시 직접 수정을 진행 해야 한다.

충돌이 발생한 것은 오류가 발생한 것이 아니라 이력이 변경되는 과정에서 반드시 발생할 수 있다는 것이다.

* Branch merge - fast-forward

  기존 master 브랜치에 변경사항이 없어 단순히 앞으로 이동

  1. feature-a branch(새로 생성한 브랜치)로 이동 후 commit
  2. master branch는 별도 변경 없음
  3. master branch로 merge

* Branch merge (merge commit case)

  기존 master 브랜치에 변경사항이 있어 병합 커밋 발생

  1. feature-a branch(새로 생성한 브랜치)로 이동 후 commit
  2. master branch commit
  3. master branch로 merge

  ` (master) $ git merge feature-a`

## Git Flow

-------------------

Git을 활용하여 협업하는 흐름으로 branch를 활용하는 전략을 의미한다.

Git Flow는 정해진 답은 없다. Github Flow, Gitlab Flow 등의 각 서비스별 제안되는 흐름이 있으며,

변형되어 각자의 프로젝트/회사에서 활용되고 있다.

* Github Flow 기본 원칙
  1.  master branch는 반드시 배포 가능한 상태여야 한다.
  2.  feature branch(새로 생성한 브랜치)는 각 기능의 의도를 알 수 있도록 작성한다.
  3.  Commit message는 매우 중요하며, 명확하고 알아보기 쉽게 작성한다.
  4.  Pull Request를 통해 협업을 진행한다.
  5. 변경사항을 반영하고 싶다면, master branch에 병합한다.













