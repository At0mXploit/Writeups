# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4511]
╰─[:)] % nc saturn.picoctf.net 50923
Please md5 hash the text between quotes, excluding the quotes: 'chorus girls'
Answer: 
fdaf7298de6707185d68175ba4bd2f17
fdaf7298de6707185d68175ba4bd2f17
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'log cabins'
Answer: 
0cf9a466703d6f50227a4f85dfc63b58
0cf9a466703d6f50227a4f85dfc63b58
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'communists'
Answer: 
60dc96cdf23898725b1f6862e99b5109
60dc96cdf23898725b1f6862e99b5109
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4513]
╰─[:)] % 
```

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4497]
╰─[:)] % echo "Cindy Crawford" | md5sum
bbb6be951a4ad44417355ed98749cd3b  -
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4508]
╰─[:)] % echo "Muhammad Ali" | md5sum
7160ffee42774b308301c78d265b6827  -
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4510]
╰─[:)] % echo -n "commuting" | md5sum

d2c3874ec246fb1858841223ffe4992e  -
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4512]
╰─[:)] % echo -n "commuting" | md5sum

╭─[~/Hentai/CTF/pico]─[at0m@heker]─[130]─[4512]
╰─[:(] % echo -n "chorus girls" | md5sum

fdaf7298de6707185d68175ba4bd2f17  -
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4514]
╰─[:)] % echo -n "log cabins" | md5sum

0cf9a466703d6f50227a4f85dfc63b58  -
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4515]
╰─[:)] % echo -n "communists" | md5sum

60dc96cdf23898725b1f6862e99b5109  -
```

- `picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}`

---
