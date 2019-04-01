# git 기본 명령어 정리

`git을 사용하기 위한 5가지 기본 명령어와 각 명령의 옵션에 대해 정리하는 문서입니다.`

| 명령어       | 작업자 |
|--------------|--------|
| git add      | 미정   |
| git commit   | 지원   |
| git branch   | 다연   |
| git checkout | 진우   |
| git merge    | 민석   |


## git add
`git add` 파일의 변화를 `Staging Area(Index)`에 올릴 때 사용하는 기본 명령어  
> (파일의 변화: 수정, 추가, 삭제)

```
## add 관련 명령어
	
// 확장자가 .md 인 모든 파일 add
git add *.md
	
// 수정되거나 새롭게 추가된 여러개 파일 한번에 add(삭제한 파일은 add 하지 않음)
git add .
	
// 수정되거나 삭제된 여러 파일 한번에 add(새로 추가한 파일은 add 하지 않음)
git add -u
	
// 수정되거나 추가/삭제된 여러개 파일 한번에 add
git add -A
	
// 파일의 변화 내역을 확인 하면서 파일보다 더 작은 hunk 단위로 add
git add -p
	
// add한 파일 되돌리기(unstaging)
git checkout -- foo1
```

## git checkout

과거 특정 commit/branch 지점으로 옮기기위해 사용하는 기본 명령어  

```
## checkout 관련 명령어

// 특정 커밋 상태로 변경
git checkout <commitId>

// 사용할 브랜치 변경
git checkout <branchName>

// 브랜치가 없으면 생성후 변경
git checkout -b <branchName>

// 특정 지점에서 브랜치를 생성후 변경
git checkout -B <branchName> <startPoint>
```

## git commit 

Staging Area에 올라간 파일 및 폴더의 추가/변경 사항을 로컬 저장소에 기록하는 기본 명령어 

```
## commit 관련 명령어

//Staging Area에 올라와 있는 모든 파일에 대해 commit(커밋 메세지 길게 남기기 가능)
git commit

// -m 옵션으로 간단한 메세지를 작성하여 commit
git commit -m "<commit message>"

// 수정된 파일 한번에 add 해서 commit
git commit -a -m "commit message"
```



### reference

* [git scm : 2.2 Git의 기초 - 수정하고 저장소에 저장하기](https://git-scm.com/book/ko/v2/Git의-기초-수정하고-저장소에-저장하기)
* [Outsider's Dev Story : git add -p 와 git commit -v 의 사용](https://blog.outsider.ne.kr/1247)
* [민소네 : [Git]명령어 정리](http://minsone.github.io/git/git-command-list)
* [freeCodeCamp : Git Checkout](https://guide.freecodecamp.org/git/git-checkout/)
