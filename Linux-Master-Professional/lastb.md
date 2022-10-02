Command - lastb
===============
"last" 명령어와 반대되는 개념을 가진 명령어로, 로그인 실패 정보를 "/var/log/btmp"에<br>
기록하는데 해당 로그인 실패 정보에 대해 출력하는 명령어다. 사용법은 동일하나<br>
root 계정만 사용할 수 있다.

1. 명령어 사용 형태<br>
lastb [Option] [User name]

2. 명령어 옵션

| Option | Document |
|--------|----------|
| -f [File name]     | 로그 로테이션 설정이 되어 있는 경우, 즉 기본 로그파일<br>이외에 다른 로그 파일의 기록을 볼 경우에 사용한다. |
| -n [Number] or -[Number]    | 가장 최근부터 해당 숫자값 만큼만 출력한다. |

3. 명령어 사용 예<br>
    - lastb<br>
    /var/log/btmp에 기록된 정보를 출력한다.
    - lastb anigil<br>
    "anigil" 유저의 로그인 실패 기록을 출력한다.
    - lastb -3 reboot<br>
    가장 최근에 실패한 로그인 기록 3개를 출력한다.
    - lastb -f /var/log/btmp.1<br>
    "/var/log/btmp.1"이라는 파일에 대한 바이너리 값을 출력한다.
    - lastb 2<br>
    "last tty2"와 동일한 명령으로 "/dev/tty2"로 로그인 실패한 정보를 출력한다.

4. 알아둘 점<br>
    - last 명령어와 옵션만 다르므로 쉽게 이해할 수 있다.