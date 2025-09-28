# Shell Variables

## Setting Variables
Naturally, as well as reading values stored in variables, you can write values to variables. This is done, as with many other languages, using =. To set variable VAR to value 1337, you would use:

hacker@dojo:~$ VAR=1337
Note that there are no spaces around the =! If you put spaces (e.g., VAR = 1337), the shell won't recognize a variable assignment and will, instead, try to run the VAR command (which does not exist).

Also note that this uses VAR and not $VAR: the $ is only prepended to access variables. In shell terms, this prepending of $ triggers what is called variable expansion, and is, surprisingly, the source of many potential vulnerabilities (if you're interested in that, check out the Art of the Shell dojo when you get comfortable with the command line!).

After setting variables, you can access them using the techniques you've learned previously, such as:

hacker@dojo:~$ echo $VAR
1337
To solve this level, you must set the PWN variable to the value COLLEGE. Be careful: both the names and values of variables are case-sensitive! PWN is not the same as pwn and COLLEGE is not the same as College.

### Solve
**Flag:** `pwn.college{AsBpOO6tsXG72LShClWcHAt9oHb.QX5UTN0wSM4AzNzEzW}`

Set variable 'PWN' as 'COLLEGE' and got the flag,

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{AsBpOO6tsXG72LShClWcHAt9oHb.QX5UTN0wSM4AzNzEzW}
```

### New Learnings
Learned how to assign values to variables.

### References 
No references used.
