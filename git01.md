<!-- git 특강 day 2 -->
블로그에 더 자세히 다룬 내용 

# github FAQ 및 주의사항 

## git FAQ

1. github에서 영상이나 피피티는 업로드 가능한지?
    - 모든 파일 관리 가능하지만, 문자로 된 것처럼 한 줄 한 줄 변경사항을 확인할 수는 없음 
    - 깃헙 용량 제한 고려해야 함 

2. 깃헙 초록색 네모칸을 채우는 방법은 커밋으로만 가능한지?
    - 초록 네모 칸 채우는 것은 커밋 밖에 안 됨

3. git 터미널에서 README.md 파일을 생성하고 push 했는데 깃헙에서 자동으로 read me를 인식을 해주지 않았습니다 내용이 없으면 자동인식이 안 되는지?
    - 인식 안 되는 이유들: 오타, 내용 없는 파일 등

4. 원격 저장소 생성 후에 이름 또는 GitHub user name을 바꿨을 때는?
    - 로컬에서 원격 저장소 설정을 해주기
    > git remote add origin (https://github.com/바꾼이름)


## github에 올리면 안 되는 코드 처리 방법

- `.gitignore` 명령어를 사용하면 추가되면 안 되는 (무시해야 하는) 파일을 정의해 줄 수 있음. 
- 이 파일에서 정의된 파일은 staging area에 올라가지 않기 때문에 tracking 또한 되지 않는다. 
- `git status` 명령어를 이용했을 때 보이지 않는다!
- 개발자들이 일반적으로 많이 쓰는 gitignore 파일 생성해주는 웹사이트:  https://www.toptal.com/developers/gitignore/ 

