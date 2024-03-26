# 3/19(화) 개발 입문 스터디 1주차

#### 학습 목표 : Git 과 GitHub 의 큰 흐름을 파악한다.

**Git ?**  
: 버전 관리 및 협업을 위해 사용하는 VCS(Version Control System)이다.  
: 무엇을 누가 언제 어떻게 수정하였는가 ?

**[파일의 생명주기]**

1. Untracked  
   : Git 으로 추적되지 않는 상태
2. Tracked - Unmodified  
   : 변경 사항이 없는 상태
3. Tracked - Moditied  
   : 변경 사항이 있는 상태
4. Tracked - Staged  
   : 변경사항이 commit 될 준비가 된 상태

**[Git의 영역]**

1. Working Directory  
   : 내가 작업하는 공간. 폴더.  
   : 변경사항이 생기면 Modified 상태를 add 하여 staging
2. Staging Area  
   : Repo로 Push 되기 전 commit 되기를 기다리는 공간.  
   : 변경사항을 commit 하여 Local Repo로 이동
3. Repository  
   : push 하면 도착하는 GitHub 상에 기록되는 공간.  
   3-1. Local Repo  
   : commit 하면 도착  
   3-2. Remote Repo  
   : commit 후 push 하면 도착

---

**Git 명령어 모음**

📌 `git init`

: 디렉토리에 Git 저장소를 만든다.

📌 `git remote add origin <repo address>`

: GitHub repo 의 주소와 Git 을 연결한다. (VScode - Git - GitHub 연결완료)

📌 `git add -A`

: **작업 디렉토리 내** 모든 변경 내용을 **스테이징 영역**으로 넘기고 싶을때 사용한다.

📌 `git add .`

: **현재 디렉토리**의 모든 변경 내용을 **스테이징 영역**으로 넘기고 싶을때 사용한다.

    <aside>
    💡 `git add -A`는 작업 디렉토리 상에 어디에 위치하든 항상 동일하게 모든 변경 내용을 스테이징으로 넘깁니다. 반면에 `git add .`는 명령어를 실행한 디렉토리 이하에서 발생한 변경 내용만 포함하며, 해당 디렉토리 기준으로 상위 디렉토리의 변경 내용을 포함하지 않습니다. 만약에 `git add .`를 프로젝트 최상위 디렉토리에서 실행한다면 `git add -A`와 동일한 효과를 낼 것입니다.

    </aside>

📌 `git add <파일/디렉토리 경로>`

: 작업 디렉토리 내 변경 내용의 일부만 **스테이징 영역**에 추가하기 위해 사용한다.

📌 `git add -p`

: 각 변경 사항을 터미널에서 눈으로 하나씩 확인하며 **스테이징**하거나 제외 가능

: 많은 변경 내용을 여러 개의 변경 기록으로 나누어서 남기고 싶을때 유용

📌 `git status`

: `git add` 와 세트같은 명령어

: 작업 디렉토리와 **스테이징 영역**의 상태를 확인하기 위해 사용한다.

: `git status`의 3가지 영역

    <aside>
    💡 Staging Area (스테이징 영역) ?

    **[작업 디렉토리, 워킹 디렉토리]**
    : 아직 commit 할 준비가 안된 변경 내용을 자유롭게 수정 가능한 공간

    **[스테이징 영역]** - 징검다리
    : commit 할 준비가 된 변경 내용이 Git 저장소에 기록되기 전에 대기하는 공간

    `git add` : 작업 디렉토리 → 스테이징 영역 이동
    `git commit` : 스테이징 영역 → git 변경 이력 (작업 디렉토리 상관 x)

    </aside>

📌 `git commit -m "commit massage"`

: 스테이징 영역에서 Git 변경 이력으로 이동. 최종 반영하는 작업

    <aside>
    💡 commit massage 작성?

    commit massage 는 변경사항을 한눈에 알아볼 수 있게 명확한 메세지를 전달해야한다.
    따라서 type : subject 형식으로 작성한다.

    [type]
    feat  새로운 기능 추가  / refactor 기존 코드 개선 / fix  버그 수정
    chore 코드 외 설정 변경 / docs     문서화        / test 테스트 코드 등

    </aside>

📌 `git log`

: commit 이 정상적으로 되었는 지 확인

📌 `git push origin (branch name)`

: Git 변경 이력에서 GitHub repo 의 원하는 브랜치로 이동(push)

📌 `git rm —cached <file>`

: unstage 로 되돌리기

📌 `rm -r .git`

: git 으로 관리 중단

**실습링크**
: <https://github.com/SYAAINN/SYAAINN.git>
