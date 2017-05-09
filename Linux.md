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
