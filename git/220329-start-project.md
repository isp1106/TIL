## git & github

### top -> bottom
```
github -> repo create
git clone
git push
```

### bottom -> top
```
create repo at local (gitbash)
$ mkdir {repo name}
$ git init {create repo}
$ git remote
$ git remote add origin{alias} {repo address}

//etc work (vi REMOTE.md wq .....)

git add {filename}
git commit
git branch -M main (change git name master to main)
git push -u mask main (-u : upstream set {make a same state})
```

### commit convention

```
*A blob unit is created as a unit of operation.

Write about 50 characters
Put a space between the title and the content.

commit prefix convention

feat (features:기능개발)
docs (documentations:문서형식)
conf (configurations:환경설정)
test (test:테스트)
fix (bug-fix:버그수정)
refactor (refactoring:코드개선)
ci (Continuous Intergration :코드자동화)
build (부산물)
perf (퍼포먼스)
```
