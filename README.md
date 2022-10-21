# linux-privilege-escalation-checklist

https://steflan-security.com/linux-privilege-escalation-checklist/

https://gtfobins.github.io/

which awk perl python ruby gcc cc vi vim nmap find netcat nc wget tftp ftp tmux screen nmap 2>/dev/null

sudo -l

sudo su

id;who;whoami;w;last;cat /etc/passwd; cat /etc/sudoers;cat /etc/group

uname -a ; lsb_release -a; cat /proc/version /etc/issue /etc/*-release

ls -la ~/; ls -la /var/mail /home/*/ /var/spool/mail /home/*/.bash_history /var

cat /etc/passwd ; cat /etc/shadow; ls -la /etc/passwd /etc/shadow

ls -la /root/.bashrc or ls -la /home/*/.bashrc; locate .bashrc; find / -name .bashrc -xdev 2>/dev/null

ps aux | grep root

find / -perm -u=s -type f 2>/dev/null; find / -perm -4000 -o- -perm -2000 -o- -perm -6000 2>/dev/null

ls -la /home /root /etc/ssh; locate id_rsa; locate id_dsa; cat /home/*/.ssh/id_rsa

find / -perm -0002 -user root 2>/dev/null

find / -type f -user stef -xdev 2>/dev/null; find / -type d -user stef -xdev 2>/dev/null

sudo -V | grep “Sudo ver”

netstat -antup

cat /etc/profile; cat /etc/bashrc; cat ~/.bash_profile; cat ~/.bashrc; cat ~/.bash_logout

crontab -l; ls -alh /var/spool/cron; ls -al /etc/ | grep cron; ls -al /etc/cron*; cat /etc/cron*; cat /etc/at.allow; cat /etc/at.deny; cat /etc/cron.allow; cat /etc/cron.deny; cat /etc/crontab; cat /etc/anacrontab; cat /var/spool/cron/crontabs/root
./pspy > pspy-out.txt

cat /etc/fstab

getcap -r / 2>/dev/null

showmount -e X.X.X.X; mount X.X.X.X:/ /tmp/

ls -alh /usr/bin/ /sbin/ /var/cache/apt/archives /var/cache/yum/; dpkg -l; rpm -qa

Credential re-use

tmux ls; tmux attach -t tmuxname; screen -ls; screen-dr sessionname; byobu list-session;

gdb -p SERVICE; gdb PROCID
