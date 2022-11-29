# Git
![깃](https://user-images.githubusercontent.com/101856066/204583545-d8827484-98ad-4c45-83d0-d4f368ee817b.jpg)

### Git이란?
- 분산형 버전 관리 시스템의 한 종류이다.
- 버전 관리는 파일들을 복사, 백업, 저장 등을 해서 관리하는 것을 의미한. 이러한 버전 관리는 크게 1) 클라이언트-서버 모델(CVS, SVN 등)과 2) 분산 모델, 두 가지로 나눠서 볼 수 있다. 깃(Git)은 분산 모델에 속한다.
### 장점
- 별도로 주고 받는 작업 없이 같은 파일을 여러 명이 동시에, 병렬 개발이 가능하다.
- 작업한 파일에 대한 변경된 정보를 실시간으로 저장해준다.
- 같은 파일에 대한 각각 다른 버전을 보관할 수 있다.

## 깃 환경설정

### 기본설정

- 사용자 설정  
$ git config --global user.name "User name"  
$ git config --global user.email "email"

- 편집기 설정  
$ git config --global core.editor 'code --wait'

- 축약 별칭 명령어  
$ git config --global alias.<단축_명령어> <실제_명령어>

- CR과 LF문자  
$ git config --global core.autocrlf true #window  
$ git config --global core.autocrlf input #mac  
$ git config --global core.safecrlf false  
- 설정 취소  
$ git config --global --unset <이름>
 
- 설정 보기  
$ git config --global --list

## 기본 용어
### Repository 
- 저장소를 의미한다.
- 저장소는 히스토리, 태그, 소스의 Branch에 따라 버전을 저장한다.
- 저장소를 통해서 작업자가 변경한 모든 히스토리를 확인할 수 있수 있다.
### Working Tree 
- 저장소를 어느 한 시점을 바라보는 작업자의 현재 시점을 의미한다.
### Staging Area 
- 저장소에 커밋하기 전에 커밋을 준비하는 위치이다.
### Commit 
- 현재 변경된 작업 상태를 점검을 마친 뒤 확정하여 저장소에 저장하는 작업을 의미한다.
### Head 
- 현재 작업중인 Branch를 의미한다.
### Branch 
- 분기점을 의미한다. 
- 복사하여 Branch에서 작업을 한 후 완전할 경우 Merge를 한다.
### Merge 
- Branch의 내용을 현재 Branch로 가져와 합치는 작업을 의미한다.

## 주요 명령어
### git init
- 깃 저장소를 초기화한다. 
- 저장소나 디렉토리 안에서 이 명령을 실행하기 전까지는 그냥 일반 폴더이다. 
- 이것을 입력한 후에야 추가적인 깃 명령어들을 줄 수 있다.

### git status
- 저장소 상태를 체크한다.
- 어떤 파일이 저장소 안에 있는지, 커밋이 필요한 변경사항이 있는지, 현재 저장소의 어떤 브랜치에서 작업하고 있는지 등을 볼 수 있다.

### git clone
- 원격 저장소의 저장소를 내 local에서 이용할 수 있게 그대로 복사해 가져온다.

### git add
- 이 명령이 저장소에 새 파일들을 추가하진 않는다. 
- 대신, 깃이 파일들을 지켜보게 한다. 
- 파일을 추가하면, 깃의 저장소 “스냅샷”에 포함된다.

### git commit 
- 깃의 의미있는 수정 작업이 끝났을 때 마침을 알리는 작업이다. 

### git push
- 로컬 컴퓨터에서 작업하고 커밋을 깃허브에서 온라인으로도 볼 수 있기를 원한다면, 이 명령어로 깃허브에 변경사항을 "push"한다.

### git pull 
- 로컬 컴퓨터에서 작업할 때, 저장소의 변경된 내용을 로컬(내 컴퓨터) 저장소에 적용하는 작업이다.

### git branch 
- 여러 협업자와 작업하고 자신만의 변경을 원한다면 이 명령어로 새로운 브랜치를 만들고, 독립적인 공간을 만든다. 

### git checkout
- 독립된 작업 공간인 브랜치를 자유롭게 이동할 수 있다

### git merge
- 브랜치에서 작업을 끝내고, 모든 협업자가 볼 수 있는 master 브랜치로 병합할 수 있다
