# Practicing Piping

## Filtering with grep -v
The grep command has a very useful option: -v (invert match). While normal grep shows lines that MATCH a pattern, grep -v shows lines that do NOT match a pattern:

hacker@dojo:~$ cat data.txt
hello hackers!
hello world!
hacker@dojo:~$ cat data.txt | grep -v world
hello hackers!
hacker@dojo:~$
Sometimes, the only way to filter to just the data you want is to filter out the data you don't want. In this challenge, /challenge/run will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word DECOY somewhere in the flag) mixed in with the real flag. You'll need to filter out the decoys while keeping the real flag!

Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!

### Solve
**Flag:** `pwn.college{whmOtHT6jMpRPsLBqhM1VWguvYI.0FOxEzNxwSM4AzNzEzW}`

Piped the stdout of /challenge/run and filtered word DECOY by grep -v to get the real flag only.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{whmOtHT6jMpRPsLBqhM1VWguvYI.0FOxEzNxwSM4AzNzEzW}
```

### New Learnings
Learned how to filter content using grep -v.

### References 
No references used.
