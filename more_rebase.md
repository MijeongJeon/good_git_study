# git 추가 명령어 정리
`git을 사용할 때 상황에 따라 추가적으로 사용되어 질 수 있는 명령어에 대해 정리하는 문서입니다.`

| 명령어             | 작업자 |
|--------------------|--------|
| git revert/reset   | 지원   |
| git commit --amend | 다연   |
| git cherry-pick    | 진우   |
| git rebase         | 민석   |

## git rebase
`git rebase`는 branch의 이미 commit된 내용들에 대하여 수정할 수 있는 기능을 지원함.  
> (push된 commit들에 대해서도 rebase가능하나 권장하지 않음)

```
// 최근 3개의 커밋을 수정
git rebase -i HEAD~3

// rebase 작업 종료
git rebase --continue

// rebase 작업 중지
git rebase --abort

// 다양한 명령어 옵션 확인
git rebase --help
```


### reference
* [누구나 쉽게 이해할 수 있는 Git입문](https://backlog.com/git-tutorial/kr/stepup/stepup7_6.html)
