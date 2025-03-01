# Project 2175: Python - import & modules
----

* [Quiz](#quiz)
## Resources

**Read or watch**:

* [Modules](https://docs.python.org/3/tutorial/modules.html)
* [Command line arguments](https://docs.python.org/3/tutorial/stdlib.html#command-line-arguments)
* [Pycodestyle – Style Guide for Python Code](https://pypi.org/project/pycodestyle/)

**man or help**:

* `python3`
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* Why Python programming is awesome
* How to import functions from another file
* How to use imported functions
* How to create a module
* How to use the built-in function`dir()`
* How to prevent code in your script from being executed when imported
* How to use command line arguments with your Python programs
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 22.04 LTS using python3 (version 3.10.*)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the pycodestyle (version 2.7.*)
* All your files must be executable
* The length of your files will be tested using`wc`
**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What do these lines print?

``
```
>>> def my_function():
>>>     print("In my function")
>>> 
>>> my_function()
```

 * “In my function”

 * In my function

 * function my_function at …

 * Nothing

#### Question #1

What do these lines print?

``
```
>>> def my_function():
>>>     print("In my function")
>>> 
>>> my_function
```

 * “In my function”

 * In my function

 * function my_function at …

 * Nothing

#### Question #2

What do these lines print?

``
```
>>> def my_function(counter):
>>>     print("Counter: {}".format(counter))
>>> 
>>> my_function(12)
```

 * Counter: counter

 * Counter: c

 * Counter: 12

#### Question #3

What do these lines print?

``
```
>>> def my_function(counter=89):
>>>     print("Counter: {}".format(counter))
>>> 
>>> my_function(12)
```

 * Counter: 12

 * Counter: 89

 * Counter: 101

#### Question #4

What do these lines print?

``
```
>>> def my_function(counter=89):
>>>     print("Counter: {}".format(counter))
>>> 
>>> my_function()
```

 * Counter: 12

 * Counter: 89

 * Counter: 101

#### Question #5

What do these lines print?

``
```
>>> def my_function(counter=89):
>>>     return counter + 1
>>> 
>>> print(my_function())
```

 * 1

 * 89

 * 90

 * 891


----
## Tasks
---
### 0. Import a simple function from a simple file

Write a program that imports the function def add(a, b): from the file add_0.py and prints the result of the addition 1 + 2 = 3

- You have to use `print` function with string format to display integers
- You have to assign:


the value `1` to a variable called `a` 
the value `2` to a variable called `b`
and use those two variables as arguments when calling the functions `add` and `print`
- the value `1` to a variable called `a`
- the value `2` to a variable called `b`
- and use those two variables as arguments when calling the functions `add` and `print`
- `a` and `b` must be defined in 2 different lines: `a = 1` and another `b = 2`
- Your program should print: `&lt;a value&gt; + &lt;b value&gt; = &lt;add(a, b) value&gt;` followed with a new line
- You can only use the word `add_0` once in your code
- You are not allowed to use `*` for importing or `__import__`
- Your code should not be executed when imported - by using `__import__`, like the example below

- the value `1` to a variable called `a`
- the value `2` to a variable called `b`
- and use those two variables as arguments when calling the functions `add` and `print`

```
guillaume@ubuntu:~/$ cat add_0.py
#!/usr/bin/python3
def add(a, b):
    """My addition function

    Args:
        a: first integer
        b: second integer

    Returns:
        The return value. a + b
    """
    return (a + b)

guillaume@ubuntu:~/$ ./0-add.py
1 + 2 = 3
guillaume@ubuntu:~/$ cat 0-import_add.py
__import__("0-add")
guillaume@ubuntu:~/$ python3 0-import_add.py 
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `0-add.py`


---
### 1. My first toolbox!

Write a program that imports functions from the file calculator_1.py, does some Maths, and prints the result.

- Do not use the function `print` (with string format to display integers) more than 4 times
- You have to define:


the value `10` to a variable `a`
the value `5` to a variable `b`
and use those two variables only, as arguments when calling functions (including `print`)
- the value `10` to a variable `a`
- the value `5` to a variable `b`
- and use those two variables only, as arguments when calling functions (including `print`)
- `a` and `b` must be defined in 2 different lines: `a = 10` and another `b = 5`
- Your program should call each of the imported functions. See example below for format
- the word `calculator_1` should be used only once in your file
- You are not allowed to use `*` for importing or `__import__`
- Your code should not be executed when imported

- the value `10` to a variable `a`
- the value `5` to a variable `b`
- and use those two variables only, as arguments when calling functions (including `print`)

```
guillaume@ubuntu:~/$ cat calculator_1.py
#!/usr/bin/python3
def add(a, b):
    """My addition function

    Args:
        a: first integer
        b: second integer

    Returns:
        The return value. a + b
    """
    return (a + b)


def sub(a, b):
    """My subtraction function

    Args:
        a: first integer
        b: second integer

    Returns:
        The return value. a - b
    """
    return (a - b)


def mul(a, b):
    """My multiplication function

    Args:
        a: first integer
        b: second integer

    Returns:
        The return value. a * b
    """
    return (a * b)


def div(a, b):
    """My division function

    Args:
        a: first integer
        b: second integer

    Returns:
        The return value. a / b
    """
    return int(a / b)

guillaume@ubuntu:~/$ ./1-calculation.py
10 + 5 = 15
10 - 5 = 5
10 * 5 = 50
10 / 5 = 2
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `1-calculation.py`


---
### 2. How to make a script dynamic!

Write a program that prints the number of and the list of its arguments.

- The output should be:


Number of argument(s) followed by `argument` (if number is one) or `arguments` (otherwise), followed by
`:` (or `.` if no arguments were passed) followed by
a new line, followed by (if at least one argument),
one line per argument:


the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line
- Number of argument(s) followed by `argument` (if number is one) or `arguments` (otherwise), followed by
- `:` (or `.` if no arguments were passed) followed by
- a new line, followed by (if at least one argument),
- one line per argument:


the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line
- the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line
- Your code should not be executed when imported
- The number of elements of `argv` can be retrieved by using: `len(argv)`
- You do not have to fully understand lists yet, but imagine that `argv` can be used just like a C array: you can use an index to walk through it. There are other ways (which will be preferred for future project tasks), if you know them you can use them.

- Number of argument(s) followed by `argument` (if number is one) or `arguments` (otherwise), followed by
- `:` (or `.` if no arguments were passed) followed by
- a new line, followed by (if at least one argument),
- one line per argument:


the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line
- the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line

- the position of the argument (starting at `1`) followed by `:`, followed by the argument value and a new line

```
guillaume@ubuntu:~/$ ./2-args.py 
0 arguments.
guillaume@ubuntu:~/$ ./2-args.py Hello
1 argument:
1: Hello
guillaume@ubuntu:~/$ ./2-args.py Hello Welcome To The Best School
6 arguments:
1: Hello
2: Welcome
3: To
4: The
5: Best
6: School
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `2-args.py`


---
### 3. Infinite addition

Write a program that prints the result of the addition of all arguments

Last but not least, your program should also handle big numbers. And the good news is: if your program works for the above example, it will work for the following example:

- The output should be the result of the addition of all arguments, followed by a new line
- You can cast arguments into integers by using `int()` (you can assume that all arguments can be casted into integers)
- Your code should not be executed when imported

```
guillaume@ubuntu:~/$ ./3-infinite_add.py
0
guillaume@ubuntu:~/$ ./3-infinite_add.py 79 10
89
guillaume@ubuntu:~/$ ./3-infinite_add.py 79 10 -40 -300 89 
-162
guillaume@ubuntu:~/$ 

```

```
guillaume@ubuntu:~/$ ./3-infinite_add.py 1111111111111111111111111111111111111111111111111111111111112222222222222222222222222222222222223435467866765443534434222222254444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555666666666666666666666666666666777777777777777777777777777777888888888888888888888888888888899999999999999999999999990000000000000000000 11111111111111111111111111111111111111111111111111222222222222222222222222222333333333333333333334567788888899999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999
11111111111111111111111111111111111111111111111111222222222222222222222222222333333333333333333334568900000011111111111111111111111111111111111111111111111111112222222222222222222222222222222222223435467866765443534434222222254444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444444555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555666666666666666666666666666666777777777777777777777777777777888888888888888888888888888888899999999999999999999999989999999999999999999
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `3-infinite_add.py`


---
### 4. Who are you?

Write a program that prints all the names defined by the compiled module hidden_4.pyc (please download it locally in your sandbox using curl).

- This task must be done on the sandbox only
- File 4-hidden_discovery.py must be located on the folder /tmp/
- You should print one name per line, in alpha order
- You should print only names that do **not** start with `__`
- Your code should not be executed when imported

```
guillaume@ubuntu:/tmp$ curl -Lso "hidden_4.pyc" "https://github.com/hs-hq/0x02.py/raw/main/hidden_4.pyc"
guillaume@ubuntu:/tmp$ ./4-hidden_discovery.py | sort
my_secret_santa
print_hidden
print_school
guillaume@ubuntu:/tmp$ 

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `5-variable_load.py`


---
### 5. Everything can be imported

Write a program that imports the variable a from the file variable_load_5.py and prints its value.

- You are not allowed to use `*` for importing or `__import__`
- Your code should not be executed when imported

```
guillaume@ubuntu:~/$ cat variable_load_5.py
#!/usr/bin/python3
a = 98
"""Simple variable
"""

guillaume@ubuntu:~/$ ./5-variable_load.py
98
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-higher_level_programming`
- Directory: `python-import_modules`
- File: `5-variable_load.py`