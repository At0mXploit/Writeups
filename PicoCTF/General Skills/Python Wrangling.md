
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?
# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[130]─[4588]
╰─[:(] % cat pw.txt     
67c6cc9667c6cc9667c6cc9667c6cc96
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4589]
╰─[:)] % python3 ende.py -d flag.txt.en
Please enter the password:67c6cc9667c6cc9667c6cc9667c6cc96
picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4590]
╰─[:)] % 
```

- `picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}`

---
