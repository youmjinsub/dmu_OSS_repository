git 명령어 정리
--------------

* add, commit, log, show

> add - 작업 디렉토리(working directory)에서 변경 내용을 스테이징 영역(staging area)에 추가하는 명령어입니다.
>
> commit - 파일 및 폴더의 추가, 변경 사항을 저장소에 기록하는 명령어입니다.
> 
> log - 커밋 히스토리를 조회하는 명령어입니다.
>
> show - commit 정보를 확인하는 명령어입니다. commit의 해시값, 메시지 등을 확인할 수 있습니다.

<br>

* clone, push, pull, fetch/merge

> clone - 원격저장소에 있는 파일을 로컬 브랜치에 가지고 올때 사용하는 명령어입니다.
>
> push - 로컬 브랜치를 원격 저장소로 보낼 때 사용하는 명령어입니다.
>
> pull - 원격 저장소에서 로컬 브랜치로 가지고 올 때 사용하는 명령어입니다.
>
> fetch/merge - fetch는 원격저장소에 있는 변경사항들을 로컬로 가지고 오기 전 변경내용을 확인할 때 사용하는 명령어입니다.
>
> merge는 다른 브랜치를 현재 checkout된 브랜치에 병합하는 명령어입니다.

<br>

* branch, checkout, switch

> branch - 여러 개발자들이 동시에 다양한 작업을 가능하게 만들어 주는 기능입니다.
>
> checkout - 브랜치를 변경하고 해당 파일을 워킹 디렉토리로 복사하는 기능입니다.
>
> switch - 브랜치를 변경하는 명령어입니다.

<br>

* fast forward merge, 3-way merge, rebase

> fast forward merge - 기본적인 병합으로, 현재 브랜치의 헤드가 대상 브랜치의 헤드까지 옮겨 병합하는 기능입니다.
>
> 3-way merge - 두 브랜치가 base에서 분리된 커밋을 참조할 때, 새로운 커밋이 생성되는 경우입니다.
>
> rebase - 두 개의 공통 base를 가진 브랜치에서 한 브랜치의 base를 다른 브랜치의 최신 커밋으로 base를 옮기는 기능입니다.

<br>

* reset, revert

> reset - 작업 중 파일들이 변경되었을 때 특정 커밋으로 되돌리는 기능입니다.
>
> revert - 하나의 커밋에서의 변경사항을 제거하고 새로운 커밋을 생성하는 명령어입니다. 커밋 사이의 중간 커밋만 제거가 가능합니다.
