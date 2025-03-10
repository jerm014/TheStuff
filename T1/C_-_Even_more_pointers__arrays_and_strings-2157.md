# Project 2157: C - Even more pointers, arrays and strings
----



*For this project, we expect you to look at this concept:*

* [Pointers and arrays](/concepts/888)

![1](2157_1.jpg)

## Resources

**Read or watch**:

* [C - Pointer to Pointer](https://www.tutorialspoint.com/cprogramming/c_pointer_to_pointer.htm)
* [C � Pointer to Pointer with example](https://beginnersbook.com/2014/01/c-pointer-to-pointer/)
* [Multi-dimensional Arrays in C](https://www.tutorialspoint.com/cprogramming/c_multi_dimensional_arrays.htm)
* [Two dimensional (2D) arrays in C programming with example](https://beginnersbook.com/2014/01/2d-arrays-in-c-example/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What are pointers to pointers and how to use them
* What are multidimensional arrays and how to use them
* What are the most common C standard library functions to manipulate strings
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be compiled on Ubuntu 20.04 LTS using`gcc`, using the options`-Wall -Werror -Wextra -pedantic -std=gnu89`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project is mandatory
* Your code should use the`Betty`style. It will be checked using[betty-style.pl](https://github.com/hs-hq/Betty/blob/master/betty-style.pl)and[betty-doc.pl](https://github.com/hs-hq/Betty/blob/master/betty-doc.pl)
* You are not allowed to use global variables
* No more than 5 functions per file
* You are not allowed to use the standard library. Any use of functions like`printf`,`puts`, etc� is forbidden
* You are allowed to use[_putchar](https://github.com/hs-hq/_putchar.c/blob/master/_putchar.c)
* You don�t have to push`_putchar.c`, we will use our file. If you do it won�t be taken into account
* In the following examples, the`main.c`files are shown as examples. You can use them to test your functions, but you don�t have to push them to your repo (if you do we won�t take them into account). We will use our own`main.c`files at compilation. Our`main.c`files might be different from the one shown in the examples
* The prototypes of all your functions and the prototype of the function`_putchar`should be included in your header file called`main.h`
* Don�t forget to push your header file
## More Info

You do not need to learn about pointers to functions, arrays of structures,`malloc`and`free`- yet.

**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What is the size of`p`in this code?

``
```
int *p;
```

 * 4 bytes

 * 8 bytes

 * 16 bytes

#### Question #1

What is the size of`p`in this code?

``
```
int **p;
```

 * 4 bytes

 * 8 bytes

 * 16 bytes

#### Question #2

In this following code, what is the value of`a[0][0]`?

``
```
int a[5][2] = {{1, 2}, {3, 4}, {5, 6}, {7, 8}, {9, 10}};
```

 * 1

 * 2

 * 3

 * 4

#### Question #3

In this following code, what is the value of`a[3][0]`?

``
```
int a[5][2] = {{1, 2}, {3, 4}, {5, 6}, {7, 8}, {9, 10}};
```

 * 7

 * 8

 * {7, 8}

 * 5

#### Question #4

In this following code, what is the value of`a[3][1]`?

``
```
int a[5][2] = {{1, 2}, {3, 4}, {5, 6}, {7, 8}, {9, 10}};
```

 * 7

 * 9

 * {7, 8}

 * 8

#### Question #5

In this following code, what is the value of`a[1][1]`?

``
```
int a[5][2] = {{1, 2}, {3, 4}, {5, 6}, {7, 8}, {9, 10}};
```

 * 1

 * 2

 * 3

 * 4

#### Question #6

What is the size of`*p`in this code?

``
```
int **p;
```

 * 4 bytes

 * 8 bytes

 * 16 bytes

#### Question #7

What is the size of`*p`in this code?

``
```
int *p;
```

 * 4 bytes

 * 8 bytes

 * 16 bytes

#### Question #8

What is stored inside a pointer to a pointer to an int?

 * An address where an int is stored

 * An int

 * An address where an address is stored


----
## Tasks
---
### 0. memset

Write a function that fills memory with a constant byte.

FYI: The standard library provides a similar function: memset. Run man memset to learn more.

- Prototype: `char *_memset(char *s, char b, unsigned int n);`
- The `_memset()` function fills the first `n` bytes of the memory area pointed to by `s` with the constant byte `b`
- Returns a pointer to the memory area `s`

```
julien@ubuntu:~/$ cat 0-main.c
#include "main.h"
#include <stdio.h>

/**
 * simple_print_buffer - prints buffer in hexa
 * @buffer: the address of memory to print
 * @size: the size of the memory to print
 *
 * Return: Nothing.
 */
void simple_print_buffer(char *buffer, unsigned int size)
{
        unsigned int i;

        i = 0;
        while (i < size)
        {
                if (i % 10)
                {
                        printf(" ");
                }
                if (!(i % 10) && i)
                {
                        printf("\n");
                }
                printf("0x%02x", buffer[i]);
                i++;
        }
        printf("\n");
}

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char buffer[98] = {0x00};

    simple_print_buffer(buffer, 98);
    _memset(buffer, 0x01, 95);
    printf("-------------------------------------------------\n");
    simple_print_buffer(buffer, 98);    
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 0-main.c 0-memset.c -o 0-memset
julien@ubuntu:~/$ ./0-memset 
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
-------------------------------------------------
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01 0x01
0x01 0x01 0x01 0x01 0x01 0x00 0x00 0x00
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `0-memset.c`


---
### 1. memcpy

Write a function that copies memory area.

FYI: The standard library provides a similar function: memcpy. Run man memcpy to learn more.

- Prototype: `char *_memcpy(char *dest, char *src, unsigned int n);`
- The `_memcpy()`  function  copies `n` bytes from memory area `src` to memory area `dest`
- Returns a pointer to `dest`

```
julien@ubuntu:~/$ cat 1-main.c
#include "main.h"
#include <stdio.h>

/**
 * simple_print_buffer - prints buffer in hexa
 * @buffer: the address of memory to print
 * @size: the size of the memory to print
 *
 * Return: Nothing.
 */
void simple_print_buffer(char *buffer, unsigned int size)
{
    unsigned int i;

    i = 0;
    while (i < size)
    {
        if (i % 10)
        {
            printf(" ");
        }
        if (!(i % 10) && i)
        {
            printf("\n");
        }
        printf("0x%02x", buffer[i]);
        i++;
    }
    printf("\n");
}

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char buffer[98] = {0};
    char buffer2[98] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14};

    simple_print_buffer(buffer, 98);
    _memcpy(buffer + 50, buffer2, 10);
    printf("-------------------------------------------------\n");
    simple_print_buffer(buffer, 98);    
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 1-main.c 1-memcpy.c -o 1-memcpy
julien@ubuntu:~/$ ./1-memcpy 
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
-------------------------------------------------
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x01 0x02 0x03 0x04 0x05 0x06 0x07 0x08 0x09 0x0a
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `1-memcpy.c`


---
### 2. strchr

Write a function that locates a character in a string.

FYI: The standard library provides a similar function: strchr. Run man strchr to learn more.

- Prototype: `char *_strchr(char *s, char c);`
- Returns a pointer to the first occurrence of the character `c` in the string `s`, or `NULL` if the character is not  found

```
julien@ubuntu:~/$ cat 2-main.c
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char *s = "hello";
    char *f;

    f = _strchr(s, 'l');

    if (f != NULL)
    {
        printf("%s\n", f);
    }
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 2-main.c 2-strchr.c -o 2-strchr
julien@ubuntu:~/$ ./2-strchr 
llo
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `2-strchr.c`


---
### 3. strspn

Write a function that gets the length of a prefix substring.

FYI: The standard library provides a similar function: strspn. Run man strspn to learn more.

- Prototype: `unsigned int _strspn(char *s, char *accept);`
- Returns the number of bytes in the initial segment of `s` which consist only of bytes from `accept`

```
julien@ubuntu:~/$ cat 3-main.c
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char *s = "hello, world";
    char *f = "oleh";
    unsigned int n;

    n = _strspn(s, f);
    printf("%u\n", n);
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 3-main.c 3-strspn.c -o 3-strspn
julien@ubuntu:~/$ ./3-strspn 
5
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `3-strspn.c`


---
### 4. strpbrk

Write a function that searches a string for any of a set of bytes.

FYI: The standard library provides a similar function: strpbrk. Run man strpbrk to learn more.

- Prototype: `char *_strpbrk(char *s, char *accept);`
- The `_strpbrk()`  function locates the first occurrence in the string `s` of any of the bytes in the string `accept`
- Returns a pointer to the byte in `s` that matches one of the bytes in `accept`,  or `NULL` if no such byte is found

```
julien@ubuntu:~/$ cat 4-main.c
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char *s = "hello, world";
    char *f = "world";
    char *t;

    t = _strpbrk(s, f);
    printf("%s\n", t);
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 4-main.c 4-strpbrk.c -o 4-strpbrk
julien@ubuntu:~/$ ./4-strpbrk 
llo, world
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `4-strpbrk.c`


---
### 5. strstr

Write a function that locates a substring.

FYI: The standard library provides a similar function: strstr. Run man strstr to learn more.

- Prototype: `char *_strstr(char *haystack, char *needle);`
- The `_strstr()` function finds the first occurrence of the substring `needle` in the string `haystack`.  The terminating null bytes (`\0`) are not compared
- Returns a pointer to the beginning of the located substring, or `NULL` if the substring is not found.

```
julien@ubuntu:~/$ cat 5-main.c
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char *s = "hello, world";
    char *f = "world";
    char *t;

    t = _strstr(s, f);
    printf("%s\n", t);
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 5-main.c 5-strstr.c -o 5-strstr
julien@ubuntu:~/$ ./5-strstr 
world
julien@ubuntu:~/$ 


```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `5-strstr.c`


---
### 6. Chess is mental torture

Write a function that prints the chessboard.

- Prototype: `void print_chessboard(char (*a)[8]);`

```
julien@ubuntu:~/$ cat 7-main.c 
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    char board[8][8] = {
        {'r', 'k', 'b', 'q', 'k', 'b', 'k', 'r'},
        {'p', 'p', 'p', 'p', 'p', 'p', 'p', 'p'},
        {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
        {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '},
        {'P', 'P', 'P', 'P', 'P', 'P', 'P', 'P'},
        {'R', 'K', 'B', 'Q', 'K', 'B', 'K', 'R'},
    };
    print_chessboard(board);
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 _putchar.c 7-main.c 7-print_chessboard.c -o 7-print_chessboard
julien@ubuntu:~/$ ./7-print_chessboard 
rkbqkbkr
pppppppp




PPPPPPPP
RKBQKBKR
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `7-print_chessboard.c`


---
### 7. The line of life is a ragged diagonal between duty and desire

Write a function that prints the sum of the two diagonals of a square matrix of integers.

Note that in the following example we are casting an int[][] into an int*. This is not something you should do. The goal here is to make sure you understand how an array of array is stored in memory.

- Prototype: `void print_diagsums(int *a, int size);`
- Format: see example
- You are allowed to use the standard library

```
julien@ubuntu:~/$ cat 8-main.c
#include "main.h"
#include <stdio.h>

/**
 * main - check the code
 *
 * Return: Always 0.
 */
int main(void)
{
    int c3[3][3] = {
        {0, 1, 5},
        {10, 11, 12},
        {1000, 101, 102},
    };
    int c5[5][5] = {
        {0, 1, 5, 12124, 1234},
        {10, 11, 12, 123521, 12512},
        {1000, 101, 102, 12545, 214543435},
        {100, 1012451, 11102, 12545, 214543435},
        {10, 12401, 10452, 11542545, 1214543435},
    };
    print_diagsums((int *)c3, 3);
    print_diagsums((int *)c5, 5);
    return (0);
}
julien@ubuntu:~/$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 8-main.c 8-print_diagsums.c -o 8-print_diagsums
julien@ubuntu:~/$ ./8-print_diagsums 
113, 1016
1214556093, 1137318
julien@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `pointers_arrays_strings`
- File: `8-print_diagsums.c`