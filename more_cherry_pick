# git 추가 명령어 정리
`git을 사용할 때 상황에 따라 추가적으로 사용되어 질 수 있는 명령어에 대해 정리하는 문서입니다.`

| 명령어             | 작업자 |
|--------------------|--------|
| git revert/reset   | 지원   |
| git commit --amend | 다연   |
| git cherry-pick    | 진우   |
| git rebase         | 민석   |

## git cherry pick
`git commit을 선택해서 현재 branch에 반영하기 위한 명령어

```
// 특정 commit을 현재 브런치로 가져옴
git cherry-pick <commitID>

// 여러개 commit을 현재 브랜치로 가져오기
git cherry-pick <commitID> <commitID>

// 특정 commit을 반영하고 add까지 수행
git cherry-pick -n <commitID>

// 여러개의 커밋을 하나의 커밋으로 합쳐서 반영
git cherry-pick -n <commitID>
git cherry-pick -n <commitID> ... 여러번
git commit -m <commit message>

// cherry-pick이 실패한 경우 현재 상태 빠져나오기
git cherry-pick --quit

// cherry-pick 이전 상태로 돌리고 체리픽을 취소
git cherry-pick --abort
```


### reference
* [누구나 쉽게 이해할 수 있는 Git입문](https://backlog.com/git-tutorial/kr/stepup/stepup7_6.html)
* [Git에서 체리픽을 사용하여 커밋하는 방법은?](https://webisfree.com/2017-04-11/git%EC%97%90%EC%84%9C-%EC%B2%B4%EB%A6%AC%ED%94%BD%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EC%97%AC-%EC%BB%A4%EB%B0%8B(commit)-%ED%95%98%EB%8A%94-%EB%B0%A9%EB%B2%95%EC%9D%80)
