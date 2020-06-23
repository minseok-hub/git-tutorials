## 소스코드 수정하여 Git 저장소에 반영하기!

깃헙의 소스코드를 수정하는 것은 두 가지 사례로 나뉘게 된다.

1. 해당 프로젝트에 소속된 사람이 아닌 경우

   특정 커뮤니티(Community)의 구성원이 아니라서 스스로 커밋을 하거나 저장소에 적용할 권한이 없다면, 소스코드를 수정하는 것에 제약이 있다. 이런 경우 <u>PR(Pull Request)를 작성하여 오픈소스에 기여</u>할 수 있다.

2. 해당 프로젝트에 소속된 사람인 경우

    자신이 해당 프로젝트에 대한 권한을 가지고 있을 경우, 커밋(commit)하고 푸시(push)해서 저장소에 수정 내역을 반영하면 된다.

> git add <FILENAME>
>
> \> staging area로 옮겨감.
>
> git reset <FILENAME>
>
> \> working directory로 돌아감. 즉, add 명령 취소하는 것.
>
> git commit -m "Message"
>
> \> local repository로 옮겨감.
>
> 만약 파일을 수정했는데 다시 원래 대로 돌리고 싶을 경우
>
> git restore <FILENAME> 명령을 통해서 돌릴 수 있다.
>
> 또한 git commit -m "Messageeeee" 와 같이 commit 메세지를 잘못 작성했을 경우 다음 명령으로 바꿀 수 있다.
>
> git commit --amend