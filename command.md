# 명령어

> **기초**
- pwd : 현재 자신이 있는 디렉토리를 보여줌
- cd 디렉토리 이름 : 다른 디렉토리로 이동

    - cd .. : 현재 위치하고 있는 폴더의 상위폴더로 이동

- rm -rf 디렉토리 이름: 디렉토리 삭제 
- ls -a : 현재 디렉토리 안에 있는 파일 목록 출력 
- ls -al : 현재 디렉토리 하부 파일 목록을 자세히 출력 
<br>

> **git config**
- cat ~/.gitconfig : 전체 설정 파일을 화면에 출력
- cat .git/config : 지역 설정 파일 내용 출력
- git init 폴더 이름 : 저장소 생성  
- git config --global user.name(email) ~ : 깃 전체 사용자 설정
- git config user.name(email): 지역 저장소 사용자 설정 
- git config (--global) --unset user.name(email) : 전역(지역) 설정 삭제
 
 
- git config --global core.editor notepad : 편집기 환경 설정 (메모장으로 파일 열기)
- git config --global core.editor 'code --wait' : visual studio code로 파일 열기
- git config --global -l : 환경 설정 간단히 출력
- git config -l : 모든 설정 내용 출력
- git config --global init.defaultbranch main : 브랜치 이름 바꾸기(전역 전체 설정에서 지정 가능)
- git config -e : 지역 설정 파일을 열어 수정할 수 있게 편집기 열기 
- git config --global -e : 현재 전역 설정 파일을 열어 편집

<br>

> **버전 관리**
- echo > 내용 : 기존에 있던 내용 삭제 후 새로운 내용 추가
- echo >> 내용 : 기존 내용 뒤에 마지막으로 추가
- git status (-s) : 현재 상태 보기 (간단하게 표시)
    
    - untracked 파일은 빨간색 물음표 2개로, 처음 커밋된 건 녹색 A로 표현

- git add : staging area에 저장
- git commit -m '메시지' : commit 하기 (git repository로 이동)

    - 저장소의 현 상태를 저장하는 행위

    - 어느 시점의 파일 추가/변경 사항을 저장소에 기록

- git commit -am '메시지' : add, commit을 한 번에 하기 
- git commit --amend : 커밋 메시지 바꾸기 
- git log(--oneline) : 커밋 이력을 출력 (간단하게 한 줄로 표시)
- git log head : 가장 최근 커밋 이력 출력
- git show : 현재 브랜치의 가장 최근 커밋 정보 확인
- git show head^ : 제일 최근 커밋 바로 이전의 커밋에 대한 정보 표시
- git show head^^ : 제일 최근 커밋 바로 이전의 이전 커밋에 대한 정보 표시

    - ^ : 이전이라는 의미 

- git config --global alias.명령어 이름 '원래 이름' : 명령어의 별칭 저장
