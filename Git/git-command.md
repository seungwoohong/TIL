# Git Command 정리

## git init

 .git file를 생성하여 git 저장소를 기능을 할 수 있도록 해준다.
```
$ git init
```
## git version

현재 설치된 git의 버전을 볼 수 있다.
```
$ git --version
```
## git clone

저장소를 **복제** 하여 가져 올 수 있다.
```
$ git clone [option] [repo] [dir_name]
```

* 특정 브랜치 가져오기

    그냥 clone을 하게 되면 default 로 설정된 브랜치를 가져오게 되는데 **-b**를 쓰면 특정 브랜치를 복제하여 가져 올 수 있다.
    ```
    $ git clone -b <branch> <repo>
    ```

## git config

현재 git 저장소에 대한 환경 설정을 할 수 있다.

* 설정 목록 보기
```
$ git config --global --list
```

* 사용자명 설정 하기
```
$ git config --global user.name <사용자명>
```

* 사용자 이메일 설정하기
```
$ git config --global user.email "이메일주소"
```
> push, pull등 해당 설정 사용자명으로 적용 되니 필수적으로 해야한다.


## git add

modified file이나 new file 을 스테이징한다.
```
$ git add <file_name | --all>  or add .
```
> add . 은 --all과 같다.

* 단위별 commit 하기
```
$ git add -p
```
개발이나 유지 보수를 하다보면 다른 feature 또는 수정 사항을 한 파일이나 혹은 한번에 수정 하게 되어 feature별로 나우어 커밋 하고 싶을때가 있다.
그럴 때 쓰면 아주 유용하다.
**내가 원하는 파일 또는 같은 파일에 원하는 부분만 스테이징 할 수 있다.**

## git commit

스테이징 한 파일을 커밋 할 수 있다.
```
$ git commit [option]
```

* 메세지와 함께 커밋 하기

    **-m** 옵션을 사용하면 메세지를 추가 할 수 있다.
```
$ git commit -m "contents of commit"
```

* 멀티 라인 메세지

커밋을 할때 다양한 수정 사항을 한번에 메세지에 기록 하다보면 내용이 길어지거나 지저분해지는데 멀티 라인 메세지를 주면 좀 더 예쁘게 정리 할 수 있다. 방법은 그냥 커밋내용에 마지막 "를 입력 안하고 enter key를 누르면 new line이 생성된다.
```
$ git commit -m "contents of commit
>
> * contents 1
> * contents 2"
```
> new line을 그만 넣고 싶을때 " 를 입력하고 enter key를 누르면 된다.

* 커밋 전 마지막으로 변경 내용 확인 하기

    **-v**옵션을 사용하면 커밋전 변경 내용을 확인 할 수 있다.
```
$ git commit -v
```
* 잘못 커밋 된 거 수정하여 다시 올리기

    **--amend** 옵션을 사용하면 파일을 수정하고 직전에 한 커밋에 재커밋 할 수있다.
```
$ git commit --amend
```
>  ***주의 할점*** : 커밋 번호가 바껴서 push 할때 -f 옵션으로 강제 push를 해야하며 협업 하는 사람과 커밋 순서가 꼬일 우려가 있기때문에 조심하여 사용하기 바란다.

## git status

커밋되지 않은 변경사항을 조회한다. 스테이징 된 것과 언스테이징 된것, modified file과 new file을 구분 하여 보여준다.
```
$ git status
```

## git diff

head의 커밋 내용과 working 에 수정된 내용의 차이점을 보여준다.
```
$ git diff
```

* commit 끼리 차이점 보기
```
$ git diff commit-A commit-B
$ git diff HEAD^ HEAD
```
> ***주의*** : A를 기준으로 B의 변경사항을 보여준다.


* 변경 사항 통계 보기

    **--stat** 옵션을 사용하면 변경 사항에 대한 통계를 보여준다.
    변경 된 라인 수, 파일 수
```
$ git diff --stat
```

## git mv

기존에 존재하는 파일을 지정된 이름의 새파일로 이동합니다. 변경이력은 그대로 유지 된다.
```
$ git mv <file_name> <new_file_name>
```

## git branch

브랜치의 리스트를 조회 한다.
```
git branch
```

* 원격저장소 브랜치 확인 하기

    **-r**을 사용 하면 원격저장소의 브랜치를 확인할 수 있다.
```
$ git branch -r
```
* 특정 브랜치를 기반으로 새로운 브랜치 만들기
```
$ git branch <standard_branch> <new_branch>
```
* 그냥 새로운 브랜치 만들기
```
$ git branch <new_branch>
```
> 체크아웃 하지 않는다

* 브랜치 삭제
**-d** 옵션을 사용하면 브랜치를 삭제 할 수 있다.
```
$ git branch -d <branch_name>
```

* 브랜치 정보보기
**-vv** 옵션을 사용하면 최신 커밋 내용과 리모트 정보를 보여준다.
```
$ git branch -vv
```
> -v 옵션은 최신 커밋 내용만 보여줌

## git remote

리모트 리스트를 조회 한다.

```
$ git remote
```

* remote 연결 된 저장소 확인

    **-v** 옵션을 사용하여 리모트 정보 조회가 가능하다.
```
$ git remote -v or -vv
```

* 원격저장소 정보 보기
**show**를 이용하면 원격 저장소의 정보가 보여짐
```
$ git remote show <remote_name>
```

* 리모트 삭제
    **rm** 을 이용하면 리모트를 삭제 할 수 있다.

```
$ git remote rm <remote_name>
```

## git tag

태그 조회
```
$ git tag
```

* 원하는 조건으로 태그 검색
    **-l** 옵션을 이용하면 원하는 조건으로 태그를 검색 할 수 있다.

```
$ git tag -l v1.1.*

v1.1.0
v1.1.1
```

* 태그 이름 붙이기
```
$ git tag <tag_name>
```

* 태그에 정보와 함께 저장하기

    **-a**을 이용하면 태그에 메시지, 만든 사람, 이메일, 날짜가 저장된다.
```
$ git tag -a <tag_name> -m "contents of tag"
```

* 태그 정보 확인
    **show**를 이용하면 정보 확인이 된다.

```
$ git show <tag_name>
```

* 태그 push 하기

태그는 그냥 push 가 안되기 때문에 리모트와 함께 태그명을 적어 줘야 한다.
```
$ git push origin <tag_name>
$ git push origin --tags
```
> 모든 태그를 올릴 때는 --tags를 사용하면 된다.

* 태그 삭제
```
$ git tag -d <tag_name>
```
> 원격 저장소에 이미 올라간 태그를 삭제 하려면 로컬에서 삭제 후아래와 같이 push 해줘야 한다.

```
$ git push <remote_name> :<tag_name>
```

## git log
커밋의 히스토리를 보여준다.
```
$ git log
```

* 헤드 변경 이력과 함께보기

    **-g** 옵션을 이용하면 (reflog) 헤드의 변경이력을 커밋 히스토리와 함께 보여준다.
```
$ git log -g
```

* 특정 기간의 커밋 히스토만 보기
```
$ git log commit-A..commit-B
```
위와 같이 .. 마침표 두개와 사용하면 commit-A 부터 commit-B까지의 이력을 보여준다.

```
$ git log HEAD~5
```
위와 같이 사용하면 최신 커밋 5개만 보여준다.

```
$ git log HEAD^^^
```
위와 같이 사용하면 ^의 갯수인 최신 커밋 3개만 보여준다 HEAD~3과 동일

## git blame
커밋 내용, 커밋명, 수정 시간, 커밋한 사람등의 정보를 보여준다.
```
$ git blame <file_name>
```

## git revert
기존 커밋에서 변경한 내용을 취소해서 새로운 커밋을 생성한다.
```
$ git revert <commit_name>
```

* 여러번 revert 하기
**-n** 옵션을 사용 하면 여러번 revert 후 커밋 할 수 있다.
```
git revert -n <commit_name>
```

## git reset

스테이징 된 파일을 되돌리거나 헤드의 위치를 이전 커밋으로 옮긴다.

* 스테이징 된 파일 언스테이징 하기
```
$ git reset <dir_name | file_name>
```

* 이전 커밋으로 되돌리기
```
$ git reset --hard HEAD~3
```
> --hard옵션은 수정된 파일까지 지정 커밋으로 되돌린다. --soft는 수정된 파일은 남긴다. HEAD는 ***^나 커밋 번호로도 가능***

* 원격저장소의 브랜치 내용 가져오기
```
$ git reset --hard <remote_name>/<branch_name>
```

## git checkout
브랜치를 이동하거나 수정 된 파일 내용을 복구 시킨다.

```
$ git checkout <branch_name>
```

* 수정 된 파일 원상복구
```
$ git checkout <file_name>
```

* 브랜치를 생성 후 이동
```
$ git checkout -b <new_branch_name>
```

* 원격 브랜치 정보를 가져와서 브랜치 생성 후 이동
```
$ git checkout -b <new_branch_name> <remote_name>/<원격저장소의 브랜치 이름>
```

## git fetch

원격저장소를 갱신합니다.
```
$ git fetch <remote_name> | --all
```
> --all은 모든 리모트를 갱신

## git push
커밋된 내용을 원격저장소에 푸싱한다.
```
git push <remote_name>
```
> 리모트 이름을 안적어주면 origin으로 푸싱된다.

* 강제 push
    **-f** 옵션을 사용하면 강제로 푸싱 할 수 있다.
```
$ git push -f
```
> ex) commit --amend를 사용 할 경우와 같이 커밋 번호가 기존과 달라지면 원격 저장소에서 이상함을 느껴 push가 안되는 경우가 있다.
이럴 때만 강제 푸싱한다. 잘못 쓰면 되돌릴 수 없으니 항상 조심한다.

## git pull

원격 저장소에서 변경사항을 가져와 합친다.
git fetch 와 함께 일어난다.
```
git pull <remote_name> <branch_name>
```
> push와 마찬가지로 아무것도 적지 않음 origin이 설정 된다.

## git merge
두 개의 브랜치를 병합한다.
```
git merge <banch-A>
```
현재 브랜치에 branch-A를 병합한다.

* 병합하는 브랜치의 모든 커밋을 하나의 커밋으로 만들기
    **--squash** 옵션을 사용하면 해당 브랜치의 커밋을 모아 하나로 만든다.
```
$ git merge --squash <branch_name>
```
> merge는 merge를 할 때마다 merge commit이 생성되어 히스토리를 정확 하기에 좋지만 히스토리가 지저분 해질 수 있다.

## git rebase
merge와 같이 병합 방법 중 하나이다.
```
git rebase <branch_name>
```

* 대화형 모드로 커밋 순서 변경, 커밋 합치기

**-i**옵션을 사용하면 rebase 할 경우 대화형 모드가 실행된다.
```
$ git rebase -i
```
> merge 와 rebase의 차이는 별도로 자세히 알아보겠습니다.

## git reflog

head의 변경이력을 보여준다. head의 모든 활동을 다 보여준다.
```
$ git reflog
```

## git stash
수정된 파일을 임시 저장 할 수있다.
```
$ git stash
```
> 그냥 stash 하면 수정된 파일들이 최신 커밋 메세지 내용으로 임시 저장된다.

* stash에 메세지 넣어서 저장하기
```
$ git stash save "stash contents"
```

* stash 리스트 보기
```
$ git stash list
```

* stash 가져오기
```
$ git stash pop
```
> stack 구조라고 보면 된다. 최신꺼 부터 차례대로 가져온다.

* stash 모두 비우기
```
$ git stash clear
```

* 특정 stash 내용 가져오기

    **apply**를 사용하여 특정 내용을 가져 올 수 있다.
```
$ git stash apply stash@{0}
```

* 특정 stash 내용 제거

    **drop**을 사용하여 특정 내용을 삭제 할 수 있다.
```
$ git stash drop stash@{2}
```

## git gc

저장소의 로그를 최적화합니다. 로그가 변경 되지 않고 저장하는 방식만 최적화 된다.
```
$ git gc
```
