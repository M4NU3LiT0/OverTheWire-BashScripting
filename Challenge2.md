# Challenge 2

Access via SSH | bandit.labs.overthewire.org port 2220 

## How I resolved it:

This challenge is very similar to the previous one. We just have to do the same as before, using `cat` on the directory.

~~~bash
bandit2@bandit:~$ cat /home/bandit2/--spaces\ in\ this\ filename--
~~~

This is because the `cat` command cannot interpret spaces directly, so we have to handle it the same way as with the `-` filename.
