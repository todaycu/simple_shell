# Simple Shell
 Project consists in creating a basic command interpreter with C programming language.

 ## Table of Contents
* [Introduction](#Introduction)
  * What is Simple Shell
* [Project Consideration](#Project-Consideration)
    * General considerations
    * Allowed functions
* [Documentation](#Documentation)
    * Download
    * Compilation
    * Testing
    * Files
* [Authors](#Authors)

## Introduction

### What is Simple Shell
**Simple Shell** simulates **shell**, that is a command-line interpreter. It is the computer program that provides a user interface to access the services of the operating system.

In other words, simple_shell is a program that reads commands provided, check if exists and execute

**Interactive mode**

    test@ubuntu:~/simple_shell$ ./hsh
    $ ls
    file1 file2 file3 file4
    $ 

**Non-interactive mode**

    test@ubuntu:~/simple_shell$ echo "ls" | ./hsh
    file1 file2 file3 file4
    test@ubuntu:~/simple_shell$

## Project Consideration

### General considerations
 * The program is builted and run in `Ubuntu 20.04 LTS`
 * The program is compiled with `gcc` using the options `-Wall` `-Werror` `-Wextra` `-pedantic` `-std=gnu89`
 * The code is in format: Betty style. `betty *.c`
 * All the headers is in `shell.h`
 * The program don't have memory leaks in father process neither in each child process
 * Simple_Shell have the exact same output as `sh` (`/bin/sh`) as well as the exact same error output.


### Allowed functions that we use in SIMPLE_SHELL
* `access` (man 2 access)
* `chdir` (man 2 chdir)
* `close` (man 2 close)
* `closedir` (man 3 closedir)
* `execve` (man 2 execve)
* `exit` (man 3 exit)
* `_exit` (man 2 _exit)
* `fflush` (man 3 fflush)
* `fork` (man 2 fork)
* `free` (man 3 free)
* `getcwd` (man 3 getcwd)
* `getline` (man 3 getline)
* `isatty` (man 3 isatty)
* `kill` (man 2 kill)
* `malloc` (man 3 malloc)
* `open` (man 2 open)
* `opendir` (man 3 opendir)
* `perror`(man 3 perror)
* `read` (man 2 read)
* `readdir` (man 3 readdir)
* `signal` (man 2 signal)
* `stat` (__ xstat) (man 2 stat)
* `lstat` (__ lxstat) (man 2 lstat)
* `fstat` (__ fxstat) (man 2 fstat)
* `strtok` (man 3 strtok)
* `wait` (man 2 wait)
* `waitpid` (man 2 waitpid)
* `wait3` (man 2 wait3)
* `wait4` (man 2 wait4)
* `write` (man 2 write)

### Compilation
Your shell will be compiled this way:

`cd simple_shell`
`gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`

### Testing

simple_shell works like this in interactive mode:

```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

Also in non-interactive mode:

```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```


## Authors

- [Birhanu Gebisa](https://github.com/BirhanuGebisa/) | <birhanugebisa@gmail.com>
- [Amen Amen](https://github.com/Amena17/) | <amenbefekadu2009@gmail.com>
# simple_shell
