# Project 2342: Python - Variable Annotations
----


*For this project, we expect you to look at this concept:*

* [Advanced Python](/concepts/950)

![1](2342_1.png)

## Resources

**Read or watch**:

* [Python 3 typing documentation](https://docs.python.org/3/library/typing.html)
* [MyPy cheat sheet](https://mypy.readthedocs.io/en/latest/cheat_sheet_py3.html)
## Learning Objectives

### General

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* Type annotations in Python 3
* How you can use type annotations to specify function signatures and variable types
* Duck typing
* How to validate your code with`mypy`
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.5.)
* All your files must be executable
* The length of your files will be tested using`wc`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

----
## Tasks
---
### 0. Basic annotations - add

Write a type-annotated function <!--plain-NL-->`add`<!--inline-NL--> that takes a float <!--plain-NL-->`a`<!--inline-NL--> and a float <!--plain-NL-->`b`<!--inline-NL--> as arguments and returns their sum as a float. <!--plain-NL-->

```
bob@dylan:~$ cat 0-main.py
#!/usr/bin/env python3
add = __import__('0-add').add

print(add(1.11, 2.22) == 1.11 + 2.22)
print(add.__annotations__)

bob@dylan:~$ ./0-main.py
True
{'a':  <class 'float'>, 'b': <class 'float'>, 'return': <class 'float'>}

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `0-add.py`


---
### 1. Basic annotations - concat

Write a type-annotated function <!--plain-NL-->`concat`<!--inline-NL--> that takes a string <!--plain-NL-->`str1`<!--inline-NL--> and a string <!--plain-NL-->`str2`<!--inline-NL--> as arguments and returns a concatenated string<!--plain-NL-->

```
bob@dylan:~$ cat 1-main.py
#!/usr/bin/env python3
concat = __import__('1-concat').concat

str1 = "egg"
str2 = "shell"

print(concat(str1, str2) == "{}{}".format(str1, str2))
print(concat.__annotations__)

bob@dylan:~$ ./1-main.py
True
{'str1': <class 'str'>, 'str2': <class 'str'>, 'return': <class 'str'>}

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `1-concat.py`


---
### 2. Basic annotations - floor

Write a type-annotated function <!--plain-NL-->`floor`<!--inline-NL--> which takes a float <!--plain-NL-->`n`<!--inline-NL--> as argument and returns the floor of the float.<!--plain-NL-->

```
bob@dylan:~$ cat 2-main.py
#!/usr/bin/env python3

import math

floor = __import__('2-floor').floor

ans = floor(3.14)

print(ans == math.floor(3.14))
print(floor.__annotations__)
print("floor(3.14) returns {}, which is a {}".format(ans, type(ans)))

bob@dylan:~$ ./2-main.py
True
{'n': <class 'float'>, 'return': <class 'int'>}
floor(3.14) returns 3, which is a <class 'int'>

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `2-floor.py`


---
### 3. Basic annotations - to string

Write a type-annotated function <!--plain-NL-->`to_str`<!--inline-NL--> that takes a float <!--plain-NL-->`n`<!--inline-NL--> as argument and returns the string representation of the float.<!--plain-NL-->

```
bob@dylan:~$ cat 3-main.py
#!/usr/bin/env python3
to_str = __import__('3-to_str').to_str

pi_str = to_str(3.14)
print(pi_str == str(3.14))
print(to_str.__annotations__)
print("to_str(3.14) returns {} which is a {}".format(pi_str, type(pi_str)))

bob@dylan:~$ ./3-main.py
True
{'n': <class 'float'>, 'return': <class 'str'>}
to_str(3.14) returns 3.14, which is a <class 'str'>

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `3-to_str.py`


---
### 4. Define variables

Define and annotate the following variables with the specified values:<!--plain-NL-->

- `a`, an integer with a value of 1
- `pi`, a float with a value of 3.14
- `i_understand_annotations`, a boolean with a value of True
- `school`, a string with a value of “Holberton”

```
bob@dylan:~$ cat 4-main.py
#!/usr/bin/env python3

a = __import__('4-define_variables').a
pi = __import__('4-define_variables').pi
i_understand_annotations = __import__('4-define_variables').i_understand_annotations
school = __import__('4-define_variables').school

print("a is a {} with a value of {}".format(type(a), a))
print("pi is a {} with a value of {}".format(type(pi), pi))
print("i_understand_annotations is a {} with a value of {}".format(type(i_understand_annotations), i_understand_annotations))
print("school is a {} with a value of {}".format(type(school), school))

bob@dylan:~$ ./4-main.py
a is a <class 'int'> with a value of 1
pi is a <class 'float'> with a value of 3.14
i_understand_annotations is a <class 'bool'> with a value of True
school is a <class 'str'> with a value of Holberton

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `4-define_variables.py`


---
### 5. Complex types - list of floats

Write a type-annotated function <!--plain-NL-->`sum_list`<!--inline-NL--> which takes a list <!--plain-NL-->`input_list`<!--inline-NL--> of floats as argument and returns their sum as a float.<!--plain-NL-->

```
bob@dylan:~$ cat 5-main.py
#!/usr/bin/env python3

sum_list = __import__('5-sum_list').sum_list

floats = [3.14, 1.11, 2.22]
floats_sum = sum_list(floats)
print(floats_sum == sum(floats))
print(sum_list.__annotations__)
print("sum_list(floats) returns {} which is a {}".format(floats_sum, type(floats_sum)))

bob@dylan:~$ ./5-main.py
True
{'input_list': typing.List[float], 'return': <class 'float'>}
sum_list(floats) returns 6.470000000000001 which is a <class 'float'>

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `5-sum_list.py`


---
### 6. Complex types - mixed list

Write a type-annotated function <!--plain-NL-->`sum_mixed_list`<!--inline-NL--> which takes a list <!--plain-NL-->`mxd_lst`<!--inline-NL--> of integers and floats and returns their sum as a float.<!--plain-NL-->

```
bob@dylan:~$ cat 6-main.py
#!/usr/bin/env python3

sum_mixed_list = __import__('6-sum_mixed_list').sum_mixed_list

print(sum_mixed_list.__annotations__)
mixed = [5, 4, 3.14, 666, 0.99]
ans = sum_mixed_list(mixed)
print(ans == sum(mixed))
print("sum_mixed_list(mixed) returns {} which is a {}".format(ans, type(ans)))

bob@dylan:~$ ./6-main.py
{'mxd_lst': typing.List[typing.Union[int, float]], 'return': <class 'float'>}
True
sum_mixed_list(mixed) returns 679.13 which is a <class 'float'>

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `6-sum_mixed_list.py`


---
### 7. Complex types - string and int/float to tuple

Write a type-annotated function <!--plain-NL-->`to_kv`<!--inline-NL--> that takes a string <!--plain-NL-->`k`<!--inline-NL--> and an int OR float <!--plain-NL-->`v`<!--inline-NL--> as arguments and returns a tuple. The first element of the tuple is the string <!--plain-NL-->`k`<!--inline-NL-->. The second element is the square of the int/float <!--plain-NL-->`v`<!--inline-NL--> and should be annotated as a float.<!--plain-NL-->

```
bob@dylan:~$ cat 7-main.py
#!/usr/bin/env python3

to_kv = __import__('7-to_kv').to_kv

print(to_kv.__annotations__)
print(to_kv("eggs", 3))
print(to_kv("school", 0.02))

bob@dylan:~$ ./7-main.py
{'k': <class 'str'>, 'v': typing.Union[int, float], 'return': typing.Tuple[str, float]}
('eggs', 9)
('school', 0.0004)

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `7-to_kv.py`


---
### 8. Complex types - functions

Write a type-annotated function <!--plain-NL-->`make_multiplier`<!--inline-NL--> that takes a float <!--plain-NL-->`multiplier`<!--inline-NL--> as argument and returns a function that multiplies a float by <!--plain-NL-->`multiplier`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat 8-main.py
#!/usr/bin/env python3

make_multiplier = __import__('8-make_multiplier').make_multiplier
print(make_multiplier.__annotations__)
fun = make_multiplier(2.22)
print("{}".format(fun(2.22)))

bob@dylan:~$ ./8-main.py
{'multiplier': <class 'float'>, 'return': typing.Callable[[float], float]}
4.928400000000001

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `8-make_multiplier.py`


---
### 9. Let's duck type an iterable object

Annotate the below function’s parameters and return values with the appropriate types<!--plain-NL-->

```
def element_length(lst):
    return [(i, len(i)) for i in lst]

```

```
bob@dylan:~$ cat 9-main.py 
#!/usr/bin/env python3

element_length =  __import__('9-element_length').element_length

print(element_length.__annotations__)

bob@dylan:~$ ./9-main.py 
{'lst': typing.Iterable[typing.Sequence], 'return': typing.List[typing.Tuple[typing.Sequence, int]]}

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `python_variable_annotations`
- File: `9-element_length.py`