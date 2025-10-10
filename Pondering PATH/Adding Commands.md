# Pondering PATH

## Adding Commands
Recall our example from the previous level:

hacker@dojo:~$ ls /home/hacker/scripts
goodscript	badscript	okayscript
hacker@dojo:~$ PATH=/home/hacker/scripts
hacker@dojo:~$ goodscript
YEAH! This is the best script!
hacker@dojo:~$
What we see here, of course, is the hacker making the shell more useful for themselves by bringing their own commands to the party. Over time, you might amass your own elegant tools. Let's start with win!

Previously, the win command that /challenge/run executed was stored in /challenge/more_commands. This time, win does not exist! Recall the final level of Chaining Commands, and make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!

Hint: /challenge/run runs as root and will call win. Thus, win can simply cat the flag file. Again, the win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory. But remember, if you do that, your win command won't be able to find cat.

You have three options to avoid that:

1.Figure out where the cat program is on the filesystem. It must be in a directory that lives in the PATH variable, so you can print the variable out (refer to Shell Variables to remember how!), and go through the directories in it (recall that the different entries are separated by :), find which one has cat in it, and invoke cat by its absolute path.
2.Set a PATH that has the old directories plus a new entry for wherever you create win.
3.Use read (again, refer to Shell Variables) to read /flag. Since read is a builtin functionality of bash, it is unaffected by PATH shenanigans.
Now, go and win!

### Solve
**Flag:** `pwn.college{wowQOybJtw0hjcW7gqRK6OVcnDa.QX2cjM1wSM4AzNzEzW}`

Made one directory in which made one file win and concatenated that file with the command to read flag by directly mentioning it's path in /bin. Here EOF is end of file which helps us input the code in the script till end of file is reached. Then made the win file executable, changed the path and ran /challenge/run which gave the flag.

```bash
samridh@LAPTOP-JB8B34BR:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@path~adding-commands:~$ mkdir ./script
hacker@path~adding-commands:~$ cat > ~/script/win << 'EOF'
> #!/bin/bash
> /bin/cat /flag
> EOF
hacker@path~adding-commands:~$ chmod a+x /script/win
chmod: cannot access '/script/win': No such file or directory
hacker@path~adding-commands:~$ chmod a+x ~/script/win
hacker@path~adding-commands:~$ PATH=~/script
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{wowQOybJtw0hjcW7gqRK6OVcnDa.QX2cjM1wSM4AzNzEzW}
```

### New Learnings
Learned to use commands even after changing the PATH by manipulation.

### References 
Help from a friend.
