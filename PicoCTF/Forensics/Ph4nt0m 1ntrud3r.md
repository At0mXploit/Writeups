# Solution

```bash
╰─[:)] % strings myNetworkTraffic.pcap
ezF0X3c0cw==O
I+znCJg=O
/9QZRtc=O
uF+2UTs=O
pDW7rkI=O
8esVOK4=O
cGljb0NURg==O
KWEh2jQ=O
BGAVCe8=O
RA+7xFw=O
YmhfNHJfZA==O
CMEx344=O
PGb6oYA=O
uSy5rvo=O
bnRfdGg0dA==O
MTA2NTM4NA==O
xIJPbWg=O
XzM0c3lfdA==O
oDis5T8=O
v2XglLs=O
fQ==O
STneebY=
```

- Base64 decode it (only with `==` is base64)

```bash
╰─[:)] % echo "ezF0X3c0cw==" | base64 -d 
{1t_w4s%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7116]
╰─[:)] % echo "cGljb0NURg==" | base64 -d
picoCTF%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7117]
╰─[:)] % echo "YmhfNHJfZA==" | base64 -d
bh_4r_d%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7118]
╰─[:)] % echo "bnRfdGg0dA==" | base64 -d
nt_th4t%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7119]
╰─[:)] % echo "MTA2NTM4NA==" | base64 -d
1065384%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7120]
╰─[:)] % echo "XzM0c3lfdA==" | base64 -d
_34sy_t%                                                           (venv) ╭─[~/Hentai/Heking/pico]─[at0m@heker]─[0]─[7121]
╰─[:)] % echo "fQ==" | base64 -d 
}%          
```

- Or just use this regex

```bash
╰─[:)] % tshark -r myNetworkTraffic.pcap -Y "tcp.len==12 || tcp.len==4" -T fields -e frame.time -e tcp.segment_data | sort -k4 | awk '{print $6}' | xxd -p -r | base64 -d
```

- `picoCTF{1t_w4snt_th4t_34sy_tbh_4r_d1065384}`

---
