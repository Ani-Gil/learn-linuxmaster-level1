Log files
===============
<strong>- /var/log/messages</strong><br>
시스템에서 발생하는 표준 메시지가 기록되는 파일로 대부분의 로그가 이 파일에 쌓이고<br>
root 사용자만이 해당 파일을 읽을 수 있도록 설정되어 있다.<br><br>
<strong>- /var/log/secure</strong><br>
인증을 기반으로 접속과 관련된 로그가 기록되는 파일로 보통 login(telnet & ssh),<br>
tcp_wrappers, xinetd 관련 로그가 쌓인다.<br><br>
<strong>- /var/log/dmesg</strong><br>
시스템 부팅 시 출력되었던 로그가 기록되며, 해당 로그를 커널 부트 메시지 로그라고<br>
지칭한다.<br><br>
<strong>- /var/log/maillog</strong><br>
sendmail, dovecot 등과 같이 메일 관련 작업이 기록되는 로그 파일이다.<br><br>
<strong>- /var/log/xferlog</strong><br>
FTP 접속과 관련된 작업이 기록되는 파일이다.<br><br>
<strong>- /var/log/cron</strong><br>
cron 관련 정보가 기록되는 파일이다.<br><br>
<strong>- /var/log/boot.log</strong><br>
부팅 시 발생되는 메시지가 기록되는 파일로 보통 부팅 시 동작하는 데몬 관련 정보가<br>
기록된다.<br><br>
<strong>- /var/log/lastlog</strong><br>
telnet이나 ssh를 이용해서 접속한 각 사용자의 마지막 정보가 기록되는 파일이다.<br><br>
<strong>- /var/log/wtmp</strong><br>
콘솔, telnet, ftp 등을 이용하여 접속한 사용자 기록, 시스템을 재부팅한 기록 등의<br>
로그가 쌓이는 파일이다.<br><br>
<strong>- /var/log/btmp</strong><br>
wtmp와 반대되는 로그로 접속이 실패한 경우를 기록한다.