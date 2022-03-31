# git flow
```
사전준비

-github 에서 create repo (README.md, license check) & copy address

-gitbash 에서 $ cd Documents/Dev -> $ git clone {repo.address : git-flow-practice}

-$ cd git-flow-practice(생성된 repo adress)로 경로 이동
```

#### git flow 참조
[https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html](https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html)

```
$ git flow init ->
$ git branch 확인해보면 develop branch 생성 및 브랜치로 이동된 것을 확인

$ git flow feature start {feature branch name : fizzbuzz} -> 
$ git branch 확인해보면 feature branch 생성(feature/fizzbuzz) 및 브랜치로 이동된 것을 확인

$ touch fizzbuzz.py (fizzbuzz파일 생성)

$ vi fizzbuzz.py (vim 내에서 fizzbuzz 수식 3의배수 조건 입력 후 저장나가기)

$ git add fizzbuzz.py -> $ git commit

커밋1회완료.

다시 $ vi fizzbuzz.py 실행후 5의배수 조건 입력 후 저장나가기

$ git add fizzbuzz.py -> $ git commit

커밋2회완료.

git status 확인
(branch를 병합 or 삭제시엔 항상 commit 되지 않은 불완전한 파일이 없는지 체크 후)

feature branch 작업 완료 -> $ git flow feature finish fizzbuzz -> 
merge commit 저장나가기 -> 
develop branch로 이동, feature branch는 완료되어 삭제

$git branch 확인해보면 develop main만 남아있고 develop에 switch된 것을 확인

$git flow release start v0.0.1 (v0.0.1 버전 소숫점은 major/minor/sub)

$git flow release finish v0.0.1 ->3개의 vi창이 생성
-merge branch vi window for main(저장나가기)
-tag vi window (저장나가기)
-merge branch vi window for develop(저장나가기)

local release complete.

$ git push -u origin develop
(remote로 dev branch push. 처음으로 remote branch로 보내므로 -u 추가)
$ git push origin main

remote release complete.

$ git tag (사용자가 사용하게 되는 버전에 대한 설명(label)
$ git push --tag 
(tag push to remote. tag는 특정한 commit에 종속됨, 주로 main의 commit)

```
