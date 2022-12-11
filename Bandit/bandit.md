# BANDIT
## level 0
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
## level 0 -1
```
ls
cat
```
#### pass: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```
ssh bandit1@bandit0labs.overthewire.org -p 2220
```
## level 1-2 
```
ls
cat ./-
```
###### used ./- for opening dashed file
```
ssh bandit2@bandit.labs.overthewire.org -p 2220
```
#### pass: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi 

## level 2-3
```
ls
cat "spaces in this filename"
```
###### used " " to read file with spaces
```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
#### pass: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

## level 3-4
```
ls
cd inhere
ls -a
cat .hidden
```
###### learned to use ls -a to open hidden files
```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```
#### pass: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## level 4-5
```
ls
cd inhere
file *
file ./*
cat ./-file07
```
###### learned to use file command to determine the type of file
```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```
#### pass: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## level 5-6
```
ls 
cd inhere
ls
find. -size 1033c ! -executable 
cat./inhere/maybehere07/.file2
exit
```
###### learned how to find a file from a directory with  size and type of file specified
```
ssh bandit6@bandit.labs.overthewire.org -p 2220
```
#### pass: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## level 6-7
```
ls
ls -a
find ./ -group bandit6 -user bandit7 -size 33c
cat ./var/lib/dpkg/info/bandit7.password
```
###### learned to find file from by specifying group and user
#### pass: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## level 7-8
```
ls 
strings data.txt | grep millionth
```
###### learned to use strings and grep command
```
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
#### pass: TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## level 8-9
```
ls
sort data.txt | uniq -u
```
###### learned to use sort command and also to sort line that occurs only once
```
ssh bandit9@bandit.labs.overthewire.org -p 2220
```
#### pass: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## level 9-10
```
ls
strings data.txt | grep "="
```
```
ssh bandit10@bandit.labs.overthewire.org -p 2220
```
#### pass: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## level 10-11
```
ls
cat data.txt
base64 -d data.txt
```
###### learned to decode -d command to decode/decompress
```
ssh bandit11@bandit.labs.overthewire.org -p 2220
```
#### pass: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## level 11-12
```
ls
cat data.txt
```
### later
used https://cryptii.com/pipes/caesar-cipher-decoder to convert the text in data.txt from ROT13 to plaintext
#### pass: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## level 12-13
```
ls
cat data.txt
mkdir /tmp/newfile666
cp data.txt /tmp/newfile666
cd /tmp/newfile666
xxd -r data.txt data
file data
mv data data.gz
gzip -d data.gz
file data
mv data data.bz2
bzip2 -d data.bz2
file data
mv data data.gz
gzip -d data.gz
file data
tar -x -f data
file data5.bin
tar -x -f data5.bin
file data6.bin
bzip2 -d data6.bin
file data6.bin.out
tar -x -f data6.bin.out
file data8.bin
mv data8.bin data8.gz
gzip -d data8.gz
file data8
cat data8
```
###### learned to create a tmp file , learned to use xxd command to convert hexdump file back to original binary form, learned to move and rename a file and folder , learned to decompress all types of file
```
ssh bandit13@bandit.labs.overthewire.org -p 2220
```
#### pass: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw


## level 13-14
```
ls
ssh bandit14@localhost -i sshkey.private -p 2220
```
###### learned to log into server with a private key  

### later 
```
cat /etc/bandit_pass/bandit14
```
#### pass: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
  
  ## level 14-15
```
nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
###### learned to to use netcat (nc) to connect to server on different port . nc helps in reading and writing data between 2 different computer networks
  ```
  ssh bandit15@bandit.labs.overthewire.org -p 2220
  ```
  #### pass: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## level 15-16
```
openssl s_client -connect localhost:30001
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
###### learned s_client  command to connect to local ssl server with port specified.
#### pass: JQttfApK4SeyHwDlI9SXGR50qclOAil1

## level 16-17

```
nmap localhost -p 31000-32000
nc localhost 31790
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```
### tried all ports and got a key from p 31790
```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----
```
### then made a tmp directory and saved it in a folder in it
```
cd /tmp
chmod 700 bandit17pvt.key
ssh -i bandit17pvt.key bandit17@localhost -p 2220
cd/etc/bandit_pass/bandit17
```
###### learned to use nmap to scan the ports from 31000 - 32000, learned to use chmod and change the permission of a file .

#### pass: VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## level 17 -18
```
diff passwords.new passwords.old
```
###### learned to use diff command which helps to compare 2 files
  
  ```
  ssh bandit18@bandit.labs.overthewire.org -p 2220
  ```
  
  #### pass: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
  
  ## level 18-19
  
  ###### logged me out by saying Byebye
  ```
 ssh bandit19@bandit.labs.overthewire.org -p 2220 cat readme
 hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
 ```
 #### pass: awhqfNnAbc1naukrpqDYcF95h7HoMTrC
 
 ###### tried to use cat with the usual login command then entered the password of previous level . it worked , got the password .
 
 ## level 19-20
 ```
  ./bandit20-do
./bandit20-do id
./bandit20-do cat /etc/bandit_pass/bandit20
 ```  
  ###### i understood that when i used  ' ./bandit20-do 'to setuid binary  i became the bandit 20 user and it showed the id when i put id in the next line. then i added 'cat /etc/bandit_pass/bandit20' to read the password of bandit 20 and it worked.
  #### pass: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
  





