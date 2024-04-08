git log
: commit 기록을 최신 순으로 확인한다.
: --oneline 옵션을 사용하면 각 커밋을 한 줄에 요약해준다.

HEAD
: 현재 작업 중인 위치를 가리킨다.
: 현재 작업중인 브랜치의 가장 최근 commit
: 다음 commit의 base가 되는 commit
: 새로운 commit이 생기면 HEAD도 변경된다.

git status
: 3개의 상태에 따라 파일을 분류히여 확인한다.
: Changes to be commited
add 명령어를 통해 Staging Area에 올라간 상태로 commit 되기 전 바로 전 상태이다.
: Changes not staged for commit
modified 상태로 파일이 수정된건 확인됐지만 add 명령어를 통해 Staging Area로 올라가기 전 상태이다.
: Untracked files
수정 여부를 추적할 수 없는 상태이다.

commit --amend
:
