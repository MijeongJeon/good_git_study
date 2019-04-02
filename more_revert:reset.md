### git revert/reset

-----

**git revert** 는 상태를 되돌리기 위한 명령어라고 볼 수 있습니다.

```
//가장 최근 커밋을 취소하고 싶을때 
//즉 한단계 이전의 커밋 내용으로 롤백할때 사용
(*소스코드만 보면 한단계 이전으로 돌아간것 같지만, 내부적으로는 롤백에 대한 커밋이 발생한다.)
git revert HEAD 

//밑에 그림과 설명 참고
git revert <되돌릴 커밋> 
```

![image](/Users/gongjiwon/Desktop/good_git_study/images/revert:reset(1).jpg)

예를들어 git revert 2664ce8 이라고 명령어를 치면, '절름발이 범인이다라는 댓글을 발견' 이라고 남긴 커밋까지 취소되고 파일에는 '유주얼 서스펙트 개봉 소식 들음'과 '예매를 하려고 영화를 검색함' 이라는 내용만 남게된다. (2664ce8 바로 이전의 커밋상태로 돌아감. 2664ce8 커밋은 포함되지 않음)

하지만 커밋 이력을 보면 '절름발이 범인이다라는 댓글을 발견'을 revert했다는 커밋이 발생한다. 

---

**git reset** 은 원하는 커밋상태로 돌아가되, 해당 커밋 이후의 이력은 사라지는 명령어입니다.

```
git reset <옵션> <돌아가려는 커밋>
```

자주 쓰이는 옵션에는 hard, mixed, soft 세가지가 있습니다.

이 옵션들은 되돌아갈 커밋 이후에 발생했던 변화에 대해서 어떻게 할지에 대한 것입니다.

```
//hard 옵션은 되돌아가려는 커밋 이후의 모든 내용을 지워 버립니다.
git reset --hard <되돌아갈 커밋>

//soft 옵션은 원하는 커밋상태로 돌아갔지만, 이후의 내용이 지워지지 않고 다시 커밋할 수 있는 상태로 스테이지에 올라가 있습니다.
git reset --soft <되돌아갈 커밋>

//별다른 옵션을 주지 않으면 mixed가 적용됩니다. 원하는 커밋 상태로 되돌려지고, 이후 변경된 내용에 대해 남아있지만 스테이지에 올라가 있지는 않습니다. 
git reset --mixed <되돌아갈 커밋>

+ 아래 그림 예시를 참고해 주세요!
```



//기존 히스토리

![image](./images/revert:reset(2).jpg)



//git reset —hard a3bbb3c

![image](./images/revert:reset(3).jpg)

//git reset —soft a3bbb3c

![image](./images/revert:reset(4).jpg)

//git reset —mixed a3bbb3c

![image](./images/revert:reset(5).jpg)

---

*참고 블로그 

[<https://www.devpools.kr/2017/02/05/%EC%B4%88%EB%B3%B4%EC%9A%A9-git-%EB%90%98%EB%8F%8C%EB%A6%AC%EA%B8%B0-reset-revert/>](<https://www.devpools.kr/2017/02/05/%EC%B4%88%EB%B3%B4%EC%9A%A9-git-%EB%90%98%EB%8F%8C%EB%A6%AC%EA%B8%B0-reset-revert/>)

