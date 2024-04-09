# Github Tutorial

(초기 설정)

1. https://hyeo-noo.tistory.com/184 를 참고해서 personal access token을 하나 만든다. </br>
   이제부터 git 작업에서 github 비밀번호 대신 이 토큰이 비밀번호로 사용된다.
   # 240402 토큰 : 
</br>

3. 내 github에 들어가서 repository를 하나 만든다.
</br>

4. 작업중인 폴더이자 repository에 올릴 폴더의 경로에서 git init
</br>

5. git remote add [레포지토리 별명] [레포지토리 주소]
    - [레포지토리 별명]은 보통 origin을 많이  사용하나, 뭐든 상관없다.
    - [레포지토리 주소] 해당 레포지토리의 '<> Code' 에서 복붙한다.
    - name은 깃헙 name, passward는 토큰을 입력한다.

-------------------------------------------------------------------------------------

(반복 작업)

1. 작업중인 폴더이자 repository에 올릴 폴더로 들어간다. cd ~
</br>

2. 파일에서 작업을 진행한다. (수정 사항이 하나도 없으면 git add가 안 됨)
</br>
  
3. git pull [레포 별명] [branch]
    - (예시) git pull origin main 
    - 원격 저장소의 정보를 가져온다.
    - branch는 main이 default이며, 깃헙 사이트의 레포지토리에 들어가면 바로 보이는 화면이 main이다. </br>
      default branch를 변경하고 싶으면 레포지토리의 Setting에서 바꿀 수 있다. </br>
      모든 레포지토리에 대해 default branch를 변경하고 싶으면 계정의 Setting - Repositories에서 바꿀 수 있다. </br>
</br>

4. git add
    - git add .        : 모든 폴더를 한꺼번에 add  
    - git add /폴더/*  : 특정 폴더 안의 모든 파일을 add
    - git add 파일.py  : 특정 파일만 add 
    - git add *.py     : 모든 py 파일만 add 
</br>

5. (선택) git status
      - add가 잘 됐는지 확인.
</br>

6. git commit -m "수정사항에 대한 코멘트"
</br>

7. git push [레포 별명] [branch]
    - 원격 저장소에 반영

-------------------------------------------------------------------------------------

- 기타(branch 관련)
    - git branch : 현재 branch 목록 확인. *이 붙은 것이 현재 branch
    - git branch [new branch]      : 새로운 branch 생성
    - git checkout [new branch]    : branch 변경
    - git checkout -b [new branch] : 새로운 branch 생성하면서 동시에 변경
    - git checkout [branch1] merge [branch2] : branch2를 branch1에 병합
    - git reset -soft HEAD ^ : 로컬 저장소의 커밋을 취소
    - 만약 branch2(master)의 내용을 branch1(main)에 덮어쓰고 싶다면? </br>
      git checkout master </br>
      git branch main master -f </br>
      git checkout main </br>
      git push origin main -f </br>
</br>  
  
- 기타(remote 관련)
  - git remote    : 원격 저장소의 목록 보기
  - git remote -v : 원격 저장소에 대한 자세한 목록 보기
  - git remote rm : 원격 저장소 제거
</br> 
  
- 기타
  - git log -n 10       : 커밋 히스토리 10개 보기
  - git grep "검색 단어" : 저장소 내의 특정 단어가 포함된 파일 검색
  - git clone [url]     : 원격 저장소를 로컬에 다운로드

  
  
  
  
  
