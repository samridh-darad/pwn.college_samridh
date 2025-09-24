# Comprehending Commands

## grepping for a needle in a haystack
Sometimes, the files that you might cat out are too big. Luckily, we have the grep command to search for the contents we need! We'll learn it in this challenge.

There are many ways to grep, and we'll learn one way here:

hacker@dojo:~$ grep SEARCH_STRING /path/to/file

Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!

### Solve
**Flag:** `pwn.college{0sVG1P3Fysw7cp11xaRa_pW1_2f.QX3EDO0wSM4AzNzEzW}`

Since the flag always starts with pwn.college so, I used grep command with pwn.college to find the flag.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{0sVG1P3Fysw7cp11xaRa_pW1_2f.QX3EDO0wSM4AzNzEzW}
```

### New Learnings
Learned how to use grep command to find the required data between a big set of data.

### References 
No references used.

