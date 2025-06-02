# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4530]
╰─[:)] % python3 fixme1.py
  File "/home/at0m/Hentai/CTF/pico/fixme1.py", line 20
    print('That is correct! Heres your flag: ' + flag)
IndentationError: unexpected indent
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[1]─[4531]
╰─[:(] % nvim fixme1.py   
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4532]
╰─[:)] % python3 fixme1.py
That is correct! Heres your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4533]
╰─[:)] % cat fixme1.py

import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x06) + chr(0x1c) + chr(0x5a) + chr(0x5c) + chr(0x55) + chr(0x40) + chr(0x3a) + chr(0x5f) + chr(0x53) + chr(0x5b) + chr(0x57) + chr(0x41) + chr(0x57) + chr(0x08) + chr(0x5c) + chr(0x14)

  
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Heres your flag: ' + flag)

╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4534]
╰─[:)] % 
```

- `picoCTF{1nd3nt1ty_cr1515_182342f7}`

---
