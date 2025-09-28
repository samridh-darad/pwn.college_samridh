# Shell Variables

## Multi-words Variables
In this level, you will learn about quoting. Spaces have special significance in the shell, and there are places where you can't use them spuriously. Recall our variable setting:

hacker@dojo:~$ VAR=1337
That sets the VAR variable to 1337, but what if you wanted to set it to 1337 SAUCE? You might try the following:

hacker@dojo:~$ VAR=1337 SAUCE
This looks reasonable, but it does not work, for similar reasons to needing to have no spaces around the =. When the shell sees a space, it ends the variable assignment and interprets the next word (SAUCE in this case) as a command. To set VAR to 1337 SAUCE, you need to quote it:

hacker@dojo:~$ VAR="1337 SAUCE"
Here, the shell reads 1337 SAUCE as a single token, and happily sets that value to VAR. In this level, you'll need to set the variable PWN to COLLEGE YEAH. Good luck!

### Solve
**Flag:** `pwn.college{E5J7R6bxkOci5RGJTuMAvXUfMNE.QXwYTN0wSM4AzNzEzW}`

Quoted "COLLEGE YEAH" so it will be taken as a single token to set it as variable foor 'PWN'

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{E5J7R6bxkOci5RGJTuMAvXUfMNE.QXwYTN0wSM4AzNzEzW}
```

### New Learnings
Leanred how we can make variables to contain multiple words using quotes.

### References 
No references used.
