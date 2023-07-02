# Linux
모든 명령어는 기본 동작과  추가 동작시 [스페이스] 후 - 기호로 설정한다.
모든 명령어는 내 현재 위치에서 실행된다.
리눅스는 명령어 성공시 아무런 메세지가없다.
(유닉스,리눅스)는 감춰진 파일은 앞에 .이 붙는다.


# 필요한 명령어를 찾는 방법
````
create directory in inux 구글 검색
https://www.cyberciti.biz/faq/linux-make-directory-command/
````

# sudo (super user do)
````
하나의 운영체제를 여러 사람이 사용해야하니 각각의 사용자마다 권한을 부여한다.
apt-get install git : 깃을 설치하는 명령어 실행시 권한이 없다는 Permission denied 가 발생가능
sudo apt-get install git : 권한을 부여받아 설치가 가능하다.
````


# 경로 이동과 현재위치 명령어
cd     : cd 이동할 디렉토리의 경로명
cd     : cd /home/ubuntu 현재 경로에서 이동하는 / (절대경로)
cd ..  : 부모의 디렉토리로 이동하는방식 (상대경로)
ls     : 현재 디렉토리의 파일 목록을 출력하는 명령어.
ls -l  : 현재 내위치의 파일을 자세히보여준다.
ls -al : 모든 상위 경로의 파일의 자세한 파일의 설정을 보여준다. (숨김파일 포함)
ls -alS : -S명령어는 파일사이즈에 따른 정렬은 해준다 al 뒤에 붙여서 명령어들을 조합이가능
mv /이동시킬 디렉토리 [스페이스] /이동시킬 경로 : 파일을 이동시킨다
pwd    : 현재 위치하고 있는 디렉토리를 알려주는 명령어
clear  : 창을 클리어


# tial 파일 읽기 (입력받은 파일의 마지막 부분을 출력하는 프로그램)
````
tail [파일 명] : 마지막10줄을 읽기
tail -n [라인 수] [파일 명] : 해당 라인수 만큼의 라인 읽기
tail -c [바이트 수] [파일 명] : 보여줄 마지막 바이트수
tail [파일 명] [파일 명] : 여러개의 파일 보기
tail -f [파일 명] : 파일 모니터링을 하기 위해선 tail 명령어에 -f 옵션을 사용 이 옵션은 파일의 마지막 10줄을 출력하는데 파일이 새 라인이 추가 될 경우 업데이트를 한다. 일반적으로 로그파일 모니터링에 사용된다.

````

# 파일,또는 디렉토리 생성
mkdir  (이름) : 폴더 생성
mkdir -p (디렉토리)/(디렉토리)/(디렉토리) : 하위 디렉토리가 없다면 순서대로 만들어준다
touch (이름).txt : 파일을 생성한다.

# 디렉토리 삭제
rm 파일명 : 파일 삭제
m -r 디렉토리명 :디렉토리 삭제

# 도움말
ls --help , rm --help : 명령어 뒤에 --help를 붙이면 명령의 사용설명서가 출력
man (명령어) : 공식페이지의 도움 내용이 나온다. f,d로 확인가능
/(검색 명령어) : 찾기기능
q : 빠져나가기
Ctrl+C : 프로세스 종료
Ctrl+Z : 프로세스 정지 (Stop)


# 파일 편집기
nano : 파일 편집기를 연다.


# 패키지 매니저 (apt,yum)
````
ls,mkdir등도 패키지로 처음 설치시 저장되어있다.
sudo apt-get : apt 관련 사용 명령어를 찾을수있다.
````
------
## 자주사용되는 명령어
````
sudo apt-get [명령어]

자주 사용되는 명령어:
  update - 패키지 목록을 새로 가져옵니다
  upgrade - 업그레이드를 합니다
  install - 새 패키지를 설치합니다 (패키지는 libc6 식으로. libc6.deb 아님)
  reinstall - Reinstall packages (pkg is libc6 not libc6.deb)
  remove - 패키지를 지웁니다
  purge - 패키지를 완전히 지웁니다
  autoremove - 사용하지 않는 패키지를 자동으로 전부 지웁니다
  dist-upgrade - 배포판 업그레이드, apt-get(8) 참고
  dselect-upgrade - dselect에서 선택한 걸 따릅니다
  build-dep - 소스 패키지의 빌드 의존성을 설정합니다
  satisfy - Satisfy dependency strings
  clean - 내려받은 아카이브 파일들을 지웁니다
  autoclean - 과거에 내려받은 아카이브 파일들을 지웁니다
  check - 의존성이 망가지지 않았는지 확인합니다
  source - 소스 아카이브를 다운로드합니다
  download - 현재 디렉토리에 바이너리 패키지를 다운로드합니다
  changelog - 특정 패키지의 변경 사항을 다운로드 및 표시합니다

````
