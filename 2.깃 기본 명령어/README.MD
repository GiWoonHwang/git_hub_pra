git init - 지역 저장소로 설정하기
rm -rf .git - git init 취소하기

지역 저장소에 사용자 정보 등록하기
git config user.name "사용자 이름"
git config user.emial "이메일 주소"

모든 프로젝트에 적용 될 사용자 정보 등록하기
git config --global user.name "사용자 이름"
git config --global user.emial "이메일 주소"

cat .git/gitconfig - 깃 설정 파일 확인하기

git remote add origin - 원격 저장소 주소를 지역 저장소에 등록



git status - 현재 프로젝트의 파일 상태를 확인한다.

git config core.autocrlf true - 개행문자 인식 경고 해결


                           git add             git commit 
작업 디렉토리(untraccked) - 스테이징(tracked) - 지역 저장소(tracked)

git log -p - 파일 단위에서 변경 내용을 보여준다.
git log -숫자 - 최근 몇개의 커밋을 보여줄지 
git log --stat - 각 커밋의 통계정보를 볼 수 있다.
git log --pretty=옵션 - 커밋 로그를 보여주는 형식을 지정할 수 있다.

커밋 메세지 수정하기

git commit --amend - 마지막 커밋 에디터 화면을 보여준다.
git commit --amend - m "수정 메세지"
git commit --amend --no-edit - 에디터를 띄우지 않고 커밋 메세지를 수정하지 않겠다.
git commit --amend --author "username 이메일" - 커밋 저자 정보 수정

origin - 특정 원격 저장소를 식별하는 이름이다. 이 말은 새로운 이름으로 또 다른 원격 저장소를 등록해서 사용할 수 있다는 의미이다. 즉 지역 저장소에서 여러 원격 저장소를 등록하고 사용할 수 있다.
git remote add origin2 주소

git clone 원격 저장소 주소 새로운 저장소 이름

git remote update - 지역 저장소에 등록한 원격 저장소의 최신 정보를 가져온다.
git branch -a - 지역 저장소와 원격 저장소의 브랜치 정보를 함께 보여준다.
git branch -d - 브랜치 삭제
git branch -l - 지역 저장소의 브랜치 정보를 보여준다
git branch -r - 원격 저장소의 브랜치 정보를 보여준다
git branch -v - 지역 저장소의 브랜치 정보를 최신 커밋 내역과 함께 보여준다.


git checkout -t origin/test/remote-branch - 브랜치 설정 변경
git checkout -b <브랜치명> - 브랜치를 생성하고 사용할 브랜치로 지정한다

git push origin --delete test/local-branch - 원격 저장소 브랜치 삭제하기
git branch -d test/delete2 - 지역 저장소 브랜치 삭제하기

git pull, git fetch
git pull은 원격 저장소의 벼경 내역을 가져와서 지역 저장소의 작업 브랜치에 병합까지 완료한다. 반면 git fetch는 원격 저장소의 변경 내역을 가져올 뿐 지역 저장소의 작업 브랜치에 병합 작업은 하지 않느다. 즉 git fetch 후 직접 git merge를 수행해 현재 작업 브랜치에 반영해야 한다.

두 브랜치를 병합하는 대신 다른 브랜치의 커밋을 선택적으로 작업 브랜치에 추가해야 할 때도 있다. 그때 사용하는것이 git cherry-pick "추가하려는 커밋 체크섬"

git reset "커밋 체크섬" - 이전 커밋으로 작업 브랜치의 최종 커밋 변경하기

git revert "되돌리려는 커밋 체크섬"

git rebase "재정렬을 위한 기준 브랜치"