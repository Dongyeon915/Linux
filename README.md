````
모든 명령어는 기본 동작과  추가 동작시 [스페이스] 후 - 기호로 설정한다.
모든 명령어는 내 현재 위치에서 실행된다.
리눅스는 명령어 성공시 아무런 메세지가없다.
(유닉스,리눅스)는 감춰진 파일은 앞에 .이 붙는다.
./ 현재 디렉토리의 하위
````

# 필요한 명령어를 찾는 방법
````
create directory in inux 구글 검색
https://www.cyberciti.biz/faq/linux-make-directory-command/
````

# 필요한 파일 찾기 locate,find,whereis,which
````
locate *.txt : 모든 txt파일을 찾는다.

whereis ls :
ls 명령어의 바이너리(실행파일), 소스, 매뉴얼 파일의 위치를 출력한다.
whereis 명령어를 사용하면 바이너리 파일의 위치뿐만 아니라 소스, 매뉴얼의 위치도 알 수 있다.

which : 명령을 사용하면 현재 사용하고 있는 명령어 실행 파일(또는 링크)의 위치를 알 수 있다.

````



# sudo (super user do)
````
하나의 운영체제를 여러 사람이 사용해야하니 각각의 사용자마다 권한을 부여한다.
apt-get install git : 깃을 설치하는 명령어 실행시 권한이 없다는 Permission denied 가 발생가능
sudo apt-get install git : 권한을 부여받아 설치가 가능하다.
````


# 경로 이동과 현재위치 명령어
````
cd     : cd 이동할 디렉토리의 경로명
cd     : cd /home/ubuntu 현재 경로에서 이동하는 / (절대경로)
cd ..  : 부모의 디렉토리로 이동하는방식 (상대경로)
ls     : 현재 디렉토리의 파일 목록을 출력하는 명령어.
ls -l  : 현재 내위치의 파일을 자세히보여준다.
ls -l  [파일명].txt : 해당 파일을 자세히보여준다.
ls -al : 모든 상위 경로의 파일의 자세한 파일의 설정을 보여준다. (숨김파일 포함)
ls -alS : -S명령어는 파일사이즈에 따른 정렬은 해준다 al 뒤에 붙여서 명령어들을 조합이가능
mv /이동시킬 디렉토리 [스페이스] /이동시킬 경로 : 파일을 이동시킨다
pwd    : 현재 위치하고 있는 디렉토리를 알려주는 명령어
clear  : 창을 클리어
````

# tial 파일 읽기 (입력받은 파일의 마지막 부분을 출력하는 프로그램)
````
tail [파일 명] : 마지막10줄을 읽기
tail -n [라인 수] [파일 명] : 해당 라인수 만큼의 라인 읽기
tail -c [바이트 수] [파일 명] : 보여줄 마지막 바이트수
tail [파일 명] [파일 명] : 여러개의 파일 보기
tail -f [파일 명] : 파일 모니터링을 하기 위해선 tail 명령어에 -f 옵션을 사용 이 옵션은 파일의 마지막 10줄을 출력하는데 파일이 새 라인이 추가 될 경우 업데이트를 한다. 일반적으로 로그파일 모니터링에 사용된다.

````

# cat 파일 읽기 및 파일 생성및내용 복사,복제
````
cat [이름].txt : 파일의 내용을 출력해준다.
cat test01.txt > test02.txt : test01.txt내용을 test02.txt로 복사해서 만든다
cat test01.txt >> test02.txt : 새로운 내용이 계속 처음부터 복제되므로 >> 으로 마지막부분에 내용만을 추가할수있다,

````


# 파이프라인
````
하나의 프로그램의 입력은 다른 프로그램의 출력이된다.
````

# grep
````
grep [찾고싶은 정보] [파일].txt : 파일의 내용중 찾고 싶은 정보를 표시해준다.
ex : ls --help | grap sort : help의 대한 정보중 | 파이프 연결을 통해 sort라는 내용을 찾도록 하는 명령어
ex : ls --help | grap sort | grep access
````

# 파일,또는 디렉토리 생성
````
mkdir  (이름) : 폴더 생성
mkdir -p (디렉토리)/(디렉토리)/(디렉토리) : 하위 디렉토리가 없다면 순서대로 만들어준다
touch (이름).txt : 파일을 생성한다.
````
# 디렉토리 삭제
````
rm 파일명 : 파일 삭제
rm -r 디렉토리명 :디렉토리 삭제
````
# 도움말
````
ls --help , rm --help : 명령어 뒤에 --help를 붙이면 명령의 사용설명서가 출력
man (명령어) : 공식페이지의 도움 내용이 나온다. f,d로 확인가능
/(검색 명령어) : 찾기기능
q : 빠져나가기
Ctrl+C : 프로세스 종료
Ctrl+Z : 프로세스 정지 (Stop)
````

# touch (빈파일을 생성한다)
````
touch a.log b.log c.log
````


# 화면 출력(입력)
```
echo [내용] : 입력한 내용을 출력
echo [내용] > perm.txt : 입력한 내용이 perm에 저장된다.
```

# 파일 편집기
````
nano : 파일 편집기를 연다.
````

# 복사(copy)
````
cp *.log testDir : *은 모든 이름의 .log 확장자 파일을 test dir폴더에 저장한다
````


# 패키지 매니저 (apt,yum)
````
ls,mkdir등도 패키지로 처음 설치시 저장되어있다.
sudo apt-get : apt 관련 사용 명령어를 찾을수있다.
````
------
## 자주사용되는 명령어
sudo apt-get [명령어]

자주 사용되는 명령어:
````
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

# ;을 사용한 명령어 연장
````
mkdir test;cd test
````

-------

# 출력된 결과를 저장하기 (IO Redirection)
````
ls -al > result.txt : > 기호를 통해 출력된 결과를 rsult.txt에 저장한다.
````
## > 설정
````
> 기호 앞에는 1> 숫자 1이 숨겨져있으며 이는 standard output으로 에러등 관련된 결과를 저장 하고싶다면 2를 적어줘야한다.
rm result.txt 2> error.log
````
ex) rm [파일].txt 1> [출력결과가있다면저장할 파일].txt 2> [만약 에러가있다면 이곳에저장].log
````
````

------------

# SHELL
````
명령어는 Kernel을 직접 제어하기 어렵기에 SHELL을 통해 Kernel에 전달한다.
취향에 맞는 SHELL프로그램을 선택 할수있다.
````

# SHELL SCRIPT (쉘 스크립트)
### 쉘에서 실행되어야 할 코드들을 적어둔것
````
#!/bin/bash : 아래 작성될 내용은 bash를 통해 해석되야한다.
if ! [ -d bak ]; then : 현재 디렉토리에 bak라는 디렉토리가 존재 하는지 존재한다면
	mkdir bak     : 만약 bak가 존재 하지않는다면 bak 디렉토리를 생성
fi		      : 조건문의 종료 if를 거꾸로
cp *.log bak 	      : 만약 bak가 있다면 모든 log파일을 bak파일에 저장
````

# process (프로세스)
### sudo apt-get install htop : process를 보기 좋은 htop
sudo htop : 실행 클릭시 해당 기준으로 정렬이 가능하다.
````
ps aux | grep apache : 현재 실행중인 프로세스중 apache를 찾는다.
sodo kill [PID]      : 해당 PID 프로세스를 종료한다.
````

------

# 사용자(다중사용자)
````
id : 로그인한 아이디를 확인
who : 현재 접속중인 사용자를 확인
````
------
# super(root) user, user
````
sudo는 super유저의 권한을 실행할때 실행
su - root : super 유저가 되는 명령어


exit : 종료 명령어
````
sudo passwd -u root : super유저 잠금해제
````
````

# 사용자 권한
````
ls -l dong.txt : 사용시 -rw-rw-r-- 1 dong dong 7590  7월  3 16:33 dong.txt 권한 정보 (owner,group,other) 순서
````
--------
# 권한 설정 chmod(모드)
````
chmod o+x dong.txt : ohter 사용자가 실행가능하게
chmod o-x dong.txt : ohter 사용자가 실행할수 없게
chmod u+x dong.txt : owner 설정시
chmod g+x dong.txt : group 설정시
````

exit : 종료 명령어 
sudo passwd -u root : super유저 잠금해제
````
````

# 사용자 권한
````
ls -l dong.txt : 사용시 -rw-rw-r-- 1 dong dong 7590  7월  3 16:33 dong.txt 권한 정보 (owner,group,other) 순서
````
--------
# 권한 설정 chmod(모드)
````
chmod o+x dong.txt : ohter 사용자가 실행가능하게
chmod o-x dong.txt : ohter 사용자가 실행할수 없게
chmod u+x dong.txt : owner 설정시
chmod g+x dong.txt : group 설정시
````

# 유저(사용자) 추가(비밀번호 변경,속성 변경,삭제)
````
adduser dong : dong이라는 유저가 생성
adduser --uid -0915 dong : dong 사용자를 생성하면서 사용자 ID를 0915로 지정
adduser --gid 1000 dong : 유저를 생성하면서 그룹 ID가 1000인 그룹에 dong 사용자를 포함시킨다.
adduser --home /newhome dong : 유저를 생성하면서 홈 디렉토리를 /newhome으로 지정
adduser --shell /bin/csh dong : 유저를 생성하면서 기본 셸을 /bin/csh로 지정
````
````
passwd dong : 사용자의 비밀번호르 변경
````
````
usermod --shell /bin/csh dong : dong 사용자의 기본 셸을 /bin/csh로 변경
usermod --groups ubuntu dong : 사용자의 보조 그룹에 buntu 그룹 추가
````
````
userdel dong : 사용자를 삭제 단,홈 디렉터리는 삭제 되지 않음
userdel -r dong : 사용자를 삭제하며 홈 디렉토리 같이 삭제
````


# 그룹 생성(삭제,수정)
````
groupadd [그룹이름]
groupadd --gid 2222 dong : dong : 그룹을 생성하며 그룹 id를 2222로 지정
groupmod -new-name dong dong915 : 그룹을 생성하면서 그룹이름을 dong915로 변경
groupdel dong : 그룹을 삭제 (해당 그룹을 주요 그룹으로 지정한 사용자가 없어야 한다)
````

---------# 하****드디스크 관리: RAID****

# RAID

```
여러 물리적 디스크를 묶어서 그룹으로 만들어 하나의 논리적인 디스크
비용 절감,신뢰성 향상,성능 향상의 효과
논리적 디스크를 LU(Local Unit)이라 한다.
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/484b29a1-1b8f-438f-b938-1c51aecf6bcb/Untitled.png)

# 패리티(Parity)

```
**데이터를 항상 부가하고 보존하는 것으로, 어느 한 쪽 HDD가 고장난 때에도,
 거기서 잃어버린 분의 데이터를 패리티로부터 생성할 수 있다
패리티는 HDD에 장애가 발생한 뒤에 데이터를 복원하기 위해서 사용되는 부호로
RAID에 데이터를 쓸 때에 자동적으로 생성됩니다.
남아 있는 데이터와 패리티를 조합하는 것으로, 데이터를 복구할 수 있습니다**
```

# RAID

[RAIDとは何か？知っておきたい基礎知識-ELECOM WEB SITE!](https://www.elecom.co.jp.k.gj.hp.transer.com/pickup/column/storage_column/00003/)

```
Linear RADE : 최소 2개의 하드디스크가 필요,앞 디스크부터 차례로 저장 (공간효율 좋음)
						(디스크 크기가 다르다면 순차적으로 채워지니 사용성 좋음)

RAID0 : 동시저장으로 저장속도는 빠르지만 하나라도 고장날시 모든 데이터가 사라진다. (중요 데이터 저장X)
			ex) 김 , 동 , 연 이런식으로 나눠서 저장한다.

RAID1 : 모든 디스크에 데이터를 N개로 복제하여 각 디스크에 저장,두배의 공간효율(공간효율 나쁨)
한쪽에 데이터가 고장나도 데이터 손실이없다.
			ex) 김동연,김동연 두개가 저장된다

RAID5 : 1개까지의 고장을 허용하지만 2개가 고장날시 사용불가 (공간효율 X)
				최소 3개이상의 하드 디스크가 필요하며, 오류 발생시 패리티를 이용해서 데이터를 복구

RAID6 : RAID5와 비슷 2개까지 고장을허용 패리티를 2중으로 생성한다.(공간효율 X)
				패리티를 2개를 써야하니 최소 4개의 디스크가 필요하다
```

---

# 실습

# RAID 생성용 하드 만들기

```
SCSI 0:7은 VM설정으로 8부터 생성된다
```

![20230710_181522.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/79f73033-d8d4-43d7-a545-f0e0bb22b764/20230710_181522.png)

# 확인

![20230710_181712.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/83dc2354-9f8e-4a04-b38c-a6ad8014bf05/20230710_181712.png)

```
모든 sd확인
```

# 그 후 파티션 생성 순서대로 진행

![20230710_182338.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7030ef62-e818-4861-bdfe-69ab77c9e016/20230710_182338.png)

타입을 변경해 줘야한다.

![20230710_182443.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6964a85f-6f80-425b-b9b0-828c01db657d/20230710_182443.png)

L 명령어로 타입 종류 확인가능

fd 명령어로 타입을 Linux raid auto설정 

![20230710_183440.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1722c116-0458-4885-b4a0-752d1996e174/20230710_183440.png)

정상적으로 파티션 작업이 끝나면 끝에1로 나눠진걸 확인

```
sudo fdisk -l /dev/sdj 명령어로 설정값을 다시 확인 가능
```

![20230710_184214.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/40090201-6fb4-4fa0-88ab-5ceca291cf6b/20230710_184214.png)

## mdadm

```
처음 디스크를 만드는 방법에서 마찬가지로 두가지 디스크를 하나의 RAID로 합치는 명령어
초기에 없으므로 설치해줘야한다.
원칙상 /dev/md[숫자]로 만들어주는게 좋다.
```

## mdadm --create /dev/md9 --level=linear --raid-devices=2 /dev/sdd1 /dev/sde1

```
 원칙상 /dev/md[숫자]로 만들어주는게 좋다.
mdadm을 create만든다 /dev/md1이라는 곳에 linear을 만든다 raid 장치는 2개를 사용한다 
그장치는 sdb1,sdb2이다
```

## 확인

```
mdadm --detail --scan
```

![20230710_202750.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/53556a35-1a03-469a-96ef-0f8aa779a6d8/20230710_202750.png)

## mkfs.ext4 [포맷장소] 명령어 포맷작업

```
ex) mkfs.ext4 /dev/md9
```

## 디렉토리 생성후 마운트

**raidLinear** 디렉토리로 마운트했다. **(본인경로에 파일이 자동완성되는지 잘 확인)**

![20230710_203607.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f67ee7c4-7dd0-4cc8-9393-531184cba30b/20230710_203607.png)

---

# 정상적으로 합쳐진 장치확인

```
mdam --detail /dev/md9
```

![20230710_203916.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b4a4c69c-1bbb-4df8-bf58-487a72bd478e/20230710_203916.png)

완료 후  fstab설정 하기

---

# 다른 RAID 생성시

생성 레이드 명령어만 변경 후 나머지 내용은 위 방법으로 생성하면된다.
