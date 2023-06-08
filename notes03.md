# github

## vscode 파일 github 에 업로드하기

1. 우측 상단 + 버튼 누르기
2. `+` 메뉴의 create repository 버튼 누르기
3. 'Repository name'란에 이름 설정 후 우측 하단의 create repository 누르기
4. `git remote add origin https://github.com/~~~/` 복사 (url에서 ~~~ 표시 부분에 본인 아이디 넣기)
    - 이 코드의 의미: 저 url을 origin 이라는 변수 이름으로 저장하기
5. vscode의 terminal창에 위 코드를 붙여넣기 
6. `git push -u origin` 입력
    - 원격 저장소로 보내서 origin/main으로 
``` 
입력 결과:
Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (19/19), 4.09 KiB | 4.09 MiB/s, done.
Total 19 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/echo153/TIL.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

## url이 잘못되었을 경우 
- git remote rm origin 
    - 삭제(rm)
- git remote -v
    - 원격저장소 목록 조회

## push, pull
- push 를 하면 로컬 저장소에서 원격저장소인 github에 업로드가 됩니다.
- pull 명령은 원격 저장소의 내용을 가져와서 현재 브랜치와 병합(merge)를 해줍니다. pull을 하면 기존에 작업했던 내용은 유지하면서 최신 코드로 업데이트할 수 있습니다.

### Pull 주의사항

- pull을 하기 전에 commit을 하지 않으면 덮어쓰기 에러가 발생할 수 있기 때문에 기존 작업에 대해 commit을 미리 해두고 pull을 수행해야 합니다.
- pull을 했을 때 로컬과 원격 저장소에 있는 변경 사항이 충돌할 경우에는 수동으로 해결하고 직접 commit을 해 줘야 합니다!!
