Let's get into some plumbing now, not really but kinda. Let's try a command: 

```
ls -la /etc
```{{execute}}

You should see a very long list of items, it's a little hard to read actually. Instead of redirecting this output to a file, wouldn't it be nice if we could just see the output in another command like `less`? Well we can!

```
ls -la /etc | less
```{{execute}}

The pipe operator `|`, represented by a vertical bar, allows us to get the stdout of a command and make that the stdin to another process. In this case, we took the stdout of `ls -la /etc` and then "*piped*" it to the `less` command. The pipe redirection operator is extremely useful and we will continue to use it for all eternity. 

Well what if I wanted to write the output of my command to two different streams? That's possible with the `tee` command, so named because of the way it mimics the functionality of a "T-pipe" that real plumbers often use: 

```
ls | tee peanuts.txt
```{{execute}}

You should see the output of `ls` on your screen and if you open up the `peanuts.txt` file you should see the same information!

# Exercise

Try the following commands: 

* `ls | tee peanuts.txt banan.txt`{{execute}}

>>Q1: What key represents the pipe operator?<<
=== |
