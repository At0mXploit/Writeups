# Solution

- View Source

```js
|   |
|---|
|<script type="text/javascript" src="[md5.js](http://jupiter.challenges.picoctf.org:29835/md5.js)"></script>|
|||
||<script type="text/javascript">|
||function verify() {|
||checkpass = document.getElementById("pass").value;|
||split = 4;|
||if (checkpass.substring(0, split) == 'pico') {|
||if (checkpass.substring(split*6, split*7) == '723c') {|
||if (checkpass.substring(split, split*2) == 'CTF{') {|
||if (checkpass.substring(split*4, split*5) == 'ts_p') {|
||if (checkpass.substring(split*3, split*4) == 'lien') {|
||if (checkpass.substring(split*5, split*6) == 'lz_7') {|
||if (checkpass.substring(split*2, split*3) == 'no_c') {|
||if (checkpass.substring(split*7, split*8) == 'e}') {|
||alert("Password Verified")|
||}|
||}|
||}|
|||
||}|
||}|
||}|
||}|
||}|
||else {|
||alert("Incorrect password");|
||}|
|||
||}|
||</script>|
```

- It sets `split = 4`, meaning the password is broken into 4-character chunks.
- It then checks if the password contains the expected values in specific positions.
- First 4 characters: **"pico"**
- Characters 4–7: **"CTF{"**
- Characters 8–11: **"no_c"**
- Characters 12–15: **"lien"**
- Characters 16–19: **"ts_p"**
- Characters 20–23: **"lz_7"**
- Characters 24–27: **"723c"**
- Characters 28–31: **"e}"**

- `picoCTF{no_clients_plz_7723c}`

---