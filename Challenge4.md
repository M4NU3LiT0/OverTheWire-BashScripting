# Challenge 4

Access via SSH | bandit.labs.overthewire.org port 2220 

## How I resolved it:

Now, this is more funny than the last ones. 

There are multiple files called the same, but only one contains normal text. So the way we can resolve it is by using `find`. Of course, there are thousands of ways the challenge can be resolved. But this is how I made it.

~~~bash
find . -type f -exec file {} \; | grep "ASCII text"
~~~

This command is trying to find a file in that directory (`find .`). Then we indicate that our objective is a file (`-type f`) and then we want to execute `file`, a very important command to find out which type of file it is. We want to run `file` on every file, so we indicate it with `{} \;`.  
After that, we indicate we need only readable text, so that’s where `grep` comes in, indicating we want only `ASCII text`. And that’s it, easy peasy.
