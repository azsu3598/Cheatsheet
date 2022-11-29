## 1. 깃 환경설정

1. 설치
- 
-

2. 기본설정

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
