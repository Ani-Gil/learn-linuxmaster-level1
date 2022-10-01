Command - yum
===============
rpm 기반의 시스템에서 패키지를 손쉽게 설치해주고 자동으로 업데이트를 수행하는<br>
명령행 기반의 유틸리티이다. "rpm" 명령어의 문제들을 개선한 명령어라고 봐도 무방하고,<br>
yum은 소프트웨어 저장소 즉 repository라는 곳에서 자동으로 다운 및 설치를 진행해준다.<br>
Fedora 계열의 'apt'와 유사하다.

1. 명령어 사용 형태<br>
yum [Option] [command] [Package Name]

2. 커맨드 종류

| Command | Document |
|---------|----------|
| list [항목]     | 전체 패키지에 대한 정보를 출력한다. 설치가 되어 있는 경우<br> "installed", 업데이트가 가능한 항목은 "updates"라고 나타난다.<br>기본 항목값은 'all'이고, "installed", "updates" 등의 항목 값을<br> 사용할 수 있다. |
| info [패키지명]     | 패키지에 대한 정보를 출력한다. |
| update [패키지명]     | 패키지를 업데이트할 때 사용한다. |
| install [패키지명]     | 패키지를 설치할 때 사용한다. |
| search [문자열..]     | 문자열이 포함된 패키지를 찾아준다. |
| remove [패키지명]     | 패키지를 삭제할 때 사용한다. |
| group list     | yum에서 제공하는 패키지 그룹에 대한 리스트를 출력한다. |
| group info [패키지 그룹명]     | 특정 패키지 그룹명에 대한 패키지 내용 및 설명 등을 출력한다.|
| group update [패키지 그룹명]     | 특정 패키지 그룹에 대한 업데이트를 진행한다. |
| group install [패키지 그룹명]     | 특정 패키지 그룹에 대한 설치를 진행한다. |
| group remove [패키지 그룹명]     | 특정 패키지 그룹에 대한 삭제를 진행한다. |
| whatprovides     | 특정한 파일이나 기능과 관련된 패키지 정보를 검색할 때<br>사용한다. |

3. 명령어 사용 예<br>
    - yum list<br>
    전체 패키지에 대한 정보를 출력한다. 뒤에 항목 값이 없으면 'all'로 검색된다.
    - yum list installed<br>
    현재 설치되어 있는 패키지들을 출력한다.
    - yum list updates<br>
    현재 설치되어 있는 패키지들 중, 업데이트를 진행해야되는 패키지들을 검색한다.
    - yum info telnet-server<br>
    패키지 "telnet-server"에 대해 검색하여 정보를 출력한다.
    - yum update<br>
    현재 설치되어 있는 패키지들 중, 업데이트가 필요한 패키지들을 모두 업데이트 한다.
    - yum install ssh<br>
    "ssh" 패키지를 설치한다. ('-y' 옵션을 넣으면 질의에 대한 부분을 생략하고 설치한다.)
    - yum search player music<br>
    "player", "music"의 문자열이 포함된 패키지를 찾아준다.
    - yum remove ssh<br>
    설치되어 있는 "ssh" 패키지를 삭제한다.
    - yum group info 'High Availability'<br>
    "High Availability"라는 이름으로 된 패키지 그룹의 정보를 출력한다.
    - yum group install 'CIFS file server'<br>
    "CIFS file server"라는 이름으로 된 패키지 그룹을 설치한다.
    - yum group remove Eclipse
    "Eclipse"라는 이름으로 된 패키지 그룹에 속한 패키지들을 모두 삭제한다.
    - yum whatprovides portmap<br>
    "portmap"과 관련 있는 패키지 정보를 출력한다.

4. 알아둘 점<br>
    - 딱히 없으며, 해당 명령어가 이해가 안될 경우 "man" 명령어를 활용하자.