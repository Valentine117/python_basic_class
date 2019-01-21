# python_basic_class
## 파이썬 기초 문법 익히기  
<br>

### private 저장소 복사  

    $ git clone https://Haawron:\[내액세스토큰\]@github.com/Haawron/python_basic_class.git  
<br>

### 액세스 토큰 만들기
Settings >> Developer Settings >> Personal access tokens 가서  
private full control 토큰 `regenerate` 하거나  
`repo`에 체크하고 `generate new token` 하면 됨.
<br><br>

### 사용자 (collaborators) 추가
`repo`의 Settings >> Collaborators 가보면 세 명까지 추가할 수 있음.
<br><br>

### 맨날 까먹는 깃 명령어

<span style="color:red">로컬 폴더에 반드시 .git 폴더가 있어야 함.</span>

초기 설정  

    $ git config --global user.name "Hyeogeon Lee"
    $ git config --global user.email "gunsbrother@naver.com"

configuration 확인
    
    $ git config --list
    $ git config user.name

파일 트랙킹

    $ git add [파일이름]
    $ git add .  # 전체 파일 추적

현재 상태 확인 (Untracked, Modified, Unmodified, Staged 조회)

    $ git status
    $ git status -s  # 현 상태 짤막하게 확인

커밋
    
    $ git commit -m "할 말"

파일 추가

    $ echo "할 말" > [파일 이름]
원래 echo하면 파일에 할 말을 넣는 건데 파일 이름이 없으면 만들고 넣음.

파일 확인

    $ cat [파일 이름]  # 파일을 읽어서 터미널에 표시
    $ cat [파일 1] [파일 2]  # 파일 두 개를 이어 붙여서 터미널에 표시
    $ cat [파일 1] [파일 2] > [출력파일]  # 파일 두 개를 이어 붙여서 출력파일에 표시
    $ cat [파일 1] > [파일 2]  # 파일 1의 내용을 파일 2에 복사
    $ cat [파일 1] >> [파일 2]  # 파일 1의 내용을 파일 2에 갖다 붙임
    $ cat >[새파일]  # 내용을 입력하며 새 파일 생성, Ctrl + D로 종료

<br><br>


### .gitignore
[깃설명서]
#### 확장자가 .a인 파일 무시
`*.a`
#### 윗 라인에서 확장자가 .a인 파일은 무시하게 했지만 lib.a는 무시하지 않음
`!lib.a`
#### 현재 디렉토리에 있는 TODO파일은 무시하고 subdir/TODO처럼 하위디렉토리에 있는 파일은 무시하지 않음
`/TODO`
#### build/ 디렉토리에 있는 모든 파일은 무시
`build/`
#### doc/notes.txt 파일은 무시하고 doc/server/arch.txt 파일은 무시하지 않음
`doc/*.txt`
#### doc 디렉토리 아래의 모든 .pdf 파일을 무시
`doc/**/*.pdf`


[깃설명서]: https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%88%98%EC%A0%95%ED%95%98%EA%B3%A0-%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90-%EC%A0%80%EC%9E%A5%ED%95%98%EA%B8%B0