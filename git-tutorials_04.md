## 깃(Git)의 동작 원리

기본적으로 깃(git)프로젝트에 담겨 있는 데이터들은 파일 시스템 상에서 스냅샷(SnapShot)이라 볼 수 있다. 실제 프로젝트를 커밋(Commit)하여 적용할 때의 순간을 중요시한다는 특징이 있다. 파일 자체를 저장하기 보다는 수정 내역 자체를 저장한다.

## Git 프로젝트의 세 가지 구성요소

Git의 동작 원리를 바르게 이해하기 위해 Git 프로젝트의 세 가지 구성요소에 대해서 이해할 필요가 있다.

- **Working Directory**: 작업할 파일이 있는 디렉토리이다.
- **Staging Area**: 커밋(Commit)을 수행할 파일들이 올라가는 영역이다.
- **Git Directory**: Git 프로젝트의 메타 데이터와 데이터 정보가 저장되는 디렉토리이다.

```.git```이란 디렉토리를 지우면 git이 제대로 작동하지 않는다. (절대 삭제하면 안됨)

깃의 기본적인 동작과정

> **Working Directory**->```git add```->**Staging Area** -> ```git commit```->**Local Repository**->```git push```-> **Remote Repository**
>
> **Remote Repository**->```git fetch```->**Local Repository**->```git merge```->**Working Directory**

```git commit```을 하면 우리 컴퓨터(Local Repository)에 저장된다는 것이다.

다른 사람이 수정한 내역을 받기 위해서 ```git fetch```명령을 사용한다. 이후 ```git merge```를 수행해 **Remote Repository**와 **Local Repository**를 동기화한다.

```git fetch```와 ```git merge```를 하나의 명령어인 ```git pull```을 쓸 수도 있다.

## 저장소(Repository)에 대해

저장소(Repo)는 실제 소스코드가 담겨 있고, 커밋(Commit) 내역 등의 모든 작업 이력이 담겨 있는 공간을 의미한다. 실제 프로젝트의 메타 데이터를 포함해 각 종 데이터가 **.git** 폴더에 담기게 된다. 폴더는 각종 데이터와 해시 값이 담겨 있다.

어떠한 파일을 Commit하게 되면 각 작업들을 분류하기 위해 내부적으로 해당 작업에 대한 해시(Hash)값을 이용한다. 일반적으로 해시 값은 충돌이 발생하지 않기 때문에 정확히 커밋 내역들을 관리할 수 있다.

내부적인 원리는 몰라도 깃의 명령어를 잘 아는 것이 중요하다.!