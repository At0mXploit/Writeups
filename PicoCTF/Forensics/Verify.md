# Solution

With `cat checksum.txt` the SHA256 hash of the real thing could be seen. In the files directory, there are 301 files with 8 8-character randomized names all with different checksums and contents. Lastly, decrypt.sh is the script provided that could be used on the correct file to get the flag.

If one of the checksums of the files in the files directory matches the checksum provided by checksum.txt then that file used with the decrypt script will give the flag.

Contents of checksum.txt: `03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8`

The `sha256sum` command can be used on a file to get the checksum. To get the checksum of all the files in the directory the `sha256sum files/*` command could be used. When paired with grep command with the known SHA256 checksum that needs to be found the correct file is displayed.

Command: `sha256sum files/* | grep 03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8`

Output: `03b52eabed517324828b9e09cbbf8a7b0911f348f76cf989ba6d51acede6d5d8 files/00011a60`

Lastly, the decrypt script could be run, `./decrypt.sh files/00011a60`, which gives the flag.

- `picoCTF{trust_but_verify_e018b574}`

---



