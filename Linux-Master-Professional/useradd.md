Command - useradd
===============
사용자의 계정을 생성하는 명령어이며, 동일한 명령어로는 "adduser"가 존재한다.

1. 명령어 사용 형태<br>
useradd [Option] [User name]

2. 명령어 옵션

| Option | Document |
|--------|----------|
| -p     | 사용자를 암호를 생성 시 지정할 수 있다. |
| -d     | 홈 디렉터리를 지정할 때 사용한다. |
| -g     | 그룹을 지정할 때 사용하며, 해당 그룹이 생성되어 있어야한다. |
| -G     | 기본 그룹 이외에 다른 그룹을 추가로 속하게 할 경우 사용한다. |
| -f     | 사용자의 패스워드 만기일을 숫자로 지정한다. |
| -e     | 사용자의 계정 만기일을 YYYY-MM-DD 형식으로 지정한다. |

3. 명령어 사용 예<br>
    - useradd -p TEST1234# anigil<br>
    "anigil" 유저 생성 시 패스워드는 "TEST1234#"으로 지정하여 생성한다.
    - useradd -d /home/test/in-test -g samsung anigil<br>
    "anigil" 유저 생성 시 기본 홈 디렉토리는 "/home/test/in-test"로 지정하며<br>
    기본 그룹은 "samsung"으로 지정하여 생성한다.

4. 알아둘 점<br>
    - 해당 명령어도 "man" 명령어를 사용하여 다른 옵션을 참고해도 된다.<br>
    - "useradd -D"를 입력하면 "/etc/default/useradd"의 파일의 내용을 보여준다.<br>
    해당 파일은 useradd 입력 시 기본적으로 설정되어있는 값을 의미하며, 해당 파일을<br>
    수정하여 새로운 옵션을 가진 기본 유저들을 만들 수 있다.