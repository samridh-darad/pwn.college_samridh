# Comprehending Commands

## An Epic Filesystem Quest
With your knowledge of cd, ls, and cat, we're ready to play a little game!

We'll start it out in /. Normally:

hacker@dojo:~$ cd /
hacker@dojo:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  proc  run   srv  tmp  var
boot  dev        flag  lib   lib64  media   opt  root  sbin  sys  usr

That's a lot of contents! One day, you will be quite familiar with them, but already, you might recognize the flag file and the challenge directory.

In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

0.Your first clue is in /. Head on over there.
1.Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
2.cat that file to read the clue!
3.Depending on what the clue says, head on over to the next directory (or don't!).
4.Follow the clues to the flag!
Good luck!

### Solve
**Flag:** `pwn.college{YgGaW6obplFujxgB2AeGCNQRrsU.QX5IDO0wSM4AzNzEzW}`

Kept changing directories,lissting and reading files according to the clues until found the flag.

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
README  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin     challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat README
Congratulations, you found the clue!
The next clue is in: /usr/share/doc/python3-twisted-bin
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/doc/python3-twisted-bin
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-twisted-bin$ ls
GIST  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-twisted-bin$ cat GIST
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/need/per/cpu

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/python3-twisted-bin$ cd /opt/linux/linux-5.4/include/config/need/per/cpu
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/need/per/cpu$ ls -a
.  ..  .DOSSIER  embed  page
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/need/per/cpu$ cat .DOSSIER
Tubular find!
The next clue is in: /opt/linux/linux-5.4/arch/arm/mach-davinci/include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/need/per/cpu$ cd /opt/linux/linux-5.4/arch/arm/mach-davinci/include
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-davinci/include$ ls
DISPATCH  mach
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-davinci/include$ cat DISPATCH
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/bcrypt/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-davinci/include$ cd /usr/local/lib/python3.8/dist-packages/bcrypt/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/bcrypt/__pycache__$ ls -a
.  ..  .TEASER  __init__.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/bcrypt/__pycache__$ cat .TEASER
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/bcrypt/__pycache__$ cd /usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info$ ls
INFO  INSTALLER  LICENSE  METADATA  RECORD  WHEEL  top_level.txt
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info$ ls -a
.  ..  INFO  INSTALLER  LICENSE  METADATA  RECORD  WHEEL  top_level.txt
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info$ cat INFO
Lucky listing!
The next clue is in: /usr/share/locale/ug

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/importlib_resources-6.4.5.dist-info$ cd /usr/share/locale/ug
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/ug$ ls
LC_MESSAGES  POINTER
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/ug$ cat POINTER
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/Documentation/features/io

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/ug$ ls /opt/linux/linux-5.4/Documentation/features/io
HINT-TRAPPED  dma-contiguous
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/ug$ cat /opt/linux/linux-5.4/Documentation/features/io/HINT-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/SVG/fonts/TeX
hacker@commands~an-epic-filesystem-quest:/usr/share/locale/ug$ cd /usr/share/javascript/mathjax/jax/output/SVG/fonts/TeX
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/TeX$ ls
ALERT  Caligraphic  Main  SansSerif  Size1  Size3  Typewriter         fontdata.js
AMS    Fraktur      Math  Script     Size2  Size4  fontdata-extra.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/SVG/fonts/TeX$ cat ALERT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{YgGaW6obplFujxgB2AeGCNQRrsU.QX5IDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to use cd, ls and cat commands together on the command line.

### References 
No references used.
