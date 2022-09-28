Tech - Special permissions
===============
- Concept<br>
리눅스의 경우 권한 체계는 사용자, 그룹, 기타 사용자에게 3가지 권한인 읽기,<br>
쓰기, 실행을 부여할 수 있다. 하지만 이러한 권한 체계는 일반적인 상황에서는
적절하겠지만 특정 유저가 Root 권한이 필요한 경우가 간혹 있다. 하지만 이런 경우에<br>
Root 암호를 알려줄 수는 없기에 특수 권한이라는 것이 있다. 리눅스에서 특수권한은<br>
'Set-UID', 'Set-GID', 'Sticky-Bit' 총 3가지가 존재한다. 해당 부분은 보안상의<br>
위험을 초래할 수 있는 부분이므로 신중하게 학습 후 사용하도록 하자.<br>

| Special permission | Document |
|--------------------|----------|
| <center>Set-UID</center> | <center>보통 실행 파일에 사용되며 실행 시 해당 파일을 실행하는 동안에는<br>실행한 사용자의 권한이 아닌 해당 파일의 소유자 권한으로<br> 인식한다. 실행 파일에 주로 사용하므로 설정 시 소유자 권한 부분의 'x'자리에<br> 's'로 표기된다. 만약 실행 권한이 없는 파일에 부여하면 대문자 'S'로 나타난다.</center> |
| <center>Set-GID</center> | <center>Set-GID도 Set-UID와 같은 맥락이다. 해당 파일을 소유한 그룹 권한으로<br>인식하며 주로 디렉터리에 설정되는데, 해당 권한으로 설정된<br> 디렉토리에서 사용자들이 데이터를 생성하면 디렉터리 소유 그룹<br>권한으로 만들어진다. 이 권한의 표시는 그룹 소유권 부분에서<br>'x'자리에 's'로 나타나며, 만약 실행 권한이 없다면 대문자 'S'로 표기된다.</center> |
| <center>Sticky-Bit</center> | <center>디렉터리에 적용되는 특수 권한으로 보통 공유 디렉터리에 사용된다.<br> 보통 '/tmp'에 적용되어 있는데, 일반적인 권한 계층에서<br> 'rwx'로 설정되어 있을 경우, 모든 사용자가 해당 디렉토리에서 파일을<br>생성할 수 있다. 다만 이 경우 문제점이 다른 유저가 또 다른 유저가 <br>생성한 파일을 삭제할 수 있다는 문제점이 나오는데, Sticky-Bit를<br> 설정한다면 생성에는 제한이 없으나 삭제에는 자신이 만든 데이터<br>이 외에는 삭제가 불가능하게 설정할 수 있다. 이 권한 설정은<br> 무조건 Other 계층에서만 설정이 가능하며, 설정하면 Other 계층 권한 부분의<br>'x'자리가 't'로 표기된다. Other 계층에 실행 권한이 없는 경우,<br>즉 그룹의 공유 모드로 사용한 경우에는 대문자 T로 표기된다.</center> |

- Special permission setting<br>
특수 권한도 허가권 설정 명령어인 "chmod"를 사용한다. 문자 모드로 설정하게되면<br>
Set-UID/Set-GID는 's'를 사용하고, Sticky-Bit는 't'를 사용한다. 숫자 모드는<br>
천의 자리가 사용되며 Set-UID는 4, Set-GID는 2, Sticky-Bit는 1의 값을 가지며,<br>
사용 예는 "chmod 1755 /tmp" 형태로 사용할 수 있다.