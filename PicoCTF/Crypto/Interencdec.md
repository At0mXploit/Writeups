# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[5181]
╰─[:)] % cat enc_flag        
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[5182]
╰─[:)] % echo "YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==" | base64 --decode
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ=='
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[5183]
╰─[:)] % echo "d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ==" | base64 --decode
wpjvJAM{jhlzhy_k3jy9wa3k_78250hmj}%               
```

- Its in Caeser Cipher, ya can just decode it from [Here](https://www.dcode.fr/caesar-cipher)

- `picoCTF{caesar_d3cr9pt3d_78250afc}`

---
