# wired CTF

# Beginner challenges
## sanity check-1

 filled the form and got the flag.

## sanity check 

 filled the form and got the flag.

## IRC

 1.Downloaded mIRC app from chrome and installed it.
 2. Opened it and put the server to Libera chat.
 3. typed my username and put Bi0s hardware in channel's place.
 4.Joined it and got the flag.

## Ceasercipher

 1.Searched in google about cipher and ceaser cipher.
 2. got a decoder from online and decoded it and got the flag.

## sanity check2

  Joined discord server and found the flag.

# Easy challenges

## Dots and Dashes

 1.Downloaded the audio .
 2.Played it. Searched on google about how to decode an audio.
 3. Learned about morse code. Found an online decoder to decode morse code and uploaded the audio and clicked decode.
 4. Got the flag.
 ### WHAT I LEARNED :
 Learned about morse code. Learned that it is in dots and dashes,  short beep is called a dot and a long one is a dash.
 
 ## chan's favourite
 1.Downloaded the audio and opened it on audacity.
  2.Tried using different options and finally changed into spectrogram.
  3.The audio waves changed into a picture of Rick astley.
  4.Got the flag.
  
  ## WHAT I LEARNED
  Learned about audacity and spectrogram , which is a visual representation of the audio.

## ~logic
1.Downlaoded the file and opened it. It was logic gates.
2. It was specified output was 1 . So i started from the out like in reverse order and found A,B,C,D.
3.Opened the link and input the values.
4.Got the flag.
  
  ## find_thyself      
  1.Downloaded the image. It was a socket.
  2. Understood that we should identify the country that uses that type of socket.
  3. Opened google lens and scanned the image.
  4. Result showed Italy which was the flag.
  
  ## grep it
  1.Downloaded the file and opened linux command.
  2.Searched on google how to open a file and see contents in linux.
  3. Searched about grep command and learned about it.
  4. In linux command :
  ```
  strings chall | grep wired
  ```
  5 . Found the flag.
   
   ## WHAT I LEARNED
   Learned about strings to view contents of a file, learned about grep to search and match a word in that file, pipe ( | ) to use 2 commands in one line.

### D0Z3N_IS_K3Y
1 . Downloaded the file and opened  Linux command.
2. Tried grep command. First used grep wired but nothing came.
3. Tried grep flag and got flag with an encrypted text.
4. Used an online decoder to decrypt it.
5. Got the flag.
```
strings corrected_one | grep flag
```
## Lifetimesettlement

1 . Copied the text and searched how to identify  a cipher text.
2 . Used an online cipher identifier to identify the text and decoded.
3 . Got the flag.

## da_french_cipher
1 . Searched on google about french cipher.
2. It showed about vignere cipher. 
3. I copied the encrypted code and opened an online decoder.
4. Put the cipher text option to vignere cipher and inserted a,e,i,o,u  as key and then decoded it.
5. Got the flag.

##  da_0n3_wh3r3_u_v1su4l1s3
1 . I downloaded the file and then saw it was a corrupted file.
2. Searched on google how a file becomes corrupted, Got to know about file headers.
3. Searched how to change file headers on google and found and used an online hex editor to change the file header.
4. Searched what is the file header format of a txt file and edited it.
5. Then opened it and found the flag.

## WHAT I LEARNED
Learned about how a file gets corrupted and learned about file headers and how to edit file headers.

## HARD CHALLENGES

## xoring

1 . Downloaded the python file and googled about xor function and learned about it.
2. I learned that 
```
x ^ 0 = x
x ^ y = z
x ^ z = y
y ^ z = x 
```
 2 .  I learned that the first 5 letters were \x00 = 0
3.  I tried to xor it with "wired" and got wired as the result.
4.  As the flag is in the format wired{flag} so used 'wired{' for xoring got wiredw as the result in back.
5.  So i guessed that it was wired being repeated.
6.  Used "wiredwiredwiredwired" for xoring.
7.  Got the flag as the result. 
## WHAT I LEARNEDD
I learned about xor function and about ord and chr function in python. They are used to convert a character to an int and vice versa.

## Medium challenges
1 . First i downloaded the file and googled about .cap files.
2. Tried to open it with some websites but didnt work.
3. Found about wireshark and found how analyse it but got stuck in between so i abandoned wireshark.
4. Used hashcat . First i installed it with sudo command had a good going but again got stuck.
5. Then after researching i learned about aircrack tool and learned about wordlists attacks with rockyou.txt .
6. Downloaded rockyou.txt .
7. Used the command :
 ```
 aircrack-ng dump_c8d020f8-aa4b-43ec-b761-b9fee3f328fb.cap-01.pcap -w /usr/share/wordlists/Hob0Rules/wordlists/rockyou.txt 
 ```
 
8 .  Got  a list of packets and selected the super secret wifi one and it started scanning for the password and got the password which was the flag.
