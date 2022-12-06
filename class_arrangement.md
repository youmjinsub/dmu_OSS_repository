# OSS 수업 주차별 정리



1주차
======

소프트웨어 설치

    깃(git) - 소스코드 관리를 위한 분산 버전관리시스템
    
    소스트리(source tree) - 소스코드 관리를 위한 GUI 도구
    
    편집기(code editor) - 코드 편집과 소스코드 관리를 위한 도구
    
    ex) pytharm, vscode
    
    깃허브(github) - 깃 기반의 저장소 및 소프트웨어 협업 개발을 위한 웹호스팅서비스
    
README.md - 분산 버전 관리 툴인 깃 저장소 호스팅을 지원하는 웹 서비스
    
토큰 - 비밀번호 인증 대신 사용하는 강화된 인증 방법

리눅스 명령어

    ls(list segments): 현재 위치의 파일 목록 조회
    
    cd(change directory): 디렉터리 이동
    
    mkdir(Make dirctory): 디렉터리 생성
    
    cp(copy): 파일 복사
    
    mv(move): 파일 이동
    
    rm(Remove): 파일 삭제
    
    cat(catenate): 파일의 내용을 화면에 출력, 리다이렉션('>') 기호를 이용하여 새 파일 생성
    
    '>>' 기호 사용 시 기존 파일 내용 뒤에 덧붙여서 저장
    
    
2주차
======

버전 관리 - 시간 흐름에 따라 파일 집합에 대한 변경 사항을 추적, 관리

    버전의 저장과 백업
    여러 사용자에 대한 버전 이력 추적관리
    
버전관리의 커밋 - 저장소의 현 상태를 저장하는 행위

원격 저장소(Remote Repository) - 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소

지역(로컬) 저장소(Local Repository) - 내 pc에 파일이 저장되는 개인 전용 저장소

Push와 Pull 활용
    
    Push: 원격 저장소 올리기
    
    Pull: 원격 저장소에서 지역 저장소로 내리기
    
### 깃이란?


정의 - 컴퓨터 파일의 변경을 추적하는 버전 관리 시스템

#### 기능 

   - 여러 개발자가 함께 작업
    
   - 소스 코드의 변경 사항을 추적하는 데 사용
    
   - 소스 코드 관리에 분산 버전 제어 도구가 사용

   - 여러 개의 평행 분기를 통해 비선형 개발을 지원

#### 깃의 3단계와 3 상태
   
   - 작업 디렉토리(working directory), 작업 공간(work space), 작업 트리(working tree)

   - 스테이징 영역(staging area, stage area, index)
   
   - 깃 저장소(git repository, repository, .git dirctory)

git init - 프로젝트를 git repository로 만들기 위해 사용. git repository로 만들어야 git으로 버전 관리 가능

#### 파일 관리

###### Tracked(관리 대상)와 Untracked(비관리대상)

Tracked 파일

    Unmodified(수정하지 않음)
    
    Modified(수정함)
    
    Staged(커밋으로 저장소에 기록할) 상태 중 하나
    
Untracked 파일

    워킹 디렉토리에 있는 파일 중 스냅샷(저장소)에도 staging area에도 포함되지 않은 상태
    
    처음 저장소를 생성하면 모든 파일
    
    처음 저장소를 clone 하면 모든 파일은 Tracked이면서 Untracked 상태
    
3주차
======

add 취소 - git rm --cached 'name'

- 파일 'name'이 untracked 됨

원격저장소 복제 - git clone '주소'

원격 저장소 별칭 이름 - git remote(기본 이름 origin)

git pull - 현재 origin에서 기본 브랜치로 가져 오기

4주차
=====

Fork - 타인의 저장소를 자신의 깃허브 원격저장소에 복사

fork 한 원격 저장소 싱크 - Sync fork > update branch

### open pull request

fork한 자신의 저장소에서 파일 업로드한 후, Contribute > open pull request > PR 생성

5주차
=====
- 소스트리
    
1. 파일생성
    
2. add
    
3. commit

-------------------------------------------

왼쪽 history를 통해 커밋이력, 스테이지, 작업디렉토리 확인 가능

커밋 이후 편집 후 add만 하는 경우 상단에 커밋되지 않은 변경사항 확인 가능

6주차
======

브랜치(Branch)

    여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어주는 기능
    
    각자 독립적인 작업 영역(저장소) 안에서 마음대로 소스코드를 변경
    
브랜치 생성과 이동 명령

생성

- branch, switch -c, checkout -b

이동

- switch, checkout

항상 유지되는 메인 브랜치들

- main, develop

일정 기간 동안만 유지되는 보조 브랜치들

- feature, release, hotfix

--------------------------

'HEAD' 포인터 - 지금 작업하는 로컬 브랜치를 가리킴

프로젝트의 히스토리를 옮겨다니는 경우 detached HEAD 상태

- 체크아웃으로 과거 이력에 해당하는 커밋으로 이동한 경우

7주차
=====

git diff : 스테이징 파일상태와 작업 공간에서 현재 수정중인 상태 비교

git diff -staged : commit된 파일상태와 add된 파일 상태 비교

commit간 상태 비교 
    
    git diff 커밋해쉬1 커밋해쉬2
    
    git diff HEAD HEAD^

9주차
=====

git stash - 깃에서 임시저장소에 저장

    브랜치 이동 전에 작업 디렉토리 정리에 필요시 사용
    
    stash의 내용을 기존 작업 디렉토리의 내용만 복사하여 활용 가능

git stash pop stash@{n} - 지정된 임시저장소 내용을 가져와 반영하고 삭제

git stash apply stash@{n} - 지정된 임시저장소 내용을 가져와 반영, 작업 영역만 반영, stash 목록은 그대로

git stash apply --index stash@{n} - 지정된 임시저장소 내용을 가져와 반영, 작업 영역과 스테이징 영역도 반영, stash 목록은 그대로

git stash drop stash@{n} - 지정된 임시저장소 내용을 삭제

git stash clear - stash 목록을 모두 제거

10주차
======
