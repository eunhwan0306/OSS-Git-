## git reset, revert 

> **git reset**

- **git reset** : 커밋 이력 재설정 수행  

  - 되돌린 이후 커밋 이력 제거 => 특정 커밋으로 되돌아가기
  
  - ex) 커밋이 1 2 3 4 5 6이 있는데 2로 이동시 3 4 5 6 이력 삭제됨

<br>

- **git reset --soft** : reset 이후 커밋 내용만 수정

  - 바로 다시 커밋 가능한 상태로 남아있음 
  
  - 다시 마지막 이전 head로 돌아가려면 commit만 하면 됨
<br>

- **git reset --mixed** : reset 이후 커밋 내용과 staging 가 같음, working 수정 안함

  - head 내용을 stage에 복사 
  
  - 다시 이전으로 돌아가려면 add, commit 필요 
<br>

- **git reset --hard** : reset 이후 커밋 내용=wd=staging 모두 동일

  - head 내용을 wd에 복사, stage에 복사 
  
  - 다시 이전으로 돌아가려면 수정, add, commit 필요 

 
<br>

- 세가지 모두 head가 이동하려는 커밋아이디로 이동

- **git reset --hard orig_head** : reset 이후 다시 원상태로 되돌리기

- **git reflog** : 모든 커밋 이력을 보여줌 

<br>

> **git revert**

- **git revert** : 특정 커밋 이력을 **취소**하고 바로 이전 상태로 돌아가는 방법 수행

  - 현재까지의 커밋이력에 되돌아간 커밋 이력이 추가됨
  
  - a b c d가 있을 때 git revert b 하면 a로 이동


- **git revert [커밋아이디]** : 커밋을 추가로 수행

  - 기본 편집기에서 커밋 메시지 편집 화면 실행 

- **git revert head --no-edit** : 편집 화면 없이 이전 커밋 메시지가 커밋메시지로 사용됨
