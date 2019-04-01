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

## git branch
독립적으로 어떤 작업을 진행하기 위한 개념. 각각의 브랜치는 다른 브랜치의 영향을 받지 않으므로 여러 작업을 동시에 진행할 수 있음.

```
## branch 관련 명령어

// 새 브랜치를 특정 브랜치에서 분기
예)feature 브랜치를 'develop' 브랜치에서 분기(master가 아님)
git checkout -b feature/login develop

// --no-ff 옵션 : 새로운 커밋 객체를 만들어 merge함. 합치려는 브랜치에 존재하는 커밋 이력을 모두 합쳐 하나의 새로운 커밋 객체를 만들어 병합하는 것.
예) 현재 develop 브랜치에 있음. 'feature' 브랜치에 존재하는 커밋 이력을 모두 합쳐 하나의 커밋 객체로 만든 후 'develop' 브랜치로 병합(merge)함.
git merge --no-ff feature/login  

// 브랜치 삭제
git branch -d feature/login
```
![--no-ff 참고 사진](https://gmlwjd9405.github.io/images/types-of-git-branch/feature-branch-merge.png)


### reference

* [git scm : 2.2 Git의 기초 - 수정하고 저장소에 저장하기](https://git-scm.com/book/ko/v2/Git의-기초-수정하고-저장소에-저장하기)
* [Outsider's Dev Story : git add -p 와 git commit -v 의 사용](https://blog.outsider.ne.kr/1247)
* [민소네 : [Git]명령어 정리](http://minsone.github.io/git/git-command-list)

* [freeCodeCamp : Git Checkout](https://guide.freecodecamp.org/git/git-checkout/)
* [git branch 종류 5가지 알아보기](https://gmlwjd9405.github.io/2018/05/11/types-of-git-branch.html)

