# Challenge 3

Access via SSH | bandit.labs.overthewire.org port 2220 

## How I resolved it:

When we log in, we can see an `inhere` directory. Once we move into that directory, it seems like there are no files. There is a peculiar command that can help us find hidden files.

~~~bash
cd inhere
ls -a
cat ...Hiding-from-you
~~~

The command `ls -a` does not ignore any entries starting with `.`. It is commonly used for configuration files that are normally hidden. That’s how I understand it.
