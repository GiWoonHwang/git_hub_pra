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