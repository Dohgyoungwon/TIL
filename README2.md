# 7월 11일 교육
## Markdown(개발자의 언어)

1. Markdowm 특징
- 코드를 서로 주고 받기 좋음 
- 개발자의 언어라 빨리 서식을 맞춰서 쓸 수 있음
- 코드를 넣기 좋다
- 문법이 아주 쉽다

2. Code block & Inline code block
- code block
    - 개발에서 마크다운을 사용하는 가장 큰 이유
    - code block 예시)
    ```python
    print("Hello")
    print("World")
    ```
- Inline code block 
    - Inline code block 예시) 파이썬은 `print` 함수를 사용해 텍스트를 출력한다

3. 링크 & 이미지
- 링크 
- 링크 예시)
    
    [구글](http://www.google.com)

    [네이버](http://www.naver.com)

- 이미지 
- 이미지 예시)
    
    ![asd](https://picsum.photos/200/300)

4. 텍스트 관련 문법
- **굵게**
- *기울임*
- ~~취소선~~
- 수평선은 하이푼 3개 

## CLI(Command Line Interface)

1. CLI란
- 명령어를 통해 컴퓨터와 사용자가 상호 작용하는 방식 
- git bash, cmd 등

2. 기초 문법 실습 
- '.'의 역할
    - '.' : 현재 디렉토리
    - '..' : 현재의 상위 디렉토리

- touch : 파일생성 
- mkdir : 새 디렉토리 생성
- ls : 현재 작업중인 디렉토리 내부의 폴더/파일 목록 출력
    - cf) ls -a : 숨긴 파일까지 확인 가능 
- cd : 이동
- start : 폴더/파일 열기
- rm : 파일 삭제

3. 절대경로, 상대경로
- 절대경로 : Root 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것.  
    - pwd 명령어 사용
- 상대경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것. 

## Git

**분산 버전 관리 시스템**

1. 버전 관리 

- 변화를 기록하고 추적하는 것

2. 분산

- 중앙 vs 분산 

    - 중앙 집중식 : 버전은 중앙 서버에 저장되고 중앙 서버에서 파일을 가져와 다시 중앙에 업로드

    - 분산식 :  버전을 여러 개의 복제된 저장소에 저장 및 관리

- 분산 구조의 장점

    - 중앙 서버 의존 x , 동시에 다양한 작업o
    - 개발자들 간의 작업 충돌 낮음
    - 백업 복구 용이
    - 인터넷 연결되지 않은 환경 작업 o

3. **git의 영역**

- git의 3가지 영역

    - Working Directory(워킹 디렉토리, 작업 디렉토리)
    - Staging Area(스테이징 에어리어)
    - Repository(저장소, 레포지토리)

- **Working Directory**  : 실제 작업하는 파일들이 위치하는 영역

- **Staging Area** : 변경된 파일 중, 다음 버전에 포함 시킬 파일들을 선택적으로 추가하거나 제외할 수 있는 중간 준비 영역 

- **Repository** : 버전 이력과 파일들이 영구적으로 저장되는 영역 모든 버전과 변경 이력이 기록됨

4. Git 추가 개념

**Commit “버전”**

- 변경된 파일들을 저장하는 행위이며, 마치 사진을 찍듯이 ‘snapshot’이라고도 함

**git init**

- 로컬 저장소 설정(초기화)
    - git의 버전 관리를 시작할 디렉토리에서 진행

**git add**

- 변경사항이 있는 파일을 staging area에 추가
- 예시)
    - git add a.txt
    - git add loyer2_1
    - git add a.txt, loyer2_1
    - git add *.txt(확장명이 .txt인 애들은 전부 staging area에 추가)
    - git add .(전부 다 추가)

**git commit** 

- staging area에 있는 파일들을 저장소에 기록
    
    해당시점의 버전을 생성하고 변경이력을 남기는 것 
    
- 예시)
    - git commit -m “login 기능 추가”

**git status** 

- git 상태 명령어

**git rm --cached**

- git add한 파일을 내릴 경우

**git commit -m**

- Staging Area에서 Repository로 버전을 만들 때
- commit을 작성할 때 “메일주소”, “유저네임”이 필요함
    - git config --global user.email "[won03289@gmail.com](mailto:won03289@gmail.com)"
    - git config --global user.name "[Dohgyunogwon](mailto:won03289@gmail.com)"

**git log** 

- commit history 보기
- 쌓인 commit을 확인 할 경우
- git log —oneline : 쌓인 commit의 한 줄만 확인(단독 작업할 때 유리)

git은 로컬 저장소 내 모든 파일의 ‘변경사항’을 감시하고 있다 

**rm -r .git/**

- .git 폴더 지우기

**참고**

TIL 폴더 구조는 어떻게 만들어야 하나요 ? 

- 정답은 없음
- 여러 개발자들의  GitHub를 당겨오세요

**Commit 수정하기**

- 바로 직전 생성한 Commit 수정하기
    - git commit —amend
        
        git-amend-practice 폴더 생성 
        
        생성한 폴더로 이동 
        
        VSCCode 실행
        
        Git 저장소 생성
        

**git commit --amend**

- 버전관리 측면에서 봤을 때
    - 앗, 빠진 파일 넣었음”, “이전 commit에서 오타 살짝 고침” 과 같은 commit은 유효한 버전이라고 보기 어려움
    - 즉, 불필요한 commit을 생성하지 않고, 직전 commit을 수정할 수 있기 때문에 git에서 꼭 필요한 기능 중에 하나라고 볼 수 있음

- 직전에 적은 commit 메세지 수정
    - 수정모드 : i
    - esc 누르고, 콜론을 누르고, wq

- 실수로 b-function.txt를 빼고 commit 해버린 상황이라 가정 (commit 메세지는 ㄱㅊ, 파일을 빼먹은 상황)
    - b-function.txt만 add만 하고 위와 동일하게 진행


