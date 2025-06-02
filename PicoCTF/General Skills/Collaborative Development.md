# Solution

```bash
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4399]
╰─[:)] % ls
 .git   flag.py
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4400]
╰─[:)] % cat flag.py    
print("Printing the flag...")
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4401]
╰─[:)] % git init   
Reinitialized existing Git repository in /home/at0m/Hentai/CTF/pico/drop-in/.git/
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4402]
╰─[:)] % git log 
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4403]
╰─[:)] % git branch -a
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4404]
╰─[:)] % git checkout feature/part-1
Switched to branch 'feature/part-1'
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4405]
╰─[:)] % git log                    
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4406]
╰─[:)] % ls
 .git   flag.py
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4407]
╰─[:)] % cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')%                                ╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4408]
╰─[:)] % git checkout feature/part-2               

Switched to branch 'feature/part-2'
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4409]
╰─[:)] % git log                    
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4410]
╰─[:)] % cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')%                                 ╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4411]
╰─[:)] % git checkout feature/part-3
Switched to branch 'feature/part-3'
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4412]
╰─[:)] % cat flag.py
print("Printing the flag...")

print("w0rk_7ffa0077}")
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4413]
╰─[:)] % 
```

- `git branch -a` will let you see available branches

- `picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}`

---
