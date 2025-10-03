# Chaining Commands

## Scripting with Multiple Conditions
You've learned how to use a single if statement to check a condition. But what if you need to check multiple conditions? You can use elif (short for else if):

if [ "$1" == "one" ]
then
    echo "1"
elif [ "$1" == "two" ]
then
    echo "2"
elif [ "$1" == "three" ]
then
    echo "3"
else
    echo "unknown"
fi
Note that you do need a then after the elif, just like the if. As before the else at the end catches everything that didn't match.

For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "hack", output "the planet"
If the argument is "pwn", output "college"
If the argument is "learn", output "linux"
For any other input, output "unknown"
Example:

hacker@dojo:~$ bash /home/hacker/solve.sh hack
the planet
hacker@dojo:~$ bash /home/hacker/solve.sh pwn
college
hacker@dojo:~$ bash /home/hacker/solve.sh learn
linux
hacker@dojo:~$ bash /home/hacker/solve.sh foo
unknown
hacker@dojo:~$
Once your script works correctly, run /challenge/run to get your flag!

NOTE: As you're creating your script, make sure to follow the spacing closely in the examples. Unlike many other languages, bash requires the [ and the ] to be separated from other characters by spaces, otherwise it cannot parse the condition.

### Solve
**Flag:** `pwn.college{ofVeR7X0jCY5rl3A55yCoRWSchu.0FOzMDOxwSM4AzNzEzW}`

Wrote conditional statements using if,elif and else in the shell script as given in the challenge then checked it by running in the terminal and finally, used /challenge/run to get the flag.

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh hack the planet
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh foo
unknown
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{ofVeR7X0jCY5rl3A55yCoRWSchu.0FOzMDOxwSM4AzNzEzW}
```

### New Learnings
Learned to use multiple conditions using if,else and elif statements.

### References 
No references used.
