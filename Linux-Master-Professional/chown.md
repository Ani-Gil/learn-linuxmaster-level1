Command - chown
===============
파일이나 디렉터리의 소유권 및 그룹 소유권을 변경하는 명령어이다. "chgrp" 라는<br>
명령어가 존재하긴 하나, "chown"명령어만으로도 수정할 수 있어서 웬만해서는<br>
"chown" 명령어를 사용한다.<br>

1. 명령어 사용 형태<br>
chown [Option] [owner:group] [file(s)]

2. 명령어 옵션<br>
(옵션의 경우 사용하지 '-R' 제외하고 사용하지 않는것이 대부분이므로 기입하지 않겠다.)

3. 명령어 사용 예<br>
    - chown -R AniGil *<br>
        하위에 존재하는 모든 데이터를 포함하여 소유자를 "AniGil" 유저로 지정한다.
    - chown anigil:samsung test.txt<br>
        test.txt 파일에 대해 소유자를 "anigil"로 지정하고 소유 그룹을 "samsung"으로<br>
        지정한다.
    - chown 700 test.txt<br>
        test.txt 파일에 대해 UID가 500인 사용자를 소유자로 지정한다.
    - chown :samsung test.txt<br>
        test.txt 파일에 대해 소유 그룹을 samsung으로 지정한다.

4. 알아둘 점<br>
    - 해당 명령어는 딱히 없다.