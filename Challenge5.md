# Challenge 5

Access via SSH | bandit.labs.overthewire.org port 2220 

## How I resolved it:

This challenge is so funny by far!. PLEASE try to make this challenge by yourself, is very cool to do it by your way, DON'T surrender you can do it!.

So we have multiple directories and files, and there are specific indications for the challenge.

- human-readable
- 1033 bytes in size
- not executable

We have to adapt all of this points in one command, that's why is very funny to resolve it. So here we go.

~~~bash
find . -type f -size 1033c -exec file {} \; 2>/dev/null | grep "ASCII text"
~~~

Don't forget to use `2>/dev/null` very important if we want to have the result, cause we're gonna have a lot of files we dont have permission.
