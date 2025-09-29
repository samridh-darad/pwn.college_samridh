# Data Manipulation

## Extacting specific sections of the text
Sometimes, you want to grab specific columns of data, such as the first column, the third column, or the 42nd column. For this, there's the cut command.

For example, imagine that you have the following data file:

hacker@dojo:~$ cat scores.txt
hacker 78 99 67
root 92 43 89
hacker@dojo:~$
You could use cut to extract specific columns:

hacker@dojo:~$ cut -d " " -f 1 scores.txt
hacker
root
hacker@dojo:~$ cut -d " " -f 2 scores.txt
78
92
hacker@dojo:~$ cut -d " " -f 3 scores.txt
99
43
hacker@dojo:~$
The -d argument specifies the column delimiter (how columns are separated). In this case, it's a space character. Of course, it has to be in quotes here so that the shell knows that the space is an argument rather than a space separating other arguments! The -f argument specifies the field number (which column to extract).

In this challenge, the /challenge/run program will give you a bunch of lines with random numbers and single characters (characters of the flag) as columns. Use cut to extract the flag characters, then pipe them to tr -d "\n" (like the previous level!) to join them together into a single line. Your solution will look something like /challenge/run | cut ??? | tr ???, with the ??? filled out.

### Solve
**Flag:** `pwn.college{Qz0n-Nx5CpTf1PdBMivMXm5AJpO.01NxEzNxwSM4AzNzEzW}`

First identified the column in which flag elements are placed then used cut command to take out the command and then used tr -d to delete all the newine characters to get the flag.

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run
8739 p
18624 w
16358 n
9701 .
27787 c
19093 o
172 l
10894 l
28725 e
19040 g
29063 e
2634 {
7722 Q
58 z
6692 0
15414 n
2093 -
28430 N
8902 x
32709 5
26768 C
26645 p
27069 T
31010 f
24007 1
13453 P
8211 d
26228 B
31244 M
21598 i
3488 v
17467 M
6121 X
18967 m
14626 5
2001 A
21889 J
8511 p
13725 O
31524 .
6004 0
29884 1
5174 N
27827 x
2552 E
8931 z
7009 N
10587 x
14954 w
2181 S
22893 M
13904 4
22007 A
28788 z
22964 N
16190 z
1904 E
20984 z
3943 W
29530 }
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{Qz0n-Nx5CpTf1PdBMivMXm5AJpO.01NxEzNxwSM4AzNzEzW}
```

### New Learnings
Learned how to use cut command to extract columns.

### References 
No references used.
