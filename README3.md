# 7월 12일 교육
## Remote Repository

### 원격 저장소

코드와 버전 관리 이력을 온라인 상의 특정 위치에 저장하여 여러 개발자가 협업하고 코드를 공유할 수 있는  저장 공간

예시) GitLab(SSAFY), GitHub(메이저), Bitbucket(마이너) 

### 로컬 & 원격 저장소

- GitHub Repository —-remote—- Local Repository
- **git remote add origin remote_repo_url : 로컬 저장소에 원격 저장소 추가**
    - origin : 추가하는 원격 저장소 별칭
        - origin은 개발자들이 보편적으로 쓰는 별칭
    - remote_repo_url :
- git remote -v : 로컬이랑 원격을 연결해줌
    - fetch : 가지고 올 때
    - push : 원격으로 밀 때
    - pull or clone : 로컬로 당길 때
- git push origin master : 원격 저장소에  commit 목록을 업로드
- (HEAD → master) : 로컬에서 제일 최신
- (origin/master) : origin에서 제일 최신

**따라서 원격저장소에는 commit이 올라가는 것 commit 이력이 없다면 push 할 수 없다.**

### pull & clone

- git pull origin master
    - 원격 저장소의 변경사항만을 가져옴(업데이트)
- git clone remote_repo_url
    - 원격 저장소 전체를 복제(다운로드)
    - clone으로 받은 프로젝트는 이미 git init이 되어 있음