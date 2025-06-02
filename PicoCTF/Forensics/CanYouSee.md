# Solution

```bash
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[5196]
╰─[:)] % steghide extract -sf ukn.jpg       
Enter passphrase: 
steghide: could not extract any data with that passphrase!
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[1]─[5197]
╰─[:(] % exiftool ukn.jpg                                                         
ExifTool Version Number         : 13.21
File Name                       : ukn.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:12 05:50:53+05:45
File Access Date/Time           : 2025:03:13 22:49:24+05:45
File Inode Change Date/Time     : 2025:03:13 22:49:24+05:45
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
╭─[~/Hentai/CTF/pico]─[at0m@heker]─[0]─[5198]
╰─[:)] % echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==" | base64 --decode                                                
picoCTF{ME74D47A_HIDD3N_b32040b8}
```

- `picoCTF{ME74D47A_HIDD3N_b32040b8}`

---

