# git conflict

1. 원래 레포에 test.txt 파일이 있다.
2. fork 했다
3. 원래 레포에서 test.txt 파일을 수정했다.
4. fork 한 레포에서도 test.txt 파일을 수정했다.
5. PR 올렸더니 같은 라인에 있는 내용을 수정해버려 conflict(충돌)이 일어났다.

### 해결하는 방법은?

```
git remote add upstream https://github.com/heunyam/conflict_test_repo
git pull upstream master
```
위 명령어를 싱행한다
```text
<<<<<<< HEAD
fork: 포크된 레포에서 수정된 내용
=======
original: 원래 레포에서의 내용
>>>>>>> 42c41acae191b2e0476bb270a18cffb34e72e427
```
그러면 위와 같이 confilct 된 부분을 나타내준다.
해당 부분을 수정해주고 add commit push 해주면 된다

