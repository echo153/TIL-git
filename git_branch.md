# git으로 협업하기 
- Github Flow : Github에서 제안하는 브랜치 전략 

## branch
> 독립적인 작업 흐름을 만들고 관리

- 우아한 기술 블로그 참고 https://techblog.woowahan.com/2553/ 
- git-flow 에는 5가지 브랜치가 존재합니다:
    - 항상 유지되는 메인 브랜치
        - master : 제품으로 출시될 수 있음
        - develop : 다음 출시 버전을 개발
    - 일정 기간만 유지되는 보조 브랜치들
        - feature (topic) : 특정 기능을 개발하고, 완료되면 다시 통합 브랜치로 병합 
        - release : 이번 출시 버전을 준비
        - hotfix : 출시 버전에서 발생한 버그를 수정

### merge (병합)

non fast-forward 병합 : 브랜치를 수정하는 동시에 메인 브랜치에 여러 가지 변경 사항이 적용되는 경우도 있습니다. 그럴 경우에는 두 브랜치의 변경 사항을 하나로 통합해야 합니다. 이 경우 브랜치들이 그대로 남아 있기 때문에 브랜치로 실행한 작업 확인과 관리 면에서 더 유용할 수 있습니다. 


## 브랜치 명령어
```
git branch : 브랜치 목록 보기
git branch '새로운 브랜치 이름' : 브랜치 생성
git branch -d : 브랜치 삭제
git branch -m 이름 : 브랜치 이름 변경 
git checkout '전환하려는 브랜치 이름' : 브랜치를 전환(현재 위치에서 체크아웃해서 원하는 브랜치로 들어감)
git merge 
git log "비교할 브랜치 명 1".."비교할 브랜치 명 2" : 브랜치 간 비교
```

- git checkout을 하고 git log 실행해보면 자동으로 로그가 업데이트 되어 있음 
    ```
    git log
    > commit 26e7f1b7231b063b90036f1a58fc6c7957ff6ee1 (HEAD -> exp, origin/main, main)
    ```

- A 브랜치로 B 브랜치를 병합할 때 (A ← B)
    > git checkout A<br>git merge B




## github branch 실습
1. 원하는 (다른 사람의) 깃헙의 저장소 오픈
2. 우측 상단의 Fork 클릭
3. 원격 저장소 clone 하기: 명력어 입력
    > git clone https://github.com/아이디명/브랜치한저장소주소
    - 윈도우 : 컴퓨터 바탕화면에서 우클릭 해서 vscode 로 열어서 입력
    - 맥북 : terminal 열어서 입력
4. 파일 만들기 (ex. 개인 프로젝트 파트 등)
5. 파일 수정 및 저장 후 git add, commit, push 명령어로 github 에 업로드 
    ```
    git add .
    git commit
    git push origin main
    ```
6. 아까 만들어 둔 본인의 클론된 GitHub 접속하기 
    - 페이지 상단 왼쪽 Pull Requests 버튼 누르기
    - 우측에 초록색 New Pull Request 버튼 누르기

이렇게 하고 메인 브랜치를 확인해보면 끝!


