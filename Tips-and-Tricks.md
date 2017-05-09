### Awk and Regular Expressions to Filter Text
```
awk -F':' '{ print $1 }' /etc/passwd (. usernames will be print the the first field)

awk '{print NR "- " $1 }' /etc/passwd (To print the first item ($1) and then the second last item )

awk '/localhost/{print}' /etc/hosts  ( awk will match line having localhost in the  /etc/hosts file)

```

### SSH  Port advanced tunneling
```
ssh -R 9000:localhost:3000 root@NyaMeeEain.com
ssh -L 775:192.168.1.111:80 root@ssh.NyaMeeEain
ssh -D 775 root@NyaMeeEain
ssh -f -N -D 9050 alice@192.168.1.22(-N  instructs Mean  SSH to not send any remote commands
ssh -f -N -D 8080 alice@172.168.4.30 -p 2222
proxychains rdesktop 10.10.2.88 -u Administrator -p password -g 90%

```

### Operating System
```
cat /etc/issue
cat /etc/*-release
cat /etc/lsb-release      # Debian based
cat /etc/redhat-release   # Redhat based

```

### Applications & Services
```
ps aux
ps -ef
top
cat /etc/services

```

### Which service(s) are been running by root?

```
ps aux | grep root
ps -ef | grep root
```

### What applications are installed

```
ls -alh /usr/bin/
ls -alh /sbin/
dpkg -l
rpm -qa
ls -alh /var/cache/apt/archivesO
ls -alh /var/cache/yum/
```

### Any of the service(s) settings misconfigured

```
cat /etc/syslog.conf
cat /etc/chttp.conf
cat /etc/lighttpd.conf
cat /etc/cups/cupsd.conf
cat /etc/inetd.conf
cat /etc/apache2/apache2.conf
cat /etc/my.conf
cat /etc/httpd/conf/httpd.conf
cat /opt/lampp/etc/httpd.conf
ls -aRl /etc/ | awk '$1 ~ /^.*r.*/
```
### What jobs are scheduled

```
crontab -l
ls -alh /var/spool/cron
ls -al /etc/ | grep cron
ls -al /etc/cron*
cat /etc/cron*
cat /etc/at.allow
cat /etc/at.deny
cat /etc/cron.allow
cat /etc/cron.deny
cat /etc/crontab
cat /etc/anacrontab
cat /var/spool/cron/crontabs/root
```
### What other users & hosts are communicating with the system

```
lsof -i
lsof -i :80
grep 80 /etc/services
netstat -antup
netstat -antpx
netstat -tulpn
chkconfig --list
chkconfig --list | grep 3:on
last
```
