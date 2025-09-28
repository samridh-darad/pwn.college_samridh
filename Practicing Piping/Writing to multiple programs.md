# Practicing Piping

## Writing to multiple progams
Add challenge description here

### Solve
**Flag:** `pwn.college{QtbSSBtptNogyb2PjV2fHUWqNDv.QXwgDN1wSM4AzNzEzW}`

/challenge/hack will produce some output which is duplicated using tee, then /challenge/the will feed its output to the duplicated output and /challenge/planet runs feeding it to the same duplicated output.

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) >( /challenge/planet )
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
320586547273824287
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{QtbSSBtptNogyb2PjV2fHUWqNDv.QXwgDN1wSM4AzNzEzW}
```

### New Learnings
Leanred how to use multiple process substituion.

### References 
NO references used.
