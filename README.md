# open-source

top : 현재 OS의 상태를 나타내주는 CLI어플리케이션이다. 메모리 사용량, CPU 사용량 등을 나타내주며 top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여준다.
top 명령어를 치면 이렇게 나온다.
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Frxlg4%2FbtqYfV2LE3L%2FSW5SbyO65ZUa5PggM3KI8K%2Fimg.png)

PID: 프로세서 번호

USER: 유저 이름

PR: 우선순위

NI: 친절도

%CPU: cpu 사용율

%MEM: 메모리 사용율

COMMAND: 사용된 명령어(간단한 표기)

top 명령어 나가려면 q 누르면 된다.

ps : process status의 줄인말이며, 현재 실행중인 프로세스 목록과 상태를 출력하여 보여주는 기능을 한다.
윈도우의 작업 관리자와 비슷하다고 생각하면 된다.

명령어 : 

-p: 프로세서 아이디

-e: 현재 실행 중인 모든 프로세서

-f: 실제 유저명, 개시 시간 등을 표시

-l: 프로세서의 상태, 우선도 등과 같은 상세한 정보를 표시


현재 리눅스 시스템에 떠있는 모든 프로세서들을 출력하는 명령어는 ps -ef이고 아래는 실행사진이다.
![image](https://github.com/HOGIRL312/open-source/blob/main/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202024-05-31%20101500.png)

jobs : 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시한다.

running: 실행 중

stopped: 일시 중단 중

Done: 종료

terminated: 강제 종료됨

sleep을 백그라운드로 실행하고 jobs 명령어로 프로세스 목록을 확인하면

![image](https://github.com/HOGIRL312/open-source/blob/main/jobs.png)

이런식으로 실행 중이라는 뜻인 running이 뜨는것을 볼 수 있다.

kill : 프로세스에 신호를 보내어 그 프로세스를 종료하거나 다시 시작하는 데 사용된다.
기본 구문은 kill [옵션] [ 프로세스ID] 이다.

-1 :hangup, 로그아웃등의 접속이 끊을 때 발생하는 신호(Signal)로 특정 실행 중인 프로그램이 사용하는 설정 파일을 변경시키고 변화된 내용을 적용할때 사용됩니다.

-2 : 현재 작동중인 프로그램의 동작을 멈출때 사용되며, 일반적인 값은 <CTRL>+<c> 입니다.

-9 : 프로그램을 무조건 종료할 경우 사용됩니다.

-15 : 실행중인 프로그램을 정상적인 종료방법으로 프로그램을 종료하는 신호(Signal)로 kill 명령에서 신호(Signal)를 지정하지 않으면 이 신호(Signal)를 사용하여 프로그램을 종료합니다.

kill명령어는 시스템 리소스를 과도하게 사용하거나 응답하지 않는 프로세스를 안전하게 종료하는데 유용하다.
