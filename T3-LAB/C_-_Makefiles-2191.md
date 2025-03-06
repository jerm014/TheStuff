# Project 2191: C - Makefiles
----


![1](2191_1.gif)

## Resources

**Read or watch**:

* [Makefile](https://www.google.com/search?q=makefile)
* [Makefiletutorial](https://makefiletutorial.com/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What are`make`, Makefiles
* When, why and how to use Makefiles
* What are rules and how to set and use them
* What are explicit and implicit rules
* What are the most common / useful rules
* What are variables and how to set and use them
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* OS: Ubuntu 20.04 LTS
* Version of`gcc`: 9.3.0
* Version of`make`: GNU Make 4.2.1
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
## More Info

### Files

#### The following are very important steps

* In the following tasks, we are going to use[these files](https://github.com/hs-hq/0x1B.c). We want to compile these only.
* You can either create the files of the repository into your project folder (**makefiles**) and copy paste their content from github OR you can clone the**0x1B.c**repository into the**makefiles**folder.
* If you’re going to clone it, you should enter the**makefiles**folder and**inside this folder**delete the**.git**folder using this command`rm -rf .git`then move the files from this folder into the**makefiles**folder to test your work.

----
## Tasks
---
### 0. make -f 0-Makefile

Create your first Makefile.<!--plain-NL-->

Requirements:<!--plain-NL-->

- name of the executable: `school`
- rules: `all`

The `all` rule builds your executable
- The `all` rule builds your executable
- variables: none

- The `all` rule builds your executable

```
julien@ubuntu:~/Makefiles$ make -f 0-Makefile 
gcc main.c school.c -o school
julien@ubuntu:~/Makefiles$ ./school 
j#0000000000000000000000000000000000000
j#000000000000000000@Q**g00000000000000
j#0000000000000000*]++]4000000000000000
j#000000000000000k]++]++*N#000000000000
j#0000000000000*C+++]++]++]J*0000000000
j#00000000000@+]++qwwwp=]++++]*00000000
j#0000000000*+++]q#0000k+]+]++]4#000000
j#00000000*C+]+]w#0000*]+++]+]++0000000
j#0000we+]wW000***C++]++]+]++++40000000
j#000000000*C+]+]]+]++]++]++]+q#0000000
j#0000000*]+]+++++++]++]+++]+++J0000000
j#000000C++]=]+]+]+]++]++]+]+]+]=000000
j#00000k+]++]+++]+]++qwW0000000AgW00000
j#00000k++]++]+]+++qW#00000000000000000
j#00000A]++]++]++]++J**0000000000000000
j#000000e]++]+++]++]++]J000000000000000
j#0000000A]++]+]++]++]++000000000000000
j#000000000w]++]+]++]+qW#00000000000000
j#00000000000w]++++]*0##000000000000000
j#0000000000000Ag]+]++*0000000000000000
j#00000000000000000we]+]Q00000000000000
j#0000000000000@@+wgdA]+J00000000000000
j#0000000000000k?qwgdC=]4#0000000000000
j#00000000000000w]+]++qw#00000000000000
"!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
julien@ubuntu:~/Makefiles$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `makefiles`
- File: `0-Makefile`


---
### 1. make -f 1-Makefile

Requirements:<!--plain-NL-->

- name of the executable: `school`
- rules: `all`

The `all` rule builds your executable
- The `all` rule builds your executable
- variables: `CC`, `SRC`

`CC`: the compiler to be used
`SRC`: the `.c` files
- `CC`: the compiler to be used
- `SRC`: the `.c` files

- The `all` rule builds your executable

- `CC`: the compiler to be used
- `SRC`: the `.c` files

```
julien@ubuntu:~/Makefiles$ make -f 1-Makefile
gcc main.c school.c -o school
julien@ubuntu:~/Makefiles$ make -f 1-Makefile
gcc main.c school.c -o school
julien@ubuntu:~/Makefiles$

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `makefiles`
- File: `1-Makefile`


---
### 2. make -f 2-Makefile

Create your first useful Makefile.<!--plain-NL-->

Requirements:<!--plain-NL-->

- name of the executable: `school`
- rules: `all`

The `all` rule builds your executable
- The `all` rule builds your executable
- variables: `CC`, `SRC`, `OBJ`, `NAME`

`CC`: the compiler to be used
`SRC`: the `.c` files
`OBJ`: the `.o` files
`NAME`: the name of the executable
- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable
- The `all` rule should recompile only the updated source files
- You are not allowed to have a list of all the `.o` files

- The `all` rule builds your executable

- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable

```
julien@ubuntu:~/Makefiles$ make -f 2-Makefile
gcc    -c -o main.o main.c
gcc    -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ make -f 2-Makefile
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ echo "/* School */" >> main.c
julien@ubuntu:~/Makefiles$ make -f 2-Makefile
gcc    -c -o main.o main.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `makefiles`
- File: `2-Makefile`


---
### 3. make -f 3-Makefile

Requirements:<!--plain-NL-->

- name of the executable: `school`
- rules: `all`, `clean`, `oclean`, `fclean`, `re`

`all`: builds your executable
`clean`: deletes all Emacs and Vim temporary files along with the executable
`oclean`: deletes the object files
`fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
`re`: forces recompilation of all source files
- `all`: builds your executable
- `clean`: deletes all Emacs and Vim temporary files along with the executable
- `oclean`: deletes the object files
- `fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
- `re`: forces recompilation of all source files
- variables: `CC`, `SRC`, `OBJ`, `NAME`, `RM`

`CC`: the compiler to be used
`SRC`: the `.c` files
`OBJ`: the `.o` files
`NAME`: the name of the executable
`RM`: the program to delete files
- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable
- `RM`: the program to delete files
- The `all` rule should recompile only the updated source files
- The `clean`, `oclean`, `fclean`, `re` rules should never fail
- You are not allowed to have a list of all the `.o` files

- `all`: builds your executable
- `clean`: deletes all Emacs and Vim temporary files along with the executable
- `oclean`: deletes the object files
- `fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
- `re`: forces recompilation of all source files

- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable
- `RM`: the program to delete files

```
julien@ubuntu:~//Makefiles$ ls -1
0-Makefile
1-Makefile
2-Makefile
3-Makefile
school.c
main.c
main.c~
m.h
julien@ubuntu:~/Makefiles$ make -f 3-Makefile
gcc    -c -o main.o main.c
gcc    -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ make all -f 3-Makefile
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ ls -1
0-Makefile
1-Makefile
2-Makefile
3-Makefile
school
school.c
school.o
main.c
main.c~
main.o
m.h
julien@ubuntu:~/Makefiles$ make clean -f 3-Makefile 
rm -f *~ school
julien@ubuntu:~/Makefiles$ make oclean -f 3-Makefile 
rm -f main.o school.o
julien@ubuntu:~/Makefiles$ make all -f 3-Makefile
gcc    -c -o main.o main.c
gcc    -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ make fclean -f 3-Makefile 
rm -f *~ school
rm -f main.o school.o
julien@ubuntu:~/Makefiles$ make all -f 3-Makefile
gcc    -c -o main.o main.c
gcc    -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ make all -f 3-Makefile
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ make re -f 3-Makefile
rm -f main.o school.o
gcc    -c -o main.o main.c
gcc    -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `makefiles`
- File: `3-Makefile`


---
### 4. A complete Makefile

Requirements:<!--plain-NL-->

- name of the executable: `school`
- rules: `all`, `clean`, `fclean`, `oclean`, `re`

`all`: builds your executable
`clean`: deletes all Emacs and Vim temporary files along with the executable
`oclean`: deletes the object files
`fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
`re`: forces recompilation of all source files
- `all`: builds your executable
- `clean`: deletes all Emacs and Vim temporary files along with the executable
- `oclean`: deletes the object files
- `fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
- `re`: forces recompilation of all source files
- variables: `CC`, `SRC`, `OBJ`, `NAME`, `RM`, `CFLAGS`

`CC`: the compiler to be used
`SRC`: the `.c` files
`OBJ`: the `.o` files
`NAME`: the name of the executable
`RM`: the program to delete files
`CFLAGS`: your favorite compiler flags: `-Wall -Werror -Wextra -pedantic`
- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable
- `RM`: the program to delete files
- `CFLAGS`: your favorite compiler flags: `-Wall -Werror -Wextra -pedantic`
- The `all` rule should recompile only the updated source files
- The `clean`, `oclean`, `fclean`, `re` rules should never fail
- You are not allowed to have a list of all the `.o` files

- `all`: builds your executable
- `clean`: deletes all Emacs and Vim temporary files along with the executable
- `oclean`: deletes the object files
- `fclean`: deletes all Emacs and Vim temporary files, the executable, and the object files
- `re`: forces recompilation of all source files

- `CC`: the compiler to be used
- `SRC`: the `.c` files
- `OBJ`: the `.o` files
- `NAME`: the name of the executable
- `RM`: the program to delete files
- `CFLAGS`: your favorite compiler flags: `-Wall -Werror -Wextra -pedantic`

The <!--plain-NL-->`clean`<!--inline-NL-->, <!--plain-NL-->`oclean`<!--inline-NL-->, <!--plain-NL-->`fclean`<!--inline-NL-->, <!--plain-NL-->`re`<!--inline-NL--> rules should never fail<!--plain-NL-->

You are not allowed to have a list of all the <!--plain-NL-->`.o`<!--inline-NL--> files<!--plain-NL-->

```
julien@ubuntu:~/Makefiles$ make all -f 4-Makefile
gcc -Wall -Werror -Wextra -pedantic   -c -o main.o main.c
gcc -Wall -Werror -Wextra -pedantic   -c -o school.o school.c
gcc main.o school.o -o school
julien@ubuntu:~/Makefiles$ 

```

**Repo:**

- GitHub repository: `atlas-low_level_programming`
- Directory: `makefiles`
- File: `4-Makefile`