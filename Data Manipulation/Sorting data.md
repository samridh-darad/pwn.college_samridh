# Data Manipulation

## Sorting data
Files (or output lines of commands) aren't always in the order you need them! The sort command helps you organize data. It reads lines from input (or files) and outputs them in sorted order:

hacker@dojo:~$ cat names.txt
  hack
  the
  planet
  with
  pwn
  college
hacker@dojo:~$ sort names.txt
  college
  hack
  planet
  pwn
  the
  with
hacker@dojo:~$
By default, sort orders lines alphabetically. Arguments can change this:

-r: reverse order (Z to A)
-n: numeric sort (for numbers)
-u: unique lines only (remove duplicates)
-R: random order!
In this challenge, there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end (we made sure of this when generating fake flags). Go get it!

### Solve
**Flag:** `pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwSM4AzNzEzW}`

Sorted content of file in alphabetical reverse order to get the flag at the top.

```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r
pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwSM4AzNzEzW}
pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwSM4AzNzEzW}
pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwSM4AzNzEyW}
pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwSL4AzNyEzW}
pwn.college{wCVYkvXU7ql6efrgDpEPMiXlPxk.0FM0MDOxwRM4AzNzEzW}
.
.
.
.
```

### New Learnings
Learned about sort command and it's various functions with different arguments.

### References 
No references used.
