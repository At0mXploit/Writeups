# Solution

```bash
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt                          
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructions-to-2of3.txt               
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /root                                   
-bash: cd: /root: Permission denied
ctf-player@pico-chall$ cd /                                       
ctf-player@pico-chall$ ls                                         
2of3.flag.txt  etc			lib64	proc  srv  var
bin	      home			media	root  sys
boot	      instructions-to-3of3.txt  mnt	run   tmp
dev	      lib			opt	sbin  usr
ctf-player@pico-chall$ cat 2of3.flag.txt                          
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ cat instructions-to-3of3.txt               
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~                                       
ctf-player@pico-chall$ ls                                         
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt                          
1118a9a4}
ctf-player@pico-chall$ Connection to venus.picoctf.net closed by remote host.
```

- `picoCTF{xxsh_0ut_0f_\/\/4t3r_1118a9a4}`

---
