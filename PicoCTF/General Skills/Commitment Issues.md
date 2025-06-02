# Solution

```bash
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4372]
╰─[:)] % git init                                             
Reinitialized existing Git repository in /home/at0m/Hentai/CTF/pico/drop-in/.git/
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4373]
╰─[:)] % git log          
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4374]
╰─[:)] % git checkout 7d3aa557ff7ba7d116badaf5307761efb3622249
Note: switching to '7d3aa557ff7ba7d116badaf5307761efb3622249'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 7d3aa55 create flag
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4375]
╰─[:)] % ls
 .git   message.txt
╭─[~/Hentai/CTF/pico/drop-in]─[at0m@heker]─[0]─[4376]
╰─[:)] % cat message.txt
picoCTF{s@n1t1z3_be3dd3da}
```

- `git checkout <branch-name>` is used to restore, recover commited files.

- `picoCTF{s@n1t1z3_be3dd3da}`

---
