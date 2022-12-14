## Git 명령어 정리

1. add
- 작업 디렉토리(working directory) 상의 변경 내용을 스테이징 영역(staging area)에 추가하기 위해 사용하는 명령어 이다.

2. status
- 작업 디렉토리(working directory)와 스테이징 영역(staging area)의 상태를 확인하기 위해 사용하는 명령어 이다.

3. commit
- 스테이징 영역의 파일을 커밋하기 위해서 사용하는 명령어 이다.

4. log
- 현재 브랜치의 커밋 기록을 보고자 하는 경우 사용하는 명령어 이다.
- --oneline : 커밋을 한 줄로 요약해서 보여준다.
- --graph : 커밋 옆에 브랜치의 흐름을 그래프로 보여준다.
- --all : HEAD와 관계없이 모든 브랜치들을 보여준다.

5. show
- 현재 브랜치의 가장 최근 커밋 정보를 확인하는 명령어 이다.
- 커밋해시값을 입력하여 특정 커밋의 정보를 확인할 수 있다.

6. remote
- 다른 저장소에 원격 연결을 나열하는 명령어 이다.
- -V 옵션을 사용하면 연결의 URL이 표시된다.
- add [리모트명] [URL]으로 새 연결을 만들 수 있다.
- rm [리모트명]으로 연결을 제거 할 수 있다.
- rename을 사용하여 이름을 변경 할 수 있다.

7. clone
- 원격 저장소에 있는 레포지토리를 로컬 저장소에 복제 할때 사용하는 명령어 이다.
- git clone [원격저장소 주소] 뒤에 디렉토리명을 지정하여 작성 할 수 있다.

8. push
- 로컬 브랜치를 원격 저장소로 푸시할 때 사용하는 명령어 이다.
- force옵션을 사용하여 강제로 푸시할 수 있다.
- git push -u [리모트명] [브랜치명] : 브랜치를 원격 저장소에 연결해 준다.

9. pull
- 원격 저장소의 정보를 가져오면서 자동으로 로컬 브랜치에 병합까지 수행하기 위해 사용하는 명령어 이다.

10. fetch
- 원격 저장소의 커밋들을로컬 저장소로 가져오기 위해 사용하는 명령어 이다.
- fetch후에는 직접 병합을 하여야 한다.

11. merge
- 다른 브랜치를 현재 브랜치에 병합하기 위해 사용하는 명령어 이다.
- 병합 방식에는 fast forward merge, 3-way merge 2가지의 방식이 존재한다.
- 병합 과정에서 충돌 발생시에는 직접 수정을 해야한다.

12. branch
- 가상의 작업 폴더를 의미한다.
- git branch [브랜치명][생성할 브랜치가 가리킬 commit] : commit을 기준으로 branch를 생성한다.
- -d 옵션을 이용하여 병합이 된 브랜치를 삭제 가능하며 -D를 이용시에는 병합 여부 상관 없이 강제로 삭제 가능하다.

13. checkout
- git branch 명령에 의해 생성 된 branch를 이동하기 위해 사용하는 명령어 이다.
- git checkout -b [브랜치명] : 브랜치를 생성하며 이동할 수 있다.
- git checkout - : 이전에 위치했던 브랜치로 이동한다.

14. switch
- checkout과 같이 이동하기 위해 사용하는 명령어 이다.
- git switch -c [브랜치명] : 브랜치를 생성하며 이동할 수 있다.

15. fast forward merge
- merge의 가장 기본적인 방법이다.
- 병합하려는 branch들 사이에 분기가 존재하지 않는 경우 사용된다.
- 순차적 커밋에 맞추어 병합을 처리한다.

16. 3-way merge
- base가 되는 하나의 커밋을 기준으로 발생한 두개의 브랜치를 병합할때 사용된다.
- 충돌이 발생할 경우 수동으로 수정을 하여야한다.
- 3-way merge를 사용할 경우 병합한 새로운 커밋이 발생한다.

17. rebase
- 두 개의 공통 base를 가진 branch에서 한 branch의 base를 다른 branch의 최신 커밋으로 branch의 base를 옮기는 작업이다.
- 커밋 이력을 남기지 않는다.

18. reset
- 과거 커밋 지점으로 이동하고, 이동된 이후의 커밋을 삭제하는 명령어 이다.
- --hard : 해당 커밋ID의 상태로 이동하고, 워킹 디렉토리와 인덱스 영역을 모두 초기화한다.
- --mixed : 해당 커밋ID의 상태로 이동하고, 인덱스 영역은 초기화하고 워킹 디렉토리는 변경하지 않는다.(reset의 기본값)
- --soft : 해당 커밋ID의 상태로 이동하고, 인덱스 영역과 워킹 디렉토리 모두 변경되지 않고, 커밋된 파일들을 스테이징 영역으로 돌린다.

19. revert
- 기존 커밋을 남겨 두고 취소에 대한 새로운 커밋을 생성한다.
- 한 번에 커밋 하나만 취소할 수 있다.




