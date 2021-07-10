# Git-Tutorial

깃허브 사용법

1. git 환경설정

**cmd창에서**
- git config —global user.name [내 계정]
- git config —global user.email [내 이메일 주소]

git clone [repositive git 주소] --> git 소스코드를 다운로드 받을 때 사용

![image](https://user-images.githubusercontent.com/78203399/113874933-3cecda80-97f1-11eb-8b4d-4b844fecc934.png)

- Working Directory : 작업할 파일이 있는 디렉토리
- Staging Area : 커밋(commit)을 수행할 파일들이 올라가는 영역
- Git Directory: Git 프로젝트의 메타 데이터와 데이터 정보가 저장되는 디렉토리

※ git fetch와 git merge과정은 git pull을 통해 한꺼번에 이루어 질 수 있다. (다운로드 개념과 비슷)

* git status : 저장 영역에서의 현재 상태를 나타냄 (변경되거나 새로운 파일이 들어와 있는지 등)

* git add [파일 명] : 저장 영역에 파일을 추가 저장
(파일명 = . 일 경우 해당 파일에 있는 모든 파일 저장 영역에 저장)
* git reset [파일 명] : 저장 영역에 저장되어있던 파일 제거 
* git commit –m “[커밋 이름]” : local repository에 저장한다.
* git push : remote Repositoy에 저장 (즉, 깃허브에 저장된다.) 
* -f: 끝에 해당문자를 사용 시 강제적으로 저장된다. 

**if 수정된 파일이 생겼을 경우**
1. git add [파일명] : 수정된 파일 저장
2. git checkout -- [파일 명] : 수정된 파일 무시하여 원래 상태 저장

* git log: 내가 올린 기록(커밋 내역)들을 볼 수 있다. 
* git reset —hard [commit 정보(해쉬코드)] : 해당 커밋 이후에 정보들은 모두 삭제된다. 
* git commit —amend: commit 제목 정보를 바꿀 수 있다. 

**git은 동시에 여러 개발자들이 프로젝트에서 각기 다른 기능을 개발할 수 있는 브랜치 기능을 수행한다.
merge를 통해 각기 다른 branch를 통합할 수 있다.** 

* git branch : 현재 사용되고 있는 branch를 보여줌
* git branch [만들려고 하는 브랜치 명] : 새로운 브랜치를 하나 만듦
* git checkout [브랜치 명] : 사용하고자 하는 브랜치를 지명한다. 
* git merge [브랜치 명] : master의 branch와 해당 branch를 통합한다. 
(이 때 사용하고 있는 branch는 항상 master여야 한다. ) 
(통합을 했다면 반드시 썻던 브랜치는 제거해야한다.)
∙git branch –d [브랜치 명]: 해당 브랜치를 제거한다. 

<github 웹 페이지에서 내 저장소로 바꿀 때 사용>
- git checkout master
- 중요 : git fetch origin
- 중요 : git reset —hard origin/master
- git checkout -b newbranch
