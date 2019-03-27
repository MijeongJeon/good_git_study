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



##git checkout

과거 특정 commit/branch 지점으로 옮기기위해 사용하는 기본 명령어  

```
## checkout 관련 명령어
```



### reference

* [git scm : 2.2 Git의 기초 - 수정하고 저장소에 저장하기](https://git-scm.com/book/ko/v2/Git의-기초-수정하고-저장소에-저장하기)
* [Outsider's Dev Story : git add -p 와 git commit -v 의 사용](https://blog.outsider.ne.kr/1247)
