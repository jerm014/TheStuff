# Project 2210: C - Shell v2
----



*For this project, we expect you to look at these concepts:*

* [Everything you need to know to start coding your own shell](/concepts/900)
* [[EYNTK] - Shell v2](/concepts/919)

![1](2210_1.jpg)

## Resources

**Read or watch**:

* [Unix shell](https://en.wikipedia.org/wiki/Unix_shell)
* [Thompson shell](https://en.wikipedia.org/wiki/Thompson_shell)
* [Ken Thompson](https://en.wikipedia.org/wiki/Ken_Thompson)
* [Interactive shells](https://tldp.org/LDP/abs/html/intandnonint.html)
* [Differences between lexers and parsers](https://stackoverflow.com/questions/2842809/lexers-vs-parsers/3614928#3614928)

**man or help**:

* `sh`
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* Who designed and implemented the original Unix operating system
* Who wrote the first version of the UNIX shell
* Who invented the B programming language (the direct predecessor to the C programming language)
* Who is Ken Thompson
* How does a shell work
* What are a pid and a ppid
* How to manipulate the environment of the current process
* What is the difference between a function and a system call
* How to create processes
* What are the three prototypes of`main`
* How does the shell use the`PATH`to find the programs
* How to execute another program with the`execve`system call
* How to suspend the execution of a process until one of its children terminates
* What is`EOF`/ “end-of-file”?
* How to redirect the content of a file into another file
* What is a pipeline
* How to setup a pipe
* How to setup a pipe between two processes
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be compiled on Ubuntu 20.04 LTS
* Your C programs and functions will be compiled with`gcc 9.4.0`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* A`AUTHORS.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`Betty`style. It will be checked using[betty-style.pl](https://github.com/hs-hq/Betty/blob/master/betty-style.pl)and[betty-doc.pl](https://github.com/hs-hq/Betty/blob/master/betty-doc.pl)
* No more than 5 functions per file
* All your header files should be include guarded
* There shouldn’t be any error nor memory leak upon execution of your shell
### Allowed Functions and System Calls

* `access`
* `chdir`
* `close`
* `execve`
* `fork`
* `stat`(__xstat)
* `lstat`(__lxstat)
* `fstat`(__fxstat)
* `kill`
* `open`
* `read`
* `signal`
* `wait`
* `waitpid`
* `wait3`
* `wait4`
* `write`
* `_exit`
* `dup`
* `dup2`
* `pipe`
* `unlink`
* `time`
* `gethostname`
* `geteuid`
* `sigaction`
* `sigemptyset`
* `select`
* `getpid`
* `__errno_location`(errno macros)
* `closedir`
* `exit`
* `free`
* `getcwd`
* `getline`
* `malloc`
* `opendir`
* `perror`
* `readdir`
* `strtok`
* `localtime`
* `getpwuid`
* `isatty`
* `printf`
* `fflush`
* `fprintf`
* `vfprintf`
* `sprintf`
### Compilation

* You have to provide a`Makefile`in order to compile your program
* Your`Makefile`must define the`all`rule: The`all`rule should compile and link the source code to generate the executable`hsh`
* Make sure your program compiles on`Ubuntu 14.04 LTS`, with`gcc 4.8.4`
* You must compile using the flags`-Wall``-Werror``-Wextra`and`-pedantic`
* Your executable must be named:`hsh`
## More Info

### Output

* Your shell will be auto-reviewed in[non-interactive](https://tldp.org/LDP/abs/html/intandnonint.html)mode (commands will be piped to it). Thereby, the prompt you print in interactive mode will not be taken into account, so you are free to have the prompt of your choice.
* Unless specified otherwise, your program**must have the exact same output**as`sh`(`/bin/sh`) as well as the exact same error output.
* The only difference is when you print an error, the name of the program must be equivalent to your`argv[0]`(See below)

Example of error with`sh`:

`
```
$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
```

Same error with your program`hsh`:

`
```
$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found
$
```
### Testing

Your shell should work like this in interactive mode:

`
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

But also in non-interactive mode:

`
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
### Checks

We**strongly**encourage the entire class to work together to create a suite of checks covering both regular tests and edged cases for each task

**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" > /tmp/output
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #1

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" > /tmp/output
cat /tmp/output
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #2

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" > /tmp/output
cat /tmp/output >&2
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #3

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" > /tmp/output 2>&1
cat /tmp/output
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #4

What will be the behavior of the following script?

`
```
#!/bin/sh
cat /holberton 2>&1 > /dev/null
```

 * `stderr`is redirect on`stdout`

 * `stdout`is redirect on`/dev/null`

 * `cat`error will be redirected to`stdout`

 * `cat`error will be redirected to`/dev/null`

#### Tips:

`/holberton`does not exist

#### Question #5

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" >> /tmp/output
echo -n " School" >> /tmp/output
cat /tmp/output
```

 * `Holberton`on`stdout`

 * `School`on`stdout`

 * `Holberton School`on`stdout`

 * Nothing

#### Question #6

What will the following script output upon execution?

`
```
#!/bin/sh
rm -f /tmp/output
echo -n "Holberton" >> /tmp/output
echo -n " School" > /tmp/output
cat /tmp/output
```

 * `Holberton`on`stdout`

 * `School`on`stdout`

 * `Holberton School`on`stdout`

 * Nothing

#### Question #7

What will the following script output upon execution?

`
```
#!/bin/sh
echo -n "Holberton" > /tmp/output
cat < /tmp/output
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #8

What will the following script output upon execution?

`
```
#!/bin/sh
cat << HOLBERTON
echo -n "Holberton"
HOLBERTON
```

 * `Holberton`on`stdout`

 * `echo -n "Holberton"`on`stdout`

 * `echo -n "Holberton"`and`HOLBERTON`(on 2 separated lines) on`stdout`

 * Nothing

#### Question #9

What will the following script output upon execution?

`
```
#!/bin/sh
bash << HOLBERTON
echo -n "Holberton"
HOLBERTON
```

 * `Holberton`on`stdout`

 * `echo -n "Holberton"`on`stdout`

 * `echo -n "Holberton"`and`HOLBERTON`(on 2 separated lines) on`stdout`

 * Nothing

#### Question #10

What will the following script output upon execution?

`
```
#!/bin/sh
echo -n "Holberton" | rev
```

 * `Holberton`on`stdout`

 * `notrebloH`on`stdout`

 * Nothing

#### Question #11

What will the following script output upon execution?

`
```
#!/bin/sh
echo -n "Holberton" > /dev/null | rev
```

 * `Holberton`on`stdout`

 * `notrebloH`on`stdout`

 * Nothing

#### Question #12

What will the following script output upon execution?

`
```
#!/bin/sh
[ 1 -eq 2 ] && echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #13

What will the following script output upon execution?

`
```
#!/bin/sh
[ 1 -eq 2 ] && [ 1 -ne 1 ] && echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #14

What will the following script output upon execution?

`
```
#!/bin/sh
[ 1 -eq 0 ] && [ 1 -eq 1 ] && echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #15

What will the following script output upon execution?

`
```
#!/bin/sh
[ 4 -ne 2 ] || echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #16

What will the following script output upon execution?

`
```
#!/bin/sh
[ 1 -ne 0 ] || [ 1 -eq 1 ] || echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #17

What will the following script output upon execution?

`
```
#!/bin/sh
[ 4 -ne 4 ] || [ 0 -eq 0 ] || echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #18

What will the following script output upon execution?

`
```
#!/bin/sh
[ 5 -ne 1 ] || [ 1 -eq 5 ] && echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #19

What will the following script output upon execution?

`
```
#!/bin/sh
[ 2 -eq 2 ] && [ 1 -eq 2 ] || echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #20

What will the following script output upon execution?

`
```
#!/bin/sh
[ 1 -ne 1 ] && [ 1 -eq 2 ] || [ 0 -ne 2 ] && [ 4 -eq 4 ] && echo -n "Holberton"
```

 * `Holberton`on`stdout`

 * Nothing

#### Question #21

What will the following C program output upon execution?

`
```
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

int main(void)
{
    if (dup2(STDERR_FILENO, STDOUT_FILENO) == -1)
    {
        perror("dup2");
        return (EXIT_FAILURE);
    }
    printf("Holberton");
    return (EXIT_SUCCESS);
}
```

 * `Holberton`on`stdout`

 * `Holberton`on`stderr`

 * `Holberton`on both`stdout`and`stderr`

 * Nothing

#### Question #22

What system call(s) is/are needed to create a pipe?

 * `dup`and/or`dup2`

 * `pipefd`

 * `pipe`

 * `open`

#### Question #23

What system call(s) is/are needed to create a pipe between two processes?

 * `dup`and/or`dup2`

 * `pipefd`

 * `pipe`

 * `open`

#### Question #24

What is the index of the write end of a pipe?

 * 0

 * 1

 * 2

#### Question #25

In order to create a pipe between two processes, we need to create the pipe:

 * In each process

 * Before creating the two processes

 * In the process that reads from the pipe

 * In the process that writes into the pipe


----
## Tasks
---
### 0. README, man, AUTHORS

- Write a `README`
- Write a `man` for your shell.
- You should have an `AUTHORS.md` file at the root of your repository, listing all individuals having contributed content to the repository. Format, see Docker

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `README.md, man_1_hsh, AUTHORS.md`


---
### 1. Betty would be proud

Write a beautiful code that passes the Betty checks<!--plain-NL-->

Be aware that every single C source file (<!--plain-NL-->`*.c`<!--inline-NL--> and <!--plain-NL-->`*.h`<!--inline-NL-->) inside your repository will be checked<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`


---
### 2. hsh 1.0

Write a UNIX command line interpreter.<!--plain-NL-->

- Usage: `hsh`

- Display a prompt and wait for the user to type a command. A command line always ends with a new line.
- The prompt is displayed again each time a command has been executed.
- If an executable cannot be found, print an error message and display the prompt again.
- Handle errors.
- You have to handle the “end of file” condition (`Ctrl+D`)
- Handle command lines with arguments
- Handle and parse the `PATH` environment variable

- Implement the built-in command `exit`:

Your `exit` built-in must behave exactly like `sh`‘s
You have to handle arguments
- Your `exit` built-in must behave exactly like `sh`‘s
- You have to handle arguments
- Implement the built-in command `cd`:

Changes the current directory of the process.
Command syntax: `cd [path]`
If no argument is given to `cd` the command must be interpreted like `cd $HOME`
You have to handle the command `cd -`
You have to update the environment variable `PWD` when you change directory
- Changes the current directory of the process.
- Command syntax: `cd [path]`
- If no argument is given to `cd` the command must be interpreted like `cd $HOME`
- You have to handle the command `cd -`
- You have to update the environment variable `PWD` when you change directory
- Implement the built-in command `env`:

Prints the current environment
- Prints the current environment

Implement the built-in command <!--plain-NL-->`exit`<!--inline-NL-->:<!--plain-NL-->

- Your `exit` built-in must behave exactly like `sh`‘s
- You have to handle arguments

Implement the built-in command <!--plain-NL-->`cd`<!--inline-NL-->:<!--plain-NL-->

- Changes the current directory of the process.
- Command syntax: `cd [path]`
- If no argument is given to `cd` the command must be interpreted like `cd $HOME`
- You have to handle the command `cd -`
- You have to update the environment variable `PWD` when you change directory

Implement the built-in command <!--plain-NL-->`env`<!--inline-NL-->:<!--plain-NL-->

- Prints the current environment

- handle special characters : `"`, `'`, ```, `\`, `*`, `&amp;`, `#`
- be able to move the cursor
- handle pipes and redirections

A lot of checks will be performed for this task. Thus, the auto-review can take up to <!--plain-NL-->**5 minutes**<!--code-NL-->. Make sure to test your code locally before launching the checker.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`


---
### 3. hsh 1.1

hsh 1.0 +<!--plain-NL-->

- Handle the right stream redirection `&gt;`
- Usage: `command &gt; output_file`

```
alex@~$ echo Holberton School > test
alex@~$ cat -e test
Holberton School$
alex@~$ 

```

You don’t have to handle the syntax: <!--plain-NL-->`> output_file command`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 5. hsh 1.2

hsh 1.1 +<!--plain-NL-->

- Handle the double right stream redirection `&gt;&gt;`
- Usage: `command &gt;&gt; output_file`

```
alex@~$ rm -f test
alex@~$ echo Holberton School >> test
alex@~$ cat -e test
Holberton School$
alex@~$ echo Holberton School >> test
alex@~$ cat -e test
Holberton School$
Holberton School$
alex@~$ 

```

You don’t have to handle the syntax: <!--plain-NL-->`>> output_file command`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 6. hsh 1.3

hsh 1.2 +<!--plain-NL-->

- Handle the left stream redirection `&lt;`
- Usage: `command &lt; input_file`

```
alex@~$ cat -e small_file 
Holberton$
Second line$
alex@~$ rev < small_file
notrebloH
enil dnoceS
alex@~$

```

You don’t have to handle the syntax: <!--plain-NL-->`< input_file command`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 7. hsh 1.4

hsh 1.3 +<!--plain-NL-->

- Handle the double left stream redirection `&lt;&lt;` (also known as `heredoc`)
- Usage: `command &lt;&lt; delimiter`

```
alex@~$ cat -e << HOLBERTON
> qwertyuiop
> ls -l                          
> cat -e small_file
> HOLBERTONnope
> nopeHOLBERTON
> HOLBERTON 
> HOLBERTON
qwertyuiop$
ls -l$
cat -e small_file$
HOLBERTONnope$
nopeHOLBERTON$
HOLBERTON $
alex@~$

```

You don’t have to handle the syntax: <!--plain-NL-->`<< delimiter command`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 8. hsh 1.5

hsh 1.4 +<!--plain-NL-->

- Handle the pipe stream redirection `|`
- Usage: `command1 | command2`

```
alex@~$ ls /var | rev
spukcab
ehcac
hsarc
bil
lacol
kcol
gol
liam
scirtem
tpo
nur
loops
pmt
alex@~$ ls -lr /var | cat -e
total 44$
drwxrwxrwt  2 root root     4096 Jul  5 10:26 tmp$
drwxr-xr-x  9 root root     4096 Feb 17  2016 spool$
lrwxrwxrwx  1 root root        4 Nov 19  2016 run -> /run$
drwxr-xr-x  2 root root     4096 Feb 17  2016 opt$
drwxrwsrwt  2 root whoopsie 4096 Feb 17  2016 metrics$
drwxrwsr-x  2 root mail     4096 Feb 17  2016 mail$
drwxrwxr-x 14 root syslog   4096 Jul 11 09:34 log$
lrwxrwxrwx  1 root root        9 Nov 19  2016 lock -> /run/lock$
drwxrwsr-x  2 root staff    4096 Apr 10  2014 local$
drwxr-xr-x 70 root root     4096 Mar 21 13:06 lib$
drwxrwsrwt  2 root whoopsie 4096 Jul 11 14:54 crash$
drwxr-xr-x 17 root root     4096 Feb 17  2016 cache$
drwxr-xr-x  2 root root     4096 Jul 11 09:33 backups$
alex@~$ echo "Holberton" | wc -c
10
alex@~$ 

```

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 9. hsh 1.6

hsh 1.5 +<!--plain-NL-->

- Handle the commands separator `;`

```
alex@~$ ls /var ; ls /var
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /hbtn ; ls /var
ls: cannot access /hbtn: No such file or directory
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /var ; ls /hbtn
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
ls: cannot access /hbtn: No such file or directory
alex@~$ ls /var ; ls /hbtn ; ls /var ; ls /var
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
ls: cannot access /hbtn: No such file or directory
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$

```

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 10. hsh 1.7

hsh 1.6 +<!--plain-NL-->

- Handle the `&amp;&amp;` logical operator

```
alex@~$ ls /var && ls /var
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /hbtn && ls /var
ls: cannot access /hbtn: No such file or directory
alex@~$ ls /var && ls /var && ls /var && ls /hbtn
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
ls: cannot access /hbtn: No such file or directory
alex@~$ ls /var && ls /var && ls /var && ls /hbtn && ls /hbtn
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
ls: cannot access /hbtn: No such file or directory
alex@~$

```

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 11. hsh 1.8

hsh 1.7 +<!--plain-NL-->

- Handle the `||` logical operator

```
alex@~$ ls /var || ls /var
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /hbtn || ls /var
ls: cannot access /hbtn: No such file or directory
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /hbtn || ls /hbtn || ls /hbtn || ls /var
ls: cannot access /hbtn: No such file or directory
ls: cannot access /hbtn: No such file or directory
ls: cannot access /hbtn: No such file or directory
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$ ls /hbtn || ls /hbtn || ls /hbtn || ls /var || ls /var
ls: cannot access /hbtn: No such file or directory
ls: cannot access /hbtn: No such file or directory
ls: cannot access /hbtn: No such file or directory
backups  cache  crash  lib  local  lock  log  mail  metrics  opt  run  spool  tmp
alex@~$

```

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`


---
### 12. hsh 2.0

hsh 1.8 +<!--plain-NL-->

Implement the <!--plain-NL-->`setenv`<!--inline-NL--> and <!--plain-NL-->`unsetenv`<!--inline-NL--> builtin commands<!--plain-NL-->

- `setenv`

Initialize a new environment variable, or modify an existing one
Command syntax: `setenv VARIABLE VALUE`
Should print something on stderr on failure
- Initialize a new environment variable, or modify an existing one
- Command syntax: `setenv VARIABLE VALUE`
- Should print something on stderr on failure
- `unsetenv`

Remove a environment variable
Command syntax: `unsetenv VARIABLE`
Should print something on stderr on failure
- Remove a environment variable
- Command syntax: `unsetenv VARIABLE`
- Should print something on stderr on failure

- Initialize a new environment variable, or modify an existing one
- Command syntax: `setenv VARIABLE VALUE`
- Should print something on stderr on failure

- Remove a environment variable
- Command syntax: `unsetenv VARIABLE`
- Should print something on stderr on failure

**Repo:**

- GitHub repository: `atlas-shell_v2`
- File: `Makefile`