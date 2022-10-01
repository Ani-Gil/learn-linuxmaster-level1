Command - rpm
===============
레드햇사에서 만든 패키지 관리 기법으로 해당 명령어를 통해 갱신, 제거, 검증, 질의<br>
등의 관리를 진행할 수 있다. 해당 명령어는 아주 초기때부터 사용되는 명령어이므로<br>
옵션이 상당히 많다. 먼저 사용 형태를 알아보고 각 모드에 맞는 설명과 옵션 및 예시를 보겠다.

1. 명령어 사용 형태<br>
rpm [Option] [패키지_파일명]

2. 모드 및 옵션<br>
    <strong>2-1-1. 설치 및 업데이트 모드</strong><br>
    새로운 패키지를 설치하거나 업데이트를 할 수 있다.
    | Option | Document |
    |--------|----------|
    | -i     | 새로운 패키지를 설치할 때 사용한다. |
    | -U     | 기존의 패키지를 업데이트할 때 사용한다. 만약 업데이트를 하는 데,<br> 기존 패키지가 없을 경우 '-i' 옵션처럼 동작된다. |
    | -F     | 기존의 패키지가 설치되어 있는 경우에만 업데이트를 진행한다. |
    | -v     | 메세지를 자세히 보여준다. |
    | -vv     | 메세지를 '-v' 옵션보다 더 자세히 보여준다. |
    | -h     | 진행 상황을 '#' 기호로 표시한다. |
    | &#8208;&#8208;force     | 기존 버전이 설치되었을 경우에도 강제로 설치할 때 사용한다. |
    | &#8208;&#8208;nodeps     | 의존성 관계를 무시하고 설치한다. (기본적으로 rpm은 의존성 관계가<br>있는 패키지의 경우 의존성 관계가 있는 패키지가 없을 경우 설치하지<br>않지만, 해당 명령어를 통해 무시하여 진행할 수 있다. |
    2-1-2. 명령어 사용 예<br>
    - rpm -i gftp-2.0.19-fc15.i686.rpm<br>
    해당 패키지를 설치한다.
    - rpm -Uvh vsftpd-2.2.2-11.el6_4.1.i686.rpm<br>
    해당 패키지에 설치하며, 해당 패키지가 없는 경우 설치를 진행한다.
    - rpm -Fvh /usr/local/src/*.rpm<br>
    "/usr/local/src"에 존재하는 모든 RPM 패키지에 대해 업데이트를 진행하며,<br>
    설치되지 않은 패키지는 업데이트를 진행하지 않는다.

    <strong>2-2-1. 제거 모드</strong><br>
    설치된 패키지를 제거한다.
    | Option | Document |
    |--------|----------|
    | -e     | 설치된 패키지를 삭제하며, 의존성을 갖는 패키지가 있는 경우 삭제되지 않는다. |
    | &#8208;&#8208;nodeps     | 의존성을 갖는 패키지가 존재하는 경우에도 삭제한다. |
    2-2-2. 명령어 사용 예<br>
    - rpm -e <br>
    ego라는 패키지를 삭제하며, 의존성이 있는 패키지가 존재하면 삭제하지 않는다.
    - rpm -e --nodeps httpd<br>
    httpd 패키지를 제거하는데 의존성이 있는 패키지가 있어도 제거한다.
    
    <strong>2-3-1. 질의 모드</strong><br>
    패키지 관련 정보를 알아내기 위해 사용한다. 보통 '-q' 옵션을 사용하고 추가적으로<br>
    다른 옵션과 함께 사용하여 질의를 수행한다.

    | Option | Document |
    |--------|----------|
    |      |  |
    |      |  |
    
    2-3-2. 명령어 사용 예<br>


3. 알아둘 점<br>
    - 