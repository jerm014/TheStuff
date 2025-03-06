# Project 2208: C - Static variables, getline
----


## Resources

**Read or watch**:

* [C - Static Variables](https://www.geeksforgeeks.org/static-variables-in-c/)
* [Google](http://www.google.com)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What are static variables?
* How and when to use them?
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be compiled on Ubuntu 20.04 LTS
* Your C programs and functions will be compiled with`gcc 9.4.0`using the flags`-Wall``-Werror``-Wextra``and -pedantic`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project is mandatory
* Your code should use the`Betty`style. It will be checked using[betty-style.pl](https://github.com/hs-hq/Betty/blob/master/betty-style.pl)and[betty-doc.pl](https://github.com/hs-hq/Betty/blob/master/betty-doc.pl)
* All your header files should be include guarded
* You are allowed to have up to`6 functions`in`_getline.c`
### Allowed Functions and System Calls

* `read`
* `write`
* `malloc`
* `realloc`
* `free`
* `strcpy`
* `strncpy`
* `strcat`
* `strdup`
* `memset`
* `memcpy`
**Great!**You've completed the quiz successfully! Keep going!#### Question #0

`static int i;`What is the default value of`i`?

 * We do not know

 * 0

 * This will not compile with gcc 4

 * 98

#### Question #1

`static int i = 10;`What is the default value of`i`?

 * 0

 * 10

 * 98

 * We don’t know

#### Question #2

Static variables are located in/on:

 * The data segment

 * The stack

 * The heap

 * None of the above

#### Question #3

The following program:

`
```
int init()
{
  int i;

  return (i);
}

int main()
{
  static int i = init();

  return (i);
}
```

 * Exits with the value 0

 * Exits with the value 98

 * Exits with an unknown value

 * Does not compile


----
## Tasks
---
### 0. Racing cars

Write a function that keeps track of the number of laps made by several cars in a race.<!--plain-NL-->

- Prototype : `void race_state(int *id, size_t size)`
- `id` is an array of `int` representing the “identifier” of each car.
- `size` is the size of this array
- Each car identifier is unique
- If an identifier is unknown:


Create a new car with the number of laps = 0
Print `Car X joined the race` followed by a new line (where `X` is the identifier)
- Create a new car with the number of laps = 0
- Print `Car X joined the race` followed by a new line (where `X` is the identifier)
- Each time the function is called:


The number of laps of each cars listed in `id` must be incremented by 1
Print the state of the race:


Header: `Race state:` followed by a new line
For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)
- The number of laps of each cars listed in `id` must be incremented by 1
- Print the state of the race:


Header: `Race state:` followed by a new line
For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)
- Header: `Race state:` followed by a new line
- For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)
- If your function is called with `size = 0`,you must free all allocated memory.

- Create a new car with the number of laps = 0
- Print `Car X joined the race` followed by a new line (where `X` is the identifier)

- The number of laps of each cars listed in `id` must be incremented by 1
- Print the state of the race:


Header: `Race state:` followed by a new line
For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)
- Header: `Race state:` followed by a new line
- For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)

- Header: `Race state:` followed by a new line
- For each car sorted by the identifier: `Car X [Y laps]` (where `X` is the identifier and `Y` the number of laps already done)

```
julien@ubuntu:~/getline$ cat 0-main.c 
#include "laps.h"

/**
 * main - entry point.
 *
 * Return: always 0.
 */
int main()
{

    int ids1[3] = {1, 42, 101};
    int ids2[1] = {11};

    race_state(ids1, 3);
    printf("--\n");
    race_state(ids1, 3);
    printf("--\n");
    race_state(ids1, 3);
    printf("--\n");
    race_state(ids2, 1);
    printf("--\n");
    race_state(ids1, 3);
    printf("--\n");
    race_state(ids2, 1);
    printf("--\n");
    race_state(ids1, 3);
    printf("--\n");
    race_state(ids2, 1);
    printf("--\n");
    race_state(ids1, 3);
    printf("--\n");
    race_state(ids2, 1);
    printf("--\n");
    race_state(NULL, 0);
    return (0);
}
julien@ubuntu:~/getline$ gcc -Wall -Wextra -Werror -pedantic 0-main.c laps.c  -o laps
julien@ubuntu:~/getline$ ./laps
Car 1 joined the race
Car 42 joined the race
Car 101 joined the race
Race state:
Car 1 [0 laps]
Car 42 [0 laps]
Car 101 [0 laps]
--
Race state:
Car 1 [1 laps]
Car 42 [1 laps]
Car 101 [1 laps]
--
Race state:
Car 1 [2 laps]
Car 42 [2 laps]
Car 101 [2 laps]
--
Car 11 joined the race
Race state:
Car 1 [2 laps]
Car 11 [0 laps]
Car 42 [2 laps]
Car 101 [2 laps]
--
Race state:
Car 1 [3 laps]
Car 11 [0 laps]
Car 42 [3 laps]
Car 101 [3 laps]
--
Race state:
Car 1 [3 laps]
Car 11 [1 laps]
Car 42 [3 laps]
Car 101 [3 laps]
--
Race state:
Car 1 [4 laps]
Car 11 [1 laps]
Car 42 [4 laps]
Car 101 [4 laps]
--
Race state:
Car 1 [4 laps]
Car 11 [2 laps]
Car 42 [4 laps]
Car 101 [4 laps]
--
Race state:
Car 1 [5 laps]
Car 11 [2 laps]
Car 42 [5 laps]
Car 101 [5 laps]
--
Race state:
Car 1 [5 laps]
Car 11 [3 laps]
Car 42 [5 laps]
Car 101 [5 laps]
--
julien@ubuntu:~/getline$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `getline`
- File: `laps.c, laps.h`


---
### 1. _getline

Write a function that reads an entire line from a file descriptor.<!--plain-NL-->

- Prototype : `char *_getline(const int fd)`
- Where `fd` is the file descriptor to read from
- If there are no more lines to return, or if there is an error, the function should return `NULL`
- The function returns a null-terminated string that does not include the newline character
- Your header file `_getline.h` should define a macro called `READ_SIZE`.


This macro defines the number of bytes you will read each time you will call `read`: `read(fd, buffer, READ_SIZE)`
You are not allowed to read more or less than `READ_SIZE` bytes at once from `fd`
You are free to pick the value that you want for `READ_SIZE`
- This macro defines the number of bytes you will read each time you will call `read`: `read(fd, buffer, READ_SIZE)`
- You are not allowed to read more or less than `READ_SIZE` bytes at once from `fd`
- You are free to pick the value that you want for `READ_SIZE`
- You can assume that `fd` will always be the same

- This macro defines the number of bytes you will read each time you will call `read`: `read(fd, buffer, READ_SIZE)`
- You are not allowed to read more or less than `READ_SIZE` bytes at once from `fd`
- You are free to pick the value that you want for `READ_SIZE`

```
julien@ubuntu:~/getline$ cat 1-main.c
#include <fcntl.h>
#include <stdio.h>
#include <unistd.h>
#include <stdlib.h>

#include "_getline.h"

/**
 * main - entry point.
 *
 * Return: always 0.
 */
int main(void)
{
    int fd;
    char *line;

    fd = open("1-main.c", 0);
    while ((line = _getline(fd)))
    {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
julien@ubuntu:~/getline$ gcc -Wall -Wextra -Werror -pedantic 1-main.c _getline.c -o getline
julien@ubuntu:~/getline$ ./getline
#include <fcntl.h>
#include <stdio.h>
#include <unistd.h>
#include <stdlib.h>

#include "_getline.h"

/**
 * main - entry point.
 *
 * Return: always 0.
 */
int main(void)
{
    int fd;
    char *line;

    fd = open("1-main.c", 0);
    while ((line = _getline(fd)))
    {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
julien@ubuntu:~/getline$ 

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `getline`
- File: `_getline.c, _getline.h`


---
### 2. _getline: multi-fd

Handle multiple file descriptors.<!--plain-NL-->

- when called with `-1` you should free everything and reset all your static variables

```
julien@ubuntu:~/getline$ cat 2-main.c
#include <fcntl.h>
#include <stdio.h>
#include <unistd.h>
#include <stdlib.h>

#include "_getline.h"

/**
 * main - entry point.
 *
 * Return: always 0.
 */
int main(void)
{
    int fd1, fd2, fd3;
    char *line1;
    char *line2;
    char *line3;
    int i;

    fd1 = open("the_swing", O_RDONLY);
    fd2 = open("man_gcc", O_RDONLY);
    fd3 = open("man_cat", O_RDONLY);
    printf("---------THE SWING (first 5 lines)-----------\n");
    i = 0;
    while ((line1 = _getline(fd1)))
    {
        printf("%s\n", line1);
        free(line1);
        i++;
        if (i == 5)
        {
            break;
        }
    }
    printf("----------MAN GCC (first 5 lines)----------\n");
    i = 0;
    while ((line2 = _getline(fd2)))
    {
        printf("%s\n", line2);
        free(line2);
        i++;
        if (i == 5)
        {
            break;
        }
    }
    printf("-----------MAN CAT (first 5 lines)---------\n");
    i = 0;
    while ((line3 = _getline(fd3)))
    {
        printf("%s\n", line3);
        free(line3);
        i++;
        if (i == 5)
        {
            break;
        }
    }
    printf("---------THE SWING (END)-----------\n");
    while ((line1 = _getline(fd1)))
    {
        printf("%s\n", line1);  
        free(line1);
    }   
    close(fd1);
    close(fd2);
    close(fd3);
    _getline(-1);
    printf("---------THE SWING (FULL-TEXT)-----------\n");
    fd1 = open("the_swing", O_RDONLY);
    while ((line1 = _getline(fd1)))
    {
        printf("%s\n", line1);      
        free(line1);
    }   
    close(fd1);
    _getline(-1);
    return (EXIT_SUCCESS);
}
julien@ubuntu:~/getline$ gcc -Wall -Wextra -pedantic -Werror 2-main.c _getline.c -o getline
julien@ubuntu:~/getline$ ./getline
---------THE SWING (first 5 lines)-----------
The Swing
BY ROBERT LOUIS STEVENSON
How do you like to go up in a swing, 
   Up in the air so blue? 
Oh, I do think it the pleasantest thing 
----------MAN GCC (first 5 lines)----------
GCC(1)                                 GNU                                 GCC(1)

NAME
       gcc - GNU project C and C++ compiler

-----------MAN CAT (first 5 lines)---------
CAT(1)                            User Commands                            CAT(1)

NAME
       cat - concatenate files and print on the standard output

---------THE SWING (END)-----------
   Ever a child can do! 

Up in the air and over the wall, 
   Till I can see so wide, 
Rivers and trees and cattle and all 
   Over the countryside— 

Till I look down on the garden green, 
   Down on the roof so brown— 
Up in the air I go flying again, 
   Up in the air and down!again, 
---------THE SWING (FULL-TEXT)-----------
The Swing
BY ROBERT LOUIS STEVENSON
How do you like to go up in a swing, 
   Up in the air so blue? 
Oh, I do think it the pleasantest thing 
   Ever a child can do! 

Up in the air and over the wall, 
   Till I can see so wide, 
Rivers and trees and cattle and all 
   Over the countryside— 

Till I look down on the garden green, 
   Down on the roof so brown— 
Up in the air I go flying again, 
   Up in the air and down!again, 
julien@ubuntu:~/getline$ valgrind ./getline
==4832== Memcheck, a memory error detector
==4832== Copyright (C) 2002-2013, and GNU GPL'd, by Julian Seward et al.
==4832== Using Valgrind-3.10.1 and LibVEX; rerun with -h for copyright info
==4832== Command: ./getline
==4832== 
---------THE SWING (first 5 lines)-----------
The Swing
BY ROBERT LOUIS STEVENSON
How do you like to go up in a swing, 
   Up in the air so blue? 
Oh, I do think it the pleasantest thing 
----------MAN GCC (first 5 lines)----------
GCC(1)                                 GNU                                 GCC(1)

NAME
       gcc - GNU project C and C++ compiler

-----------MAN CAT (first 5 lines)---------
CAT(1)                            User Commands                            CAT(1)

NAME
       cat - concatenate files and print on the standard output

---------THE SWING (END)-----------
   Ever a child can do! 

Up in the air and over the wall, 
   Till I can see so wide, 
Rivers and trees and cattle and all 
   Over the countryside— 

Till I look down on the garden green, 
   Down on the roof so brown— 
Up in the air I go flying again, 
   Up in the air and down!
---------THE SWING (FULL-TEXT)-----------
The Swing
BY ROBERT LOUIS STEVENSON
How do you like to go up in a swing, 
   Up in the air so blue? 
Oh, I do think it the pleasantest thing 
   Ever a child can do! 

Up in the air and over the wall, 
   Till I can see so wide, 
Rivers and trees and cattle and all 
   Over the countryside— 

Till I look down on the garden green, 
   Down on the roof so brown— 
Up in the air I go flying again, 
   Up in the air and down!
==4832== 
==4832== HEAP SUMMARY:
==4832==     in use at exit: 0 bytes in 0 blocks
==4832==   total heap usage: 84 allocs, 84 frees, 2,320 bytes allocated
==4832== 
==4832== All heap blocks were freed -- no leaks are possible
==4832== 
==4832== For counts of detected and suppressed errors, rerun with: -v
==4832== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
julien@ubuntu:~/getline$

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `getline`
- File: `_getline.c, _getline.h`