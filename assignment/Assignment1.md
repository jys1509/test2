## 정보 조사


- git stash ?
- git status 명령어는 깃이 현재 변동된 파일들 중 
- 어떤 파일을 추적하고 있는지 아닌지 확인할 수 있다.
- git add . 다음 got stash 해서 
- 업로드파일이 뭐 남았는지 확인한다 (개인생각)

- git reset ?
- git reset -- hard[commit hash]이렇게 명령어를써서
- 이전 커밋으로 돌리는 방법이다
- 즉 작업도중 파일들이 변경 되었을떄 한번에 되돌리기위해 사용된다

- git revert ?
- git reset 과 같은 명령어지만 부분만 제거하는 명령어이다
- 예를들어 git commit -m "1번커밋" ..3개의 파일을 업로드했을떄
- git revert [1번 commit hash] 이렇게 명령어를 써서
- 1번 파일만 부분 삭제하는 기능이다 


- git reset 과 revert 의 차이
- reset은 전체삭제로
- 혼자만 사용하는 브랜치인 경우
  origin에 있지만 아무도 이 브랜치를 사용하지 
- 않는다는 확신을 가지는 경우 에 사용
- revert는 부분삭제하는경우 에사용 된다 
- 그래서 내 생각에는 회사에서 협업중 reset을 사용하면 
- 다른사람이 변경사항을 내 컴퓨터에서 제거할수있다(위험)그러므로
- got revert를 사용해 변경사항을 제거하기위해 새로운 커밋을
- 추가하는것이므로 헙업시 다른사람들에게 영향을 미치지않는다


## 실습


- 바탕화면에 test2/test2.txt - test2 (Repository) 에 업로드