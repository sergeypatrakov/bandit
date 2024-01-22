## Bandit 🐱‍💻

### <https://overthewire.org/wargames/bandit/>

Если все совсем плохо, то здесь ты сможешь найти ответы

<details>
<summary>Level 0:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit0 
```
```bash
cat readme
```
</details>

<details>
<summary>Level 1:</summary> 

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit1
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL 
```
```bash
cat ./-
```
</details>

<details>
<summary>Level 2:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit2
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

```bash
cat 'spaces in this filename'
```
</details>

<details>
<summary>Level 3:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit3
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
```bash
cd inhere/
ls -a
cat .hidden
```
</details>

<details>
<summary>Level 4:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit4
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
```bash
cd inhere/
ls -a
file ./-* - printf files format
cat ./-file07
```
</details>

<details>
<summary>Level 5:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit5
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```

```bash
cd inhere/
ls -a
find -readable -size 1033c
cat ./maybehere07/.file2
```
</details>

<details>
<summary>Level 6:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit6
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
```bash
find / -type f -group bandit6 -user bandit7 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```
</details>

<details>
<summary>Level 7:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit7
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
```bash
cat data.txt | grep millionth
```
</details>

<details>
<summary>Level 8:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit8
TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
```bash
sort data.txt | uniq -u
```
</details>

<details>
<summary>Level 9:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit9
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
```bash
strings data.txt | grep ==
```
</details>

<details>
<summary>Level 10:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
```bash
base64 -d data.txt
```
</details>

<details>
<summary>Level 11:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

or cyberchef (ROT13) - just Google it!

</details>

<details>
<summary>Level 12:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit12
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
```bash
mkdir /tmp/h0mme
cp ./data.txt /tmp/h0mme
xxd -r data.txt data.bin
file data.bin
mv data.bin data.gz
gzip -d data.gz
file data
mv data data.bz
bzip2 data.bz
file data
mv data data.gz
gzip -d data.gz
file data
mv data data.tr
tar -xf data.tr
file data5.bin
tar -xf data6.bin
mv data6.bin data6.bz
bzip2 -d data6.bz
file data6
xxd data6
tar -xf data6
file data8.bin
mv data8.bin data8.gz
gzip -d data8.gz
file data8
cat data8
```

</details>

<details>
<summary>Level 13:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit13
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
```bash
ls
cat sshkey.private | Control + C
exit
touch sshkey.private
vim sshkey.private | Control + V | :wq!
chmod 700 sshkey.private
ssh -I sshkey.private bandit.labs.otherthewire.org -p 2220
-l bandit14
```

</details>

<details>
<summary>Level 14:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
```bash
ls
cat /etc/bandit_pass/bandit14
nc localhost 30000 fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq OR:
telnet localhost 30000 fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```

</details>

<details>
<summary>Level 15:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
```bash
cat /etc/bandit_pass/bandit15 jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt | Control + C openssl s_client -connect localhost:30001 Control + V
```
OR
```bash
ncat —ssl localhost 30001
```

</details>

<details>
<summary>Level 16:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
```bash
nmap -sV localhost -p 31000-32000
31790/tcp open ssl/unknown
openssl s_client -connect localhost:31790
JQttfApK4SeyHwDlI9SXGR50qclOAil1
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57S
UdyJ
imZzeyGC0gtZPGujUSxiJSWI/
oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/
GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/
kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/

 w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/
zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx
3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P2
9ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnP
w9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlp
mS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sO
mama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRR
hORT
8c8hAuRBb2G82so8vUHk/
fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEA
ypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/
b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5Si
Wg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V
5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/
lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/
WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOm
L8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/
ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/
9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9
Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTa
kzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```

</details>

<details>
<summary>Level 17:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
```
```bash
diff passwords.old passwords.new (second line because password.new is second)
```
OR
```bash
sort passwords.old passwords.new | uniq -u
password 1
password 2
cat passwords.new | grep password 1
cat passwords.new | grep password 2
password 2
```

</details>

<details>
<summary>Level 18:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit18
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
```
```bash
ssh bandit.labs.overthewire.org -p 2220 -l bandit18 cat readme
password
```
OR
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash
cat readme
```

</details>

<details>
<summary>Level 19:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit19
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
```bash
ls -la
./bandit20-do ls
./bandit20-do cat /etc/bandit_pass/bandit20
```

</details>

<details>
<summary>Level 20:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
```bash
ls
echo -n 'VxCazJaVykI6W36BkBU0mJTCM8rR95XT' | nc -l -p 1234 &
```

</details>

<details>
<summary>Level 21:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit21
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```
```bash
vim /etc/cron.d
cat /etc/cron.d/cronjob_bandit22
cat /usr/bin/cronjob_bandit22.sh
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
```

</details>

<details>
<summary>Level 22:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit22
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```
```bash
vim /etc/cron.d
cat /etc/cron.d/cronjob_bandit23
cat /usr/bin/cronjob_bandit23.sh
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
cat /tmp/8ca319486bfbbc3663ea0fbe81326349
```

</details>

<details>
<summary>Level 23:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```
```bash
vim /etc/cron.d
cat /etc/cron.d/cronjob_bandit24
cat /usr/bin/cronjob_bandit24.sh

mktemp -d
cd /tmp/tmp.(some_number)
vim bandit24_pass.sh
```
![bandit23](./screenshots/bandit_23.png "bandit23")

```bash
chmod 777 bandit24_pass.sh
chmod 777 /tmp/tmp.xy3yen6GKj
touch password
chmod 777 password
ls -la
cd /var/spool/bandit24/
ls -la
cd /tmp/tmp.xy3yen6GKj
cp bandit24_pass.sh /var/spool/bandit24/foo
cat password
```

</details>

<details>
<summary>Level 24:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit24
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```
```bash
mktemp -d
cd /tmp/tmp.VAfGXJ1PB
vim brute_force_pass.sh
```

![bandit24](./screenshots/bandit_24.png "bandit_24")

```bash
chmod +x brute_force_pass.sh
ls
./brute_force_pass.sh
sort result_2.txt | grep "Wrong!"
```

</details>

<details>
<summary>Level 25:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit25
p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
```
```bash
ls
cat bandit26.sshkey
cat /etc/passwd | grep bandit26
cat /usr/bin/showtext
ls -la /usr/bin/showtext
ssh -i bandit26.sshkey localhost -p 2220 -l bandit26 (с самым маленьким терминалом)
v - заходим в VIM
:set shell=/bin/bash
:shell
cat /etc/bandit_pass/bandit26
```

</details>

<details>
<summary>Level 26:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
```bash
ls
whoami
whoami ./bandit27-do
./bandit27-do cat /etc/bandit_pass/bandit27
```

</details>

<details>
<summary>Level 27:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```
```bash
mktemp -d
cd /tmp/tmp.KTCa6WPjLK
git clone ssh://bandit27-git@localhost:2220/home/bandit27-
git/repo
ls
cd repo/
cat README
```

</details>

<details>
<summary>Level 28:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit28
AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
```bash
mktemp -d
cd /tmp/tmp.KTCa6WPjLK
git clone ssh://bandit28-git@localhost:2220/home/bandit28-
git/repo
ls
cd repo/
cat README.md
git log
git show f08b9cc63fa1a4602fb065257633c2dae6e5651b
```

</details>

<details>
<summary>Level 29:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit29
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```
```bash
mktemp -d
cd /tmp/tmp.KTCa6WPjLK
git clone ssh://bandit29-git@localhost:2220/home/bandit29-
git/repo
ls
cd repo/
cat README.md
git branch -a
git switch dev
cat README.md
```

</details>

<details>
<summary>Level 30:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit30
xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
```bash
mktemp -d
cd /tmp/tmp.KTCa6WPjLK
git clone ssh://bandit30-git@localhost:2220/home/bandit30-
git/repo
ls
cd repo/
cat README.md
git checkout + TAB + TAB
git show secret
```

</details>

<details>
<summary>Level 31:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit31
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
```bash
mktemp -d
cd /tmp/tmp.KTCa6WPjLK
git clone ssh://bandit31-git@localhost:2220/home/bandit31-
git/repo
ls
cd repo/
cat README.md
cat .gitignore
rm -rf .gitignore
touch key.txt
vim 'May I come in?'
:wq!
git add .
git commit -m 'add key'
git push origin master
```

</details>

<details>
<summary>Level 32:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit32
rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```
```bash
$0
ls
/bin/bash
cat /etc/bandit_pass/bandit33
```

</details>

<details>
<summary>Level 33:</summary>

```
ssh bandit.labs.overthewire.org -p 2220 -l bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
```bash
cat README.txt
```

</details>