# 오늘 수업 내용(Today I Learn)
2025-07-18
## git revert
```
git revert <commit id>
```
- 특정 커밋을 없었던 일로 만드는 작업
- 커밋 수정은 권하지 않음 
- 단일 commit을 실행 취소하는 것
- 프로젝트 기록에서 커밋을 없었던 일로 처리 후에 그 결과를 새로운 커밋으로 추가함
- 변경 사항을 안전하게 실행 취소할 수 있도록 도와주는 순방향 실행 취소 작업

## git reset
```
git reset [옵션] <commit id>

[--soft] : 삭제된 commit의 기록을 staging area에 남김
[--mixed] : 삭제된 commit의 기록을 working directory에 남김(기본 옵션 값)
[--hard] : 삭제된 commit의 기록을 남기지 않음, 말 그대로 삭제
```
- 특정 commit으로 되돌아가는 작업
- 특정 commit으로 되돌아갔을 때, 되돌아간 commit 이후의 commit은 모두 삭제

## 파일 내용을 수정 전으로 되돌리기 : git restore
- 수정(Modified) 상태의 파일 되돌리는 작업
- Working Directory에서 파일을 수정한 뒤, 파일의 수정 사항을 취소하고 원래 모습대로 되돌리는 작업
- 원래 파일로 덮어쓰는 원리이기 때문에 수정한 내용은 전부 사라짐
- 수정 취소 후에는 해당 내용을 복원할 수 없음

## Staging area에 올라간 파일을 Unstage 하기
```
git rm --cached
: Staging Area에서 Working Directory로 되돌리기
-> git 저장소에 "commit이 없는 경우"
git restore --staged
: Staging Area에서 Working Directory로 되돌리기
-> git 저장소에 "commit이 존재하는 경우"
```



