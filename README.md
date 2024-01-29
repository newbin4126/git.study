# git.study

깃 공부

깃백업(스테이징)

```
git add (파일명)
```

현재파일상태를 기록해두려면

```
git commit -m '메모'
```

여러파일 스테이징 하려면

```
git add app.txt app2.txt
```

모든파일 스테이징 하려면

```
git add .
```

상태창열기(지금 내가 어떤 파일들을 스테이징 해 놨는지 알 수 잇)

```
git status
```

내가 커밋한 내역을 보고싶으면

```
git log --all --oneline
```

최근 커밋 vs 현재파일 차이점 보여줌
(터미널에 뜨는데 스크롤바 조작하고싶으면 j/k 키)
(q키는 종료)

```
git diff
```

이건 diff명령어를 더 시각적으로 잘 보여줌
(:q 또는 :qa는 종료)

```
git difftool
```

현재파일 vs 특정커밋 비교가능
(git log --oneline --all 치면 앞에 노란색으로 나오는게 커밋아이디)

```
git difftool 커밋아이디
```

브랜치생성(복사본만들기)

```
git branch 브랜치명
```

브랜치로 이동

```
git switch 브랜치명
```

깃 로그 그래프로보기

```
git log --oneline --all --graph
```

브랜치 코드를 메인코드에 합치고 싶을떄(머지)
머짘ㅋㅋㅋㅋ

```
git merge coupon
```

브랜치는 합쳐도 남아있다
merge완료된 브랜치 삭제는

```
git branch -d 브랜치명
```

머지 안한 브랜치 삭제는

```
git branch -D 브랜치명
```

파일 복구하는 법

```
git restore 파일명
```

특정 커밋 시점으로 파일 복구하는 법

```
git restore --source 커밋아이디 파일명
```

스테이징 취소

```
git restore --staged c
```

커밋취소하는법

```
git revert 커밋아이디
```

과거로 모든걸 되돌리기

```
git reset --hard 커밋아이디
```

리셋인데 변동사항 지우지 말고 스테이징해놓기

```
git reset --soft 커밋아이디
```

리셋인데 변동사항 지우지 말고 unstage 해놓기

```
git reset --mixed 커밋아이디
```

코드가 맘에 안들어서 잠깐 삭제하고 싶을 떄
커드를 잠깐다른공간에 보관

```
git stash
```

여기에 메모도 적어서 보관가능

```
git stash save "bbb 코드짰는데 망함"
```

현재 stash되어있는 코드 목록 출력

```
git stash list
```

보관했던 코드 다시 불러오기
가장 최근에 들어온것부터 먼저 나감

```
git stash pop
```
