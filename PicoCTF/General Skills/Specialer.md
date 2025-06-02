# Solution

- I decided to autocomplete the command by pressing `<tab>` button and it gave me list.

```bash
Specialer$ 
!          bash       cd         declare    else       false      hash       let        pwd        shift      times      unalias
./         bg         command    dirs       enable     fc         help       local      read       shopt      trap       unset
:          bind       compgen    disown     esac       fg         history    logout     readarray  source     true       until
[          break      complete   do         eval       fi         if         mapfile    readonly   suspend    type       wait
[[         builtin    compopt    done       exec       for        in         popd       return     test       typeset    while
]]         caller     continue   echo       exit       function   jobs       printf     select     then       ulimit     {
alias      case       coproc     elif       export     getopts    kill       pushd      set        time       umask      }
Specialer$ cd ../. 
Specialer$ pwd
/home
Specialer$ cd ../
Specialer$ pwd
/
Specialer$ cd home
Specialer$ pwd
/home
Specialer$ echo *
ctf-player
Specialer$ cd ctf-player/
Specialer$ echo *
abra ala sim
Specialer$ cd abra
Specialer$ echo *
cadabra.txt cadaniel.txt
Specialer$ echo $(<cadaniel.txt)
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ cd ../
Specialer$ pwd
/home/ctf-player
Specialer$ cd ala
Specialer$ echo *
kazam.txt mode.txt
Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}
Specialer$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```

- `picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_c42168d9}`

---
