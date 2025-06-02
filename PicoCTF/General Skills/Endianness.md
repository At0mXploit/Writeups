# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[4348]
╰─[:)] % nc titan.picoctf.net 63742
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: yxkgx
Enter the Little Endian representation: 78676B7879
Correct Little Endian representation!
Enter the Big Endian representation: 
79786B6778                                          
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_d58517b6}
```

### Understanding Endianness

Endianness refers to how bytes are ordered in memory. The two common types are:

- **Little Endian:** The least significant byte (LSB) comes first.
- **Big Endian:** The most significant byte (MSB) comes first.

### Converting "yxkgx"

Since each character in a string can be represented by its ASCII value, let's break it down:

1. Convert each character to its hexadecimal ASCII value:

    `'y' -> 79   'x' -> 78   'k' -> 6B   'g' -> 67   'x' -> 78`  
    
2. Construct the **Big Endian** representation (natural order):

	`79 78 6B 67 78`
    
3. Construct the **Little Endian** representation (reverse order):
    
    `78 67 6B 78 79`

- `picoCTF{3ndi4n_sw4p_su33ess_d58517b6}`