**git log**
: commit 기록을 최신 순으로 확인한다.
: --oneline 옵션을 사용하면 각 커밋을 한 줄에 요약해준다.

**HEAD**
: 현재 작업 중인 위치를 가리킨다.
: 현재 작업중인 브랜치의 가장 최근 commit
: 다음 commit의 base가 되는 commit
: 새로운 commit이 생기면 HEAD도 변경된다.

**git status**
: 3개의 상태에 따라 파일을 분류히여 확인한다.
: State1. Changes to be commited
add 명령어를 통해 Staging Area에 올라간 상태로 commit 되기 전 바로 전 상태이다.
: State2. Changes not staged for commit
modified 상태로 파일이 수정된건 확인됐지만 add 명령어를 통해 Staging Area로 올라가기 전 상태이다.
: State3. Untracked files
수정 여부를 추적할 수 없는 상태이다.

**git commit --amend**
: 마지막 commit 내용에 변경이 있을때 사용한다.
: 완전히 새로운 commit으로 대체 (commit id가 바뀐다.)
: vim(prompt 같은거)으로 진입하여 commit message를 수정한다.
: '-m' option으로 vim 진입 없이 수정도 가능하다.
: '--no-edit' option으로 commit message 수정 없이 commit을 수정한다.
++ vim command 추가 학습

**git reset**
: commit을 제거하는데 사용된다.
: git reset '--option' "<commit id>"
: option1. soft
commit만 취소하고 변경사항을 Staging Area로 돌려놓는다.
: option2. mixed (default)
commit 단계와 add 단계를 취소하고 Working Directory로 돌아간다.
: option3. hard
commit, add, modified 단계 전부 취소하고 변경사항을 모두 제거한다.

**git revert**
: commit을 제거하지 않고 되돌리는 방법이다.
완전히 새로운 commit 생성
: git revert --no-edit "<comment id>" 편집기 진입 없이 바로
: git revert --no-commit 직접 commit 하지않고, revert 내용을 Staging Area에 올린다.

git reset은 commit을 삭제하므로 위험하다.
commit을 공유하는 다른 브랜치에도 영향을 줄 수 있다.
commit을 삭제하기보다 생성하여 되돌리는 revert가 안전하다.
