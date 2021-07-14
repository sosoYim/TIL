# 210714-git-notion.md

## 주요 개념

### CVS / SVN (전 세대 국내 개발자들이 주로 사용함)

- VCS :Version Control System
- 중앙 서버 집중형

---

### GIT : 버전관리시스템 or 형상관리시스템

- DVCS : Distributed Version Control System
- 로컬 저장소
- branch를 이용해 실험적 개발의 안정성
- 코드 소실의 위험성 제거
- Master (main) brunch : 최초로 생성된 가지

### Github : 협업 프로세스 중 하나

- Collaborate 방식
- Pull Request 방식 (Contribution 방식)

### Git 저장 순서

- Working Tree : 파일을 수정, 삭제, 생성하는 모든 활동 (untracted file)
- 스테이징
- index/stage : 깃에 의해 추적된 파일들 저장 (tracked file)
- 커밋 (= 스냅샷 찍기 : 깃, 이 순간을 기억해 !)
- Local Repository : 로컬 저장소. 스테이징된 파일들을 스냅샷하여 로컬 저장소에 저장한다.
- pull 혹은 push 하다
- Remote Repository : Github와 같은 외부 저장소. 로컬 리퍼지토리에서 보내는 것은 pull, 반대로 받아오는 것을 push라고 한다.

## git

### 깃 명령어

- git status : 현재 git 폴더의 성태정보 (branch, ...)을 보여줌
- git add : working tree의 untracked 파일을 staging 시켜 tracked 상태로 변경
- git rm —cached fileName: 언스테이징시키는 언어
- git commit -m "커밋이름"
- 깃 등록자 이메일, 이름 등록하기. 내 컴퓨터가 아니면 —global은 빼자 (global로 등록된 계정은 windows 자격증명에서 변경 및 삭제할 수 있다.)
  - git config —global user.email "you@example.com"
  - git config —global [user.name](http://user.name) "Your Name"
- git log : 커밋 히스토리 확인
- git log -3 : 최신 커밋 히스토리 3개만 보기
- Q : end 로 나가야 할 때
- git checkout + 헤드 앞 4자리 : 해당 스냅샷으로 돌아가서 둘러보기
- git checkout master (git checkout 브런치 이름) : 해당 브런치의 가장 최신버전으로 간다.
- git reset —hard : 특정 commit 포인트를 현재로 만들어 버린다. 그 상태로 리셋.

### .gitignore(확장자 없이 생성)

- git에 의해 관리되지 않을 (무시될) 파일들의 명단을 만들어 둔 파일
- .gitignore 파일에 들어간 내용은 git status에서 빠진다.
- gitignore에 관한 설정파일 찾을 수 있는 사이트

  [https://www.toptal.com/developers/gitignore](https://www.toptal.com/developers/gitignore)

  예 ) Maven, Java, Java-Web, Eclipse, Git, Windows 를 쳐서 나온 텍스트를 복붙하고 .classpath .project 이 둘을 더 써줬다.

### github에 push, pull 하기

- remote add <원격저장소이름> <url>

  예) remote add test [https://github.com/sosoYim/test01.git](https://github.com/sosoYim/test01.git)

- git add \* 후 git status를 보고 gitignore가 잘 적용되었는지 확인
- git push <원격저장소이름> <브런치이름>

  예) remote push test master
