# Project 2214: C - Signals
----


## Resources

**Read or watch**:

* [Signals](https://en.wikipedia.org/wiki/Signal_%28IPC%29)
* [Asynchrony](https://en.wikipedia.org/wiki/Asynchrony_%28computer_programming%29)
* [Signal sets](https://www.gnu.org/software/libc/manual/html_node/Signal-Sets.html)

**man or help**:

* `signal (7)`
* `signal (2)`
* `sigaction (2)`
* `kill (2)`
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is a signal
* Why do they exist
* When are they delivered and by whom
* What are the default actions of signals
* How to set up a handler for a signal
* How to send signals
* What signals can’t be caught
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be compiled on Ubuntu 20.04 LTS
* Your C programs and functions will be compiled with`gcc 9.4.0`using the flags`-Wall``-Werror``-Wextra``and -pedantic`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project is mandatory
* Your code should use the`Betty`style. It will be checked using[betty-style.pl](https://github.com/hs-hq/Betty/blob/master/betty-style.pl)and[betty-doc.pl](https://github.com/hs-hq/Betty/blob/master/betty-doc.pl)
* You are allowed to have more than 5 functions per file
* The prototypes of all your functions should be included in your header file called`signals.h`
* Don’t forget to push your header file
* All your header files should be include guarded
### Allowed functions and system calls

* Unless specified otherwise in a task, you are allowed to use the C standard library
**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What are the different actions the Kernel can take on a process when a signal is raised?

 * terminate the process

 * terminate + core dump

 * reload a running service

 * signal is ignored

 * run in background

 * stop the process

 * restart the process

 * continue the process

#### Question #1

What function(s) can one process use to send a signal to another process?

 * `kill`

 * `signal`

 * `alarm`

 * `killpg`

 * `raise`

 * `sigaction`

#### Question #2

What function(s) can one process use to send a signal to itself?

 * `kill`

 * `signal`

 * `alarm`

 * `killpg`

 * `raise`

 * `sigaction`

#### Question #3

What is the signal sent to the foreground process when you type`Control-C`in most of terminals?

 * `SIGINT`

 * `SIGTERM`

 * `SIGKILL`

 * `SIGQUIT`

 * `SIGABRT`

 * `SIGTSTOP`

#### Question #4

What is the signal sent to the foreground process when you type`Control-\`in most of terminals?

 * `SIGINT`

 * `SIGTERM`

 * `SIGKILL`

 * `SIGQUIT`

 * `SIGABRT`

 * `SIGTSTOP`

#### Question #5

What is the signal sent to the foreground process when you type`Control-Z`in most of terminals?

 * `SIGINT`

 * `SIGTERM`

 * `SIGKILL`

 * `SIGQUIT`

 * `SIGABRT`

 * `SIGTSTP`

#### Question #6

Which of the following signals can’t be blocked, ignored or caught?

 * `SIGINT`

 * `SIGTERM`

 * `SIGKILL`

 * `SIGQUIT`

 * `SIGABRT`

 * `SIGSTOP`

#### Question #7

Which of the following signals are are not defined in`POSIX`(any version)?

 * `SIGEMT`

 * `SIGTSTP`

 * `SIGCLD`

 * `SIGTRAP`

 * `SIGBUS`

 * `SIGIOT`

 * `SIGWINCH`

#### Question #8

On Linux, what is the`sigset_t`data type?

 * A linked list

 * A hash table

 * A bit mask

 * An array


----
## Tasks
---
### 0. Handle signal

Write a function that set a handler for the signal <!--plain-NL-->`SIGINT`<!--inline-NL-->

- Prototype: `int handle_signal(void);`
- Your function must return `0` on success, or `-1` on error
- The program should print `Gotcha! [&lt;signum&gt;]` followed by a new line, every time `Control-C` is pressed (See example below)


where `&lt;signum&gt;` must be replaced with the signal number that was caught
- where `&lt;signum&gt;` must be replaced with the signal number that was caught
- `sigaction`(2) is not allowed

- where `&lt;signum&gt;` must be replaced with the signal number that was caught

```
alex@~/signals$ cat 0-main.c
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

#include "signals.h"

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    int i;

    if (handle_signal() == -1)
    {
        printf("Failure\n");
        return (EXIT_FAILURE);
    }
    for (i = 0; ; i++)
    {
        printf("[%d] Wait for it ...\n", i);
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 0-main.c 0-handle_signal.c -o 0-handle_signal
alex@~/signals$ ./0-handle_signal 
[0] Wait for it ...
[1] Wait for it ...
[2] Wait for it ...
^CGotcha! [2]
[3] Wait for it ...
^CGotcha! [2]
[4] Wait for it ...
[5] Wait for it ...
^CGotcha! [2]
[6] Wait for it ...
[7] Wait for it ...
^CGotcha! [2]
[8] Wait for it ...
[9] Wait for it ...
^\Quit (core dumped)
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `0-handle_signal.c`


---
### 1. Current handler - signal

Write a function that retrieves the current handler of the signal SIGINT<!--plain-NL-->

- Prototype: `void (*current_handler_signal(void))(int);`
- Your function returns a pointer to the current handler of SIGINT, or `NULL` on failure
- You are not allowed to use `sigaction`(2)
- The handler must be unchanged after calling your function

```
alex@~/signals$ cat 1-main.c 
#include <stdlib.h>
#include <stdio.h>
#include <unistd.h>

#include "signals.h"

/* Our functions */
void print_hello(int);
void set_print_hello(void);

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    void (*handler)(int);
    int i;

    handler = current_handler_signal();
    printf("Address of the current handler: %#lx\n", (unsigned long int)handler);

    /* Set 'print_hello()` as the handler for SIGINT */
    set_print_hello();

    handler = current_handler_signal();
    printf("Address of the 'print_hello' function: %#lx\n", (unsigned long int)&print_hello);
    printf("Address of the current handler: %#lx\n", (unsigned long int)handler);

    for (i = 0; ; i++)
    {
        printf("[%d] Wait for it ...\n", i);
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 1-main.c 1-set_print_hello.c 1-current_handler_signal.c -o 1-current_handler_signal
alex@~/signals$ ./1-current_handler_signal
Address of the current handler: 0
Address of the 'print_hello' function: 0x4006da
Address of the current handler: 0x4006da
[0] Wait for it ...
[1] Wait for it ...
^CHello :)
[2] Wait for it ...
^CHello :)
[3] Wait for it ...
[4] Wait for it ...
^CHello :)
[5] Wait for it ...
^\Quit (core dumped)
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `1-current_handler_signal.c`


---
### 2. Gotta catch them all

Write a function that set a handler for the signal <!--plain-NL-->`SIGINT`<!--inline-NL-->

- Prototype: `int handle_sigaction(void);`
- Your function must return `0` on success, or `-1` on error
- The program should print `Gotcha! [&lt;signum&gt;]` followed by a new line, every time `Control-C` is pressed (See example below)


where `&lt;signum&gt;` must be replaced with the signal number that was caught
- where `&lt;signum&gt;` must be replaced with the signal number that was caught
- `signal`(2) is not allowed

- where `&lt;signum&gt;` must be replaced with the signal number that was caught

```
alex@~/signals$ cat 2-main.c 
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

#include "signals.h"

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    int i;

    if (handle_sigaction() == -1)
    {
        printf("Failure\n");
        return (EXIT_FAILURE);
    }
    for (i = 0; ; i++)
    {
        printf("[%d] Wait for it ...\n", i);
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 2-main.c 2-handle_sigaction.c -o 2-handle_sigaction
alex@~/signals$ ./2-handle_sigaction 
[0] Wait for it ...
[1] Wait for it ...
^CGotcha! [2]
[2] Wait for it ...
[3] Wait for it ...
^CGotcha! [2]
[4] Wait for it ...
^CGotcha! [2]
[5] Wait for it ...
^CGotcha! [2]
[6] Wait for it ...
[7] Wait for it ...
^CGotcha! [2]
[8] Wait for it ...
^\Quit (core dumped)
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `2-handle_sigaction.c`


---
### 3. Current handler - sigaction

Write a function that retrieves the current handler of the signal SIGINT<!--plain-NL-->

- Prototype: `void (*current_handler_sigaction(void))(int);`
- Your function returns a pointer to the current handler of SIGINT, or `NULL` on failure
- You have to use the function `sigaction` (`signal` is not allowed)
- The handler must be unchanged after calling your function

```
alex@~/signals$ cat 3-main.c 
#include <stdlib.h>
#include <stdio.h>
#include <unistd.h>

#include "signals.h"

/* Our functions */
void print_hello(int);
void set_print_hello(void);

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    void (*handler)(int);
    int i;

    handler = current_handler_sigaction();
    printf("Address of the current handler: %#lx\n", (unsigned long int)handler);

    /* Set 'print_hello()` as the handler for SIGINT */
    set_print_hello();

    handler = current_handler_sigaction();
    printf("Address of the 'print_hello' function: %#lx\n", (unsigned long int)&print_hello);
    printf("Address of the current handler: %#lx\n", (unsigned long int)handler);

    for (i = 0; ; i++)
    {
        printf("[%d] Wait for it ...\n", i);
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 3-main.c 3-set_print_hello.c 3-current_handler_sigaction.c -o 3-current_handler_sigaction
alex@~/signals$ ./3-current_handler_sigaction 
Address of the current handler: 0
Address of the 'print_hello' function: 0x4006ea
Address of the current handler: 0x4006ea
[0] Wait for it ...
[1] Wait for it ...
^CHello :)
[2] Wait for it ...
^CHello :)
[3] Wait for it ...
[4] Wait for it ...
^CHello :)
[5] Wait for it ...
^CHello :)
[6] Wait for it ...
^\Quit (core dumped)
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `3-current_handler_sigaction.c`


---
### 4. Who said that?!

Write a function that defines a handler for the signal <!--plain-NL-->`SIGQUIT`<!--inline-NL--> (<!--plain-NL-->`Control-\`<!--inline-NL--> in a shell)<!--plain-NL-->

- Prototype: `int trace_signal_sender(void);`
- The handler must print `SIGQUIT sent by &lt;pid&gt;` each time a `SIGQUIT` (and only a `SIGQUIT`) is caught


Where `&lt;pid&gt;` must be replaced by the PID of the process that sent the signal
- Where `&lt;pid&gt;` must be replaced by the PID of the process that sent the signal
- Your function must return `0` on success, or `-1` on error

- Where `&lt;pid&gt;` must be replaced by the PID of the process that sent the signal

```
alex@~/signals$ cat 4-main.c
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

#include "signals.h"

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    int i;

    if (trace_signal_sender() == -1)
    {
        printf("Failure\n");
        return (EXIT_FAILURE);
    }
    for (i = 0; ; i++)
    {
        printf("[%d] Wait for it ...\n", i);
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 4-main.c 4-trace_signal_sender.c -o 4-trace_signal_sender
alex@~/signals$ ./4-trace_signal_sender
[0] Wait for it ...
[1] Wait for it ...
^\SIGQUIT sent by 0
[2] Wait for it ...
^\SIGQUIT sent by 0
[3] Wait for it ...
^\SIGQUIT sent by 0
[4] Wait for it ...
[5] Wait for it ...
^\SIGQUIT sent by 0
[6] Wait for it ...
[7] Wait for it ...
[8] Wait for it ...
SIGQUIT sent by 95337
[9] Wait for it ...
^C
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `4-trace_signal_sender.c`


---
### 5. Description

Write a program that prints a description of a given signal<!--plain-NL-->

- Usage: `./describe &lt;signum&gt;`

Where `&lt;signum&gt;` is the signal number to be described
If the number of arguments is not correct, your program must print `Usage: %s &lt;signum&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`
- Where `&lt;signum&gt;` is the signal number to be described
- If the number of arguments is not correct, your program must print `Usage: %s &lt;signum&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`
- You’re not allowed to have more than `1` function in your file
- You’re not allowed to have more than `12` lines in your function
- You can assume that if a parameter is given, it will be a number

- Where `&lt;signum&gt;` is the signal number to be described
- If the number of arguments is not correct, your program must print `Usage: %s &lt;signum&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`

```
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 5-signal_describe.c -o 5-signal_describe
alex@~/signals$ ./5-signal_describe
Usage: ./5-signal_describe <signum>
alex@~/signals$ ./5-signal_describe 1
1: Hangup
alex@~/signals$ ./5-signal_describe 9
9: Killed
alex@~/signals$ ./5-signal_describe 3
3: Quit
alex@~/signals$ ./5-signal_describe 2
2: Interrupt
alex@~/signals$ ./5-signal_describe 0
0: Unknown signal 0
alex@~/signals$ ./5-signal_describe 100
100: Unknown signal 100
alex@~/signals$ ./5-signal_describe 20
20: Stopped
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `5-signal_describe.c`


---
### 6. Catch a single time

Write a program that sets a handler for the signal <!--plain-NL-->`SIGINT`<!--inline-NL-->, and exits right after the signal is received and handled<!--plain-NL-->

- Your program does not take any argument
- Your program should suspend indefinitely until a signal is received
- When a `SIGINT` is received, you must print `Caught %d` (where `%d` must be replaced by the signal number), followed by a new line
- After the first `SIGINT` is received, your program must:


Print `Signal received`, followed by a new line
Exit with `EXIT_SUCCESS`
- Print `Signal received`, followed by a new line
- Exit with `EXIT_SUCCESS`
- You are not allowed to use the functions `exit`, `sleep` or `_exit`
- You are not allowed to use any kind of loop (`while`, `for`, `do/while`)

- Print `Signal received`, followed by a new line
- Exit with `EXIT_SUCCESS`

```
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 6-suspend.c -o 6-suspend
alex@~/signals$ ./6-suspend 
^CCaught 2
Signal received
alex@~/signals$ echo $?
0
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `6-suspend.c`


---
### 7. Sending a signal

Write a program that sends the signal <!--plain-NL-->`SIGINT`<!--inline-NL--> to a process, given its PID<!--plain-NL-->

- Usage: `signal_send &lt;pid&gt;`

Where `&lt;pid&gt;` is the PID of the process to send a signal to
If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`
`&lt;pid&gt;` won’t be `0`
- Where `&lt;pid&gt;` is the PID of the process to send a signal to
- If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`
- `&lt;pid&gt;` won’t be `0`
- Your program must return `EXIT_SUCCESS` on success, or `EXIT_FAILURE`
- You’re not allowed to have more than `1` function in your file

- Where `&lt;pid&gt;` is the PID of the process to send a signal to
- If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `EXIT_FAILURE`
- `&lt;pid&gt;` won’t be `0`

```
alex@~/signals$ cat 7-main.c
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

/**
 * main - Simple program, printing its PID and running infinitely
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    pid_t pid;

    pid = getpid();
    printf("PID: %d\n", (int)pid);
    while (98)
    {
        printf("Waiting ...\n");
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 7-main.c -o 7-wait_for_it
alex@~/signals$ ./7-wait_for_it 
PID: 98631
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...

alex@~/signals$

```

While the above example is in its <!--plain-NL-->`Waiting`<!--inline-NL--> state, execute the following, and it should terminate the process above.<!--plain-NL-->

```
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 7-signal_send.c -o 7-signal_send
alex@~/signals$ ./7-signal_send
Usage: ./7-signal_send <pid>
alex@~/signals$ ./7-signal_send 98631
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `7-signal_send.c`


---
### 8. Sending a signal in a shell

Write a <!--plain-NL-->`sh`<!--inline-NL--> script that sends the signal <!--plain-NL-->`SIGQUIT`<!--inline-NL--> to a process, given its PID<!--plain-NL-->

- Usage: `signal_send.sh &lt;pid&gt;`

Where `&lt;pid&gt;` is the PID of the process to send a signal to
If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `1`
- Where `&lt;pid&gt;` is the PID of the process to send a signal to
- If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `1`

- Where `&lt;pid&gt;` is the PID of the process to send a signal to
- If the number of arguments is not correct, your program must print `Usage: %s &lt;pid&gt;` (where `%s` is argv[0]), followed by a new line, and exit with `1`

```
alex@~/signals$ cat 8-main.c
#include <stdlib.h>
#include <unistd.h>
#include <stdio.h>

/**
 * main - Simple program, printing its PID and running infinitely
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    pid_t pid;

    pid = getpid();
    printf("PID: %d\n", (int)pid);
    while (98)
    {
        printf("Waiting ...\n");
        sleep(1);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 8-main.c -o 8-wait_for_it
alex@~/signals$ ./8-wait_for_it 
PID: 98988
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...
Waiting ...

alex@~/signals$

```

While the above example is in its <!--plain-NL-->`Waiting`<!--inline-NL--> state, execute the following, and it should terminate the process above.<!--plain-NL-->

```
alex@~/signals$ sh ./8-signal_send.sh
Usage: ./8-signal_send <pid>
alex@~/signals$ sh ./8-signal_send.sh 98988
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `8-signal_send.sh`


---
### 9. Catch with sh

Write a <!--plain-NL-->`sh`<!--inline-NL--> script that set a handler for the signals <!--plain-NL-->`SIGABRT`<!--inline-NL-->, <!--plain-NL-->`SIGIO`<!--inline-NL--> and <!--plain-NL-->`SIGTERM`<!--inline-NL-->

- The script must print `Nope` followed by a new line, each time a `SIGABRT`, `SIGIO` or `SIGTERM` is caught
- Your script must contain a shebang
- You’re not allowed to have more than 2 lines in your script
- You’re not allowed to have more than 1 instruction per line

```
alex@~/signals$ cat 9-main.sh
#!/bin/sh
. ./9-handle_signal.sh

echo "PID: $$"

while :
do
    echo "Waiting ..."
    sleep 2
done
alex@~/signals$ sh 9-main.sh
PID: 99440
Waiting ...
Waiting ...
Nope
Waiting ...
Nope
Waiting ...
Nope
Waiting ...
Nope
Waiting ...
Waiting ...
Nope
Waiting ...
Nope
Waiting ...
Waiting ...
Waiting ...
Nope
Waiting ...
Nope
Waiting ...
Waiting ...
Killed
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `9-handle_signal.sh`


---
### 10. Does it exist?

Write a function that tests if a process exists, given its PID<!--plain-NL-->

- Prototype: `int pid_exist(pid_t pid);`
- Your function must return `1` if the process with the PID `pid` exists, or `0` otherwise
- You’re not allowed to have more than `1` function in your file
- You’re not allowed to have more than `1` line in your function
- You’re not allowed to include more than `2` headers in your file
- You’re not allowed to include your header file `signals.h`
- You’re not allowed to use the function `getpgid`

```
alex@~/signals$ cat 10-main.c 
#include <stdlib.h>
#include <stdio.h>

#include "signals.h"

/**
 * main - Entry point
 * @argc: Arguments counter
 * @argv: Arguments vector
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(int argc, const char *argv[])
{
    pid_t pid;

    if (argc < 2)
    {
        fprintf(stderr, "Usage: %s <pid>\n", argv[0]);
        return (EXIT_FAILURE);
    }
    pid = atoi(argv[1]);

    if (pid_exist(pid))
    {
        printf("PID %d exists\n", pid);
    }
    else
    {
        printf("PID %d does not exist\n", pid);
    }
    return (EXIT_SUCCESS);
}
alex@~/signals$ gcc -Wall -Wextra -Werror -pedantic 10-main.c 10-pid_exist.c -o 10-pid_exist
alex@~/signals$ ./10-pid_exist 1
PID 1 exists
alex@~/signals$ ./10-pid_exist 2
PID 2 exists
alex@~/signals$ ./10-pid_exist 1234
PID 1234 does not exist
alex@~/signals$ ./10-pid_exist 98
PID 98 does not exist
alex@~/signals$ ./10-pid_exist 890
PID 890 exists
alex@~/signals$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `signals`
- File: `10-pid_exist.c`


---
### 11. Blog post

Write a blog post about signals<!--plain-NL-->

Your blog post should cover the following:<!--plain-NL-->

- What is a signal
- Why do they exist
- When are they delivered and by whom
- What are the default actions of signals
- What happens to a process when it receives a signal without handling it
- What happens to a process when it receives a signal and handles it

Your posts should have examples and at least one picture, at the top. Publish your blog post on <!--plain-NL-->`Medium`<!--inline-NL--> or <!--plain-NL-->`LinkedIn`<!--inline-NL-->, and share it at least on <!--plain-NL-->`LinkedIn`<!--inline-NL-->.<!--plain-NL-->

When done, please add all urls below (blog post, tweet, etc.)<!--plain-NL-->

Please, remember that these blogs must be written in English to further your technical ability in a variety of settings.<!--plain-NL-->