# python_basic_class
## 파이썬 기초 문법 익히기
<br>

### private 저장소 복사

    $ git clone https://Haawron:[내액세스토큰]@github.com/Haawron/python_basic_class.git
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
<br>

#### 초기 설정

    $ git config --global user.name "Hyeogeon Lee"
    $ git config --global user.email "gunsbrother@naver.com"

#### configuration 확인

    $ git config --list
    $ git config user.name

#### 파일 트랙킹

    $ git add [파일이름]
    $ git add .  # 전체 파일 추적

#### Delta 확인

    $ git diff  # 현재 Unstaged 된 수정사항
    $ git diff --staged  # 현재 staged 된 수정사항
    $ git diff HEAD  # 현재 staged 된 것과 아닌 것 모두 확인
    $ git diff HEAD HEAD^  # 마지막 커밋과 이전 커밋 비교

    $ git diff <branch명> <다른 branch명>  # branch간 비교
    $ git diff <branch명> origin/<branch명>  # 리모트 브랜치와 비교
    $ git diff <commit hash> <commit hash>  # 커밋간 비교

    $ git diff <현재 브랜치> <checkout remote branch>  # 현재 브랜치와 pull request 비교
    $ git diff <commit hash> <checkout remote branch>  # 커밋과 pull request 비교

#### 현재 상태 확인 (Untracked, Modified, Unmodified, Staged 조회)

    $ git status
    $ git status -s  # 현 상태 짤막하게 확인

#### 커밋

    $ git commit -m "할 말"
<br><br>


### 간단한 UNIX 명령어

#### 파일 추가

    $ echo "할 말" > [파일 이름]
원래 echo하면 파일에 할 말을 넣는 건데 파일 이름이 없으면 만들고 넣음.

#### 파일 확인

    $ cat [파일 이름]  # 파일을 읽어서 터미널에 표시
    $ cat [파일 1] [파일 2]  # 파일 두 개를 이어 붙여서 터미널에 표시
    $ cat [파일 1] [파일 2] > [출력파일]  # 파일 두 개를 이어 붙여서 출력파일에 표시
    $ cat [파일 1] > [파일 2]  # 파일 1의 내용을 파일 2에 복사
    $ cat [파일 1] >> [파일 2]  # 파일 1의 내용을 파일 2에 갖다 붙임
    $ cat >[새파일]  # 내용을 입력하며 새 파일 생성, Ctrl + D로 종료

#### 디렉토리 만들기

    $ mkdir [폴더 이름]  # 폴더 생성
    $ mkdir [폴더 1] [폴더 2]  # 폴더 여러 개 생성
    $ mkdir directory\ has\ space; mkdir "directory has space"  # 이름에 공백이 있는 디렉토리 생성
    $ mkdir [폴더]{01, 02, 03 ,04}  # 폴더01, 폴더02, 폴더 03, 폴더 04 생성

#### 디렉토리 삭제

    $ rm -r [폴더 이름]

<br><br>


### .gitignore
[깃설명서]

#### 확장자가 .a인 파일 무시
    *.a
#### 윗 라인에서 확장자가 .a인 파일은 무시하게 했지만 lib.a는 무시하지 않음
    !lib.a
#### 현재 디렉토리에 있는 TODO파일은 무시하고 subdir/TODO처럼 하위디렉토리에 있는 파일은 무시하지 않음
    /TODO
#### build/ 디렉토리에 있는 모든 파일은 무시
    build/
#### doc/notes.txt 파일은 무시하고 doc/server/arch.txt 파일은 무시하지 않음
    doc/*.txt
#### doc 디렉토리 아래의 모든 .pdf 파일을 무시
    doc/**/*.pdf


[깃설명서]: https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EC%88%98%EC%A0%95%ED%95%98%EA%B3%A0-%EC%A0%80%EC%9E%A5%EC%86%8C%EC%97%90-%EC%A0%80%EC%9E%A5%ED%95%98%EA%B8%B0
