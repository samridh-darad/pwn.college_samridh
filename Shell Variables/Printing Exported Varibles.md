# Shell Variables

## Printing Exported Variables
There are multiple ways to access variables in bash. echo was just one of them, and we'll now learn at least one more in this challenge.

Try the env command: it'll print out every exported variable set in your shell, and you can look through that output to find the FLAG variable!

### Solve
**Flag:** `FLAG=pwn.college{0r305Kc5nWXX4HMXBJ4ltBqlxv5.QX4UTN0wSM4AzNzEzW}`

Used env command to print all exported variables in the shell then found the flag variable in the output.

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=9ed144a8a466d8b11777e58a2514848a39d51386991aaab428f6fc212546a577
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{0r305Kc5nWXX4HMXBJ4ltBqlxv5.QX4UTN0wSM4AzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

### New Learnings
Learned to use env command.

### References 
No references used.
