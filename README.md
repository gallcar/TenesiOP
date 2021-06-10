# TenesiOP

테네시 오픈 파일럿 도움말

Git Pull 명령어 작업시에 SSL 에러 표시가 나오면서 업데이트가 안될때! 
  -> SSH 터미널에 접속해서 export GIT_SSL_NO_VERIFY=0 실행한다..

SSH터미널에서 VI,VIM명령어로 화일 내용을 수정하는 명령.. 
주요 명령 : 
  현재 편집 화일에서 나가기 => :q (키보드의 클론을 누르고 영어 q를 누른다 : 이걸 누른후에는 명령어 입력한다는 의미) 
  현재 편집 화일 저장하기 => :w (:wq 라면 저장하고 나가기가 된다)
  현재 편집 화일 저장안하고 나가기 => :qi 편집실수등을 보완..

  현재 커서위치에서 키보드의 i를 누르면 => 하단부에 insert가 나오면서 추가 모드가 된다.. ESC 누르면 취소 
  현재 커서위치에서 키보드의 r를 누르면 => 하단부에 아무것도 안나오고 입려되는 문자를 입력해서 바뀐다.. 
  현재 커서위치에서 키보드의 dd를 누르면 => 해당줄을 모두 삭제한다.

키보드 u를 누르면 입력해서 수정한것을 취소해서 원래되로 되돌린다...

운전 종료하고 이온폰이 자동으로 꺼지는 시간 설정하기.. 
  터미널 접속후 
  
  vim /data/openpilot/selfdrive/shutdownd.py
  60초 * 1.00 은 60초로 1분후 종료.. 수정후 :wq

이온 화면을 강제로 어둡게 하거나 밝게 하기.. 
  터미널 접속후
  
  vim /data/openpilot/selfdrive/hardware/eon/hardware.h 
  
  //percent = 15;
  주석처리를 할경우에 (자동모드로 변경할경우) //를 넣어준다..  
  수정하고 :wq 
  
  percent = 15; // 배터리리스-다이오드방식에서 화면 밝기 적게 해보기

100퍼센트 밝기중에서 15프로 밝기로 어둡게 설정된 상태.. 수정하고 :wq

------21년 6월 10일 초보와 고수도 봐야 하는 오픈파일럿 셋팅 관련된 내용 저장-------

다운로드 링크 
- 테네시 파일럿 전용 SSH접속시 필요한 ppk 화일 다운로드 경로 - 암호로 다운로드 가능함..
http://naver.me/xv0Ig0d5 
- Ntune 앱설치 다운로드.. 
https://drive.google.com/file/d/1-EPga-ukGl9p4SsTMCKfJs6zrZpZ6dqC/view?usp=sharing 
- 터보클라이언트로 SSH터미널이 아닌 상태에서 접속해서 수정이 가능한 앱으로 추천!  
https://play.google.com/store/apps/details?id=turbo.client 
- ssh 터미널앱으로 vim으로 편집가능한 앱이며 되도록 필수로 설치를 요하는 앱.. 특히나 ssl에러시에 필수다..
https://play.google.com/store/apps/details?id=com.sonelli.juicessh 

