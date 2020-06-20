## git-tutorials

**git**은 개발자들이 서로 협업을 하는데 도와주는 분산형 협업 오픈소스 툴이다.

나는 학부 시절 git사용법에 대해서 1도 몰랐다. 미리 알고 써놓으면 얼마나 좋을까...ㅜㅜ

지금도 후회가 된다. 

그래서 이번을 계기로 git 사용법을 공부해서 업데이트하고자 한다.

이 **git-tutorials**는 **동빈나**님의 *Git으로 시작하는 협업및 오픈소스 프로젝트* 를 바탕으로 작성하였다.

## github 계정 생성하기

1. [github사이트](www.github.com) 에 접속하여 github 계정을 생성한다. 정말 쉬움!

2. repository를 만든다. repository 라는게 저장소임. 옵션은 public으로 해야됨.
3. 그 다음 git을 원격으로 이용할 수 있는 git-scm에서 git 명령어를 다운받는다.

## 명령프로프트에서 git 명령어 실행

1. git --version으로 버전 확인 이거 해도 되고 안해도 됨. 설치 잘됐는지 몰라고 하는 것이다.
2. git 설정을 해주어야 한다.
   1. ```git config --global user.name {USERNAME}```
   2. ```git config --global user.email {USEREMAIL}```

3. ```git clone {GITREPOSITORY_PATH}```를 통해서 로컬 컴퓨터로 가져온다.
4. 간단한 README파일을 만들고 올려보자.
   1. ```git add README.md```
   2. ```git commit -m "Update README.md"```
   3. ```git push```

로컬 환경에서 새롭게 추가하거나 수정한 파일을 git add명령으로 git에 올릴 준비를 하고 git commit 메세지 명령으로 어떠한 부분을 추가하고 수정했는지 알려준다. 마지막으로 github remote repository에 올리기 위해서 로컬 컴퓨터에서 git push 명령을 통해 github remote repository에 올린다.