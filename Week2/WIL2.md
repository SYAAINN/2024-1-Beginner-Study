# 3/19(화) 개발 입문 스터디 1주차

#### 학습 목표 : issue, pull request, branch, merge에 대해 학습한다.

📌 issue

: Repo에서 작업 계획, 토론 및 추적을 위해 활용

: 템플릿을 만들어두면 편함 (Settings-Features—Issues-Set up Templates)

📌 branch

: 기존 branch 에서 분기되어 생성되는 별도의 작업 공간

: branch 의 이름 또한 commit message 와 같이 의미, 기능들을 바탕으로 작성

📌 pull request (PR)

: 분기된 branch를 다시 병합하기 위한 절차

: 어떤 branch(변경이 생긴 branch) 에서 어떤 branch(변경을 반영하고 싶은 branch)로 pull 할건지 주의

: 새로운 변경을 제안하거나 병합 시 발생하는 충돌을 해결

: merge에 앞서 코드 리뷰

: 보통 pull request를 올리면 다른 이(상사 등)의 승인(approval) 후에 merge 하게 됨

: 추후 프로젝트 시 구현 영상을 함께 첨부하는게 좋음

: issue 처럼 템플릿 있으면 편함

📌 code review

: 개발은 혼자하는 것이 아닌 만큼 PR 이후 code review 는 필수

: comment, approve, request changes 3개 중 선택 가능

: comment → 단순한 리뷰 (칭찬, 피드백 등)

: Approve → 해당 PR을 승인할 때 사용 (merge 승인)

: Request Change → 코드 재작성 요청 (반드시 고칠게 있는 경우)

📌 merge

1. merge commit

   두 브랜치를 공통 부모로 하는 새로운 commit ‘E’를 만듦.

2. squash and merge

   A,B,C 커밋을 ‘squash(으깸.짓누름)’ 해서 하나의 커밋으로 병합

3. rebase and merge

   A,B,C 커밋의 base를 재설정, 모두 새로운 커밋으로 변경

   무수한 충돌이 일어날 수 있으므로 사용에 주의

---

**[추가 내용]**

📌 fork

: 다른 사용자의 Repo를 자신의 계정으로 복사해 독립적으로 수정 및 관리

📌 star

: 관심있는 Repo나 프로젝트를 **북마크**처럼 관리 가능

📌 commit message convention

: [commit type] issue number , content

- **[FEAT]** : 새로운 기능 구현
- **[MOD]** : 코드 수정 및 내부 파일 수정
- **[ADD]** : 부수적인 코드 추가 및 라이브러리 추가, 새로운 파일 생성
- **[CHORE]** : 버전 코드 수정, 패키지 구조 변경, 타입 및 변수명 변경 등의 작은 작업
- **[DEL]** : 쓸모없는 코드나 파일 삭제
- **[UI]** : UI 작업
- **[FIX]** : 버그 및 오류 해결
- **[HOTFIX]** : issue나 QA에서 문의된 급한 버그 및 오류 해결
- **[MERGE]** : 다른 브랜치와의 MERGE
- **[MOVE]** : 프로젝트 내 파일이나 코드의 이동
- **[RENAME]** : 파일 이름 변경
- **[REFACTOR]** : 전면 수정
- **[DOCS]** : README나 WIKI 등의 문서 개정

---

**[실습 링크]** ⬇️

<https://github.com/SYAAINN/2024-1-Beginner-Study/pull/10>
