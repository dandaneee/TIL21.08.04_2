# Git

> - 소스코드를 효과적으로 관리하기 위한**`분산형 버전 관리 시스템`**
> - Git에서는 소스코드가 변경된 이력을 쉽게 확인 할 수 있고, 특정 시점에 저장된 버전과 비교하거나 특정 시점으로 되돌아갈 수 있다.

### Git 특성

>- 버전관리: commit 할때마다 버전이 기록되어 특정 시점의 버전을 수정/불러오기가 가능하다
>- 원격저장소를 통해 타인과 공유 가능하다.



### Git 명령어

> - ls : list 공용명령어 
> - touch (파일명) :(파일명)인 파일 생성
> - pwd(print wording directory) : 현재위치 출력
> - mkdir test (make directory ): 폴더생성
> - cd(change directory): 경로 변경
![image-20210804162145873](C:/Users/Robot/Documents/md_images/image-20210804162145873.png)

> - .. : 상위 디렉토리
> ![image-20210804162232969](C:/Users/Robot/Documents/md_images/image-20210804162232969.png)

> - . : 현재 디렉토리

 ______________________________________________________________________________________________________________________________________________________________________________________________________________

#### Git 외부저장소(remote)에 저장하는 과정

> 1. ==파일 등록, commit ==
>
> git add .
>
> git commit -m '커밋메시지' 개발내용이 뭔지 기록하는것
>
>  
>
> 2. ==상태 보기==
>
> git status
>
> git log
>
>  
>
> 3. ==원격저장소 저장==
>
> git remote add origin <url>
>
> git push origin master



#### Git status시 오류 정리

````bash
$ git status
On branch master
# 트래킹되고 있지 않은 파일들 (Working directory)
Untracked files:
# Staging area에 포함시키기 위해서는 git add를 해.
# Staging area -> 커밋 대상 파일들 모아놓는 공간(커밋이 될 예정인 것들)
  (use "git add <file>..." to include in what will be committed)
        new.txt

# 커밋하기 위해 추가된 것은 없는데,untracked files는 존재한다.
# Working directory -> 파일 있어
# Staging area -> 파일 없어
nothing added to commit but untracked files present (use "git add" to track)
```
````



```bash
$ git status
On branch master
# 커밋될 변경사항들 (staging area)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.txt
```

```bash
$ git status
On branch master
# Staging area (Staged O)
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.txt


# staged X (커밋을 위해)
# Working directory
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   2.txt

# 트래킹 X
# Working directory
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hi.txt


```
