# Project 2215: C - ELF: readelf
----


## Resources

**Read or watch**:

* [ELF Wikipedia](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format)
* [ELF: Understanding and Analysis](https://linux-audit.com/elf-binaries-on-linux-understanding-and-analysis/)
* [Executable and Linkable Format (ELF)](https://www.cs.cmu.edu/afs/cs/academic/class/15213-f00/docs/elf.pdf)

**man or help**:

* `elf (5)`
* `readelf (1)`
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What is the ELF format
* What kind of files are in the ELF format
* What are the different parts that constitute an ELF file
* What information are present in the file header
* What information are present in the sections header table
* What information are present in the program header table
* How to parse an ELF file using C structures
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be compiled on Ubuntu 14.04 LTS
* Your C programs and functions will be compiled with`gcc 4.8.4`using the flags`-Wall``-Werror``-Wextra``and -pedantic`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`Betty`style. It will be checked using[betty-style.pl](https://github.com/hs-hq/Betty/blob/master/betty-style.pl)and[betty-doc.pl](https://github.com/hs-hq/Betty/blob/master/betty-doc.pl)
* You are not allowed to have more than 5 functions per file
* All your header files should be include guarded
### Betty Compliance

* All the C source files in your directory and subdirectories must be Betty-compliant
### Allowed Functions and System Calls

* Unless specified otherwise, you are allowed to use the C standard library
* You’re not allowed to use`system`(3)
* You’re not allowed to use`exec*`(2 and 3)
### Tests

* Your program must be able to handle both 32-bit and 64-bit ELF files
* Your program must be able to handle both little and big endian ELF files
* Your program must be able to handle all types of ELF files
## More Info

### Extra Reading

Check out`/usr/include/elf.h`

**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What does`ELF`stand for?

 * Executable Linux File

 * Executable and Linkable Format

 * A type of supernatural being in Germanic mythology and folklore

 * Extensible Linking Format

#### Question #1

What sequence constitutes the ELF magic number?

 * 0x00 0x45 0x4c 0x46

 * 0x7f 0x45 0x4c 0x46 0x00

 * 0x7f 0x45 0x4c 0x46

 * 0x7f 0x46 0x45 0x4c

#### Question #2

Which of the following files are in the ELF format?

 * Object file`.o`compiled with`gcc`

 * Executable Python script

 * Object file`.o`compiled with`g++`

 * Shared library`.so`

 * Static library`.a`

 * Compiled Python file`.pyc`

 * Executable file linked with`ld`

 * Core dump

#### Question #3

Which of the following parts will inevitably be present in an ELF file?

 * The file header

 * The program header table

 * The section header table

 * The symbol table

#### Question #4

An Address in an ELF file is always stored on 64 bits

 * True

 * False

#### Question #5

An Offset in an ELF file is stored either on 32 bits or on 64 bits

 * True

 * False

#### Question #6

The size of a program header table entry can differ from other program header table entries

 * True

 * False

#### Question #7

The size of a section is the same for all the sections

 * True

 * False

#### Question #8

An executable file won’t have the same file header format than an object file

 * True

 * False

#### Question #9

An object file can have multiple string table sections

 * True

 * False


----
## Tasks
---
### 0. ELF file header

Write a program that displays the information contained in the <!--plain-NL-->`ELF file header`<!--inline-NL--> of an <!--plain-NL-->`ELF`<!--inline-NL--> file.<!--plain-NL-->

- Usage: `0-hreadelf elf_filename`
- Your standard output, error output and status should be the exact same as `readelf -W -h`

Your makefile must define the rule <!--plain-NL-->`0-hreadelf`<!--inline-NL--> and compile the needed sources to form the executable <!--plain-NL-->`0-hreadelf`<!--inline-NL-->

```
alex@~/readelf$ make 0-hreadelf
[...]
alex@~/readelf$ ./0-hreadelf ubuntu64
ELF Header:
  Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00 
  Class:                             ELF64
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              EXEC (Executable file)
  Machine:                           Advanced Micro Devices X86-64
  Version:                           0x1
  Entry point address:               0x400600
  Start of program headers:          64 (bytes into file)
  Start of section headers:          6936 (bytes into file)
  Flags:                             0x0
  Size of this header:               64 (bytes)
  Size of program headers:           56 (bytes)
  Number of program headers:         9
  Size of section headers:           64 (bytes)
  Number of section headers:         31
  Section header string table index: 28
alex@~/readelf$ 
alex@~/readelf$ ./0-hreadelf netbsd32
ELF Header:
  Magic:   7f 45 4c 46 01 01 01 02 00 00 00 00 00 00 00 00 
  Class:                             ELF32
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - NetBSD
  ABI Version:                       0
  Type:                              EXEC (Executable file)
  Machine:                           Intel 80386
  Version:                           0x1
  Entry point address:               0x80484c0
  Start of program headers:          52 (bytes into file)
  Start of section headers:          2752 (bytes into file)
  Flags:                             0x0
  Size of this header:               52 (bytes)
  Size of program headers:           32 (bytes)
  Number of program headers:         6
  Size of section headers:           40 (bytes)
  Number of section headers:         24
  Section header string table index: 21
alex@~/readelf$ 
alex@~/readelf$ ./0-hreadelf sparcbigendian32 
ELF Header:
  Magic:   7f 45 4c 46 01 02 01 00 00 00 00 00 00 00 00 00 
  Class:                             ELF32
  Data:                              2's complement, big endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              EXEC (Executable file)
  Machine:                           Sparc
  Version:                           0x1
  Entry point address:               0x10d20
  Start of program headers:          52 (bytes into file)
  Start of section headers:          84560 (bytes into file)
  Flags:                             0x0
  Size of this header:               52 (bytes)
  Size of program headers:           32 (bytes)
  Number of program headers:         6
  Size of section headers:           40 (bytes)
  Number of section headers:         24
  Section header string table index: 23
alex@~/readelf$ 

```

**Repo:**

- GitHub repository: `atlas-system_linux`
- Directory: `readelf`
- File: `Makefile`