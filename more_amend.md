# git 추가 명령어 정리
`git을 사용할 때 상황에 따라 추가적으로 사용되어 질 수 있는 명령어에 대해 정리하는 문서입니다.`

| 명령어             | 작업자 |
|--------------------|--------|
| git revert/reset   | 지원   |
| git commit --amend | 다연   |
| git cherry-pick    | 진우   |
| git rebase         | 민석   |

## git commit --amend
가장 최근 커밋을 수정하는 편리한 방법.
새 커밋을 전체적으로 생성하지 않아도 기존 커밋으로 단계적인 변화를 결합시킬 수 있음.

// 잘못 작성한 커밋 메시지 변경
git commit --amend -m "an updated commit message"

// 커밋된 파일 변경
--no-edit : 커밋 메시지를 변경하지 않아도 커밋을 개정할 수 있음.
git commit --amend --no-edit

* 개정된 커밋은 실제로 완전하게 새로운 커밋임. 
다른 사용자와 공유한 커밋을 개정하면 혼란스러울 가능성이 있으므로 --amend를 사용할 때는 주의해야 함.


### reference
* [Git commit --amend 및 기록을 다시 작성하는 다른 방법](https://ko.atlassian.com/git/tutorials/rewriting-history)
