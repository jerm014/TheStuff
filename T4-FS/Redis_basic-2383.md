# Project 2383: Redis basic
----


![1](2383_1.png)

## Resources

**Read or watch:**

* [Redis commands](https://redis.io/docs/latest/commands/)
* [Redis python client](https://redis-py.readthedocs.io/en/stable/)
* [How to Use Redis With Python](https://realpython.com/python-redis/)
* [Redis Crash Course Tutorial](https://www.youtube.com/watch?v=Hbt56gFj998)
## Learning Objectives

* Learn how to use redis for basic operations
* Learn how to use redis as a simple cache
## Requirements

* All of your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.9)
* All of your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* Your code should use the`pycodestyle`style (version 2.5)
* All your modules should have documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions and methods should have documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
* All your functions and coroutines must be type-annotated.
## Install Redis on Ubuntu 20.04

`
```
$ sudo apt-get -y install redis-server
$ pip3 install redis
$ sed -i "s/bind .*/bind 127.0.0.1/g" /etc/redis/redis.conf
```
## Use Redis in a container

Redis server is stopped by default - when you are starting a container, you should start it with:`service redis-server start`


----
## Tasks
---
### 0. Writing strings to Redis

Create a <!--plain-NL-->`Cache`<!--inline-NL--> class. In the <!--plain-NL-->`__init__`<!--inline-NL--> method, store an instance of the Redis client as a private variable named <!--plain-NL-->`_redis`<!--inline-NL--> (using <!--plain-NL-->`redis.Redis()`<!--inline-NL-->) and flush the instance using <!--plain-NL-->`flushdb`<!--inline-NL-->.<!--plain-NL-->

Create a <!--plain-NL-->`store`<!--inline-NL--> method that takes a <!--plain-NL-->`data`<!--inline-NL--> argument and returns a string. The method should generate a random key (e.g. using <!--plain-NL-->`uuid`<!--inline-NL-->), store the input data in Redis using the random key and return the key.<!--plain-NL-->

Type-annotate <!--plain-NL-->`store`<!--inline-NL--> correctly. Remember that <!--plain-NL-->`data`<!--inline-NL--> can be a <!--plain-NL-->`str`<!--inline-NL-->, <!--plain-NL-->`bytes`<!--inline-NL-->, <!--plain-NL-->`int`<!--inline-NL--> or <!--plain-NL-->`float`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
import redis

Cache = __import__('exercise').Cache

cache = Cache()

data = b"hello"
key = cache.store(data)
print(key)

local_redis = redis.Redis()
print(local_redis.get(key))

bob@dylan:~$ python3 main.py 
3a3e8231-b2f6-450d-8b0e-0f38f16e8ca2
b'hello'
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `0x0B_redis_basic`
- File: `exercise.py`


---
### 1. Reading from Redis and recovering original type

Redis only allows to store string, bytes and numbers (and lists thereof). Whatever you store as single elements, it will be returned as a byte string. Hence if you store <!--plain-NL-->`"a"`<!--inline-NL--> as a UTF-8 string, it will be returned as <!--plain-NL-->`b"a"`<!--inline-NL--> when retrieved from the server.<!--plain-NL-->

In this exercise we will create a <!--plain-NL-->`get`<!--inline-NL--> method that take a <!--plain-NL-->`key`<!--inline-NL--> string argument and an optional <!--plain-NL-->`Callable`<!--inline-NL--> argument named <!--plain-NL-->`fn`<!--inline-NL-->. This callable will be used to convert the data back to the desired format.<!--plain-NL-->

Remember to conserve the original <!--plain-NL-->`Redis.get`<!--inline-NL--> behavior if the key does not exist.<!--plain-NL-->

Also, implement 2 new methods: <!--plain-NL-->`get_str`<!--inline-NL--> and <!--plain-NL-->`get_int`<!--inline-NL--> that will automatically parametrize <!--plain-NL-->`Cache.get`<!--inline-NL--> with the correct conversion function.<!--plain-NL-->

The following code should not raise:<!--plain-NL-->

```
cache = Cache()

TEST_CASES = {
    b"foo": None,
    123: int,
    "bar": lambda d: d.decode("utf-8")
}

for value, fn in TEST_CASES.items():
    key = cache.store(value)
    assert cache.get(key, fn=fn) == value

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `0x0B_redis_basic`
- File: `exercise.py`


---
### 2. Incrementing values

Familiarize yourself with the <!--plain-NL-->`INCR`<!--inline-NL--> command and its python equivalent.<!--plain-NL-->

In this task, we will implement a system to count how many times methods of the <!--plain-NL-->`Cache`<!--inline-NL--> class are called.<!--plain-NL-->

Above <!--plain-NL-->`Cache`<!--inline-NL--> define a <!--plain-NL-->`count_calls`<!--inline-NL--> decorator that takes a single <!--plain-NL-->`method`<!--inline-NL--> <!--plain-NL-->`Callable`<!--inline-NL--> argument and returns a <!--plain-NL-->`Callable`<!--inline-NL-->.<!--plain-NL-->

As a key, use the qualified name of <!--plain-NL-->`method`<!--inline-NL--> using the <!--plain-NL-->`__qualname__`<!--inline-NL--> dunder method.<!--plain-NL-->

Create and return function that increments the count for that key every time the method is called and returns the value returned by the original method.<!--plain-NL-->

Remember that the first argument of the wrapped function will be <!--plain-NL-->`self`<!--inline-NL--> which is the instance itself, which lets you access the Redis instance.<!--plain-NL-->

Protip: when defining a decorator it is useful to use <!--plain-->`functool.wraps`<!--inline--> to conserve the original function’s name, docstring, etc. Make sure you use it as described <!--plain-->[here](https://docs.python.org/3.7/library/functools.html#functools.wraps) <!--link-->.<!--plain-->

Decorate <!--plain-NL-->`Cache.store`<!--inline-NL--> with <!--plain-NL-->`count_calls`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
""" Main file """

Cache = __import__('exercise').Cache

cache = Cache()

cache.store(b"first")
print(cache.get(cache.store.__qualname__))

cache.store(b"second")
cache.store(b"third")
print(cache.get(cache.store.__qualname__))

bob@dylan:~$ ./main.py
b'1'
b'3'
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `0x0B_redis_basic`
- File: `exercise.py`


---
### 3. Storing lists

Familiarize yourself with redis commands <!--plain-NL-->`RPUSH`<!--inline-NL-->, <!--plain-NL-->`LPUSH`<!--inline-NL-->, <!--plain-NL-->`LRANGE`<!--inline-NL-->, etc.<!--plain-NL-->

In this task, we will define a <!--plain-NL-->`call_history`<!--inline-NL--> decorator to store the history of inputs and outputs for a particular function.<!--plain-NL-->

Everytime the original function will be called, we will add its input parameters to one list in redis, and store its output into another list.<!--plain-NL-->

In <!--plain-NL-->`call_history`<!--inline-NL-->, use the decorated function’s qualified name and append <!--plain-NL-->`":inputs"`<!--inline-NL--> and <!--plain-NL-->`":outputs"`<!--inline-NL--> to create input and output list keys, respectively.<!--plain-NL-->

`call_history`<!--inline-NL--> has a single parameter named <!--plain-NL-->`method`<!--inline-NL--> that is a <!--plain-NL-->`Callable`<!--inline-NL--> and returns a <!--plain-NL-->`Callable`<!--inline-NL-->.<!--plain-NL-->

In the new function that the decorator will return, use <!--plain-NL-->`rpush`<!--inline-NL--> to append the input arguments. Remember that Redis can only store strings, bytes and numbers. Therefore, we can simply use <!--plain-NL-->`str(args)`<!--inline-NL--> to normalize. We can ignore potential <!--plain-NL-->`kwargs`<!--inline-NL--> for now.<!--plain-NL-->

Execute the wrapped function to retrieve the output. Store the output using <!--plain-NL-->`rpush`<!--inline-NL--> in the <!--plain-NL-->`"...:outputs"`<!--inline-NL--> list, then return the output.<!--plain-NL-->

Decorate <!--plain-NL-->`Cache.store`<!--inline-NL--> with <!--plain-NL-->`call_history`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
""" Main file """

Cache = __import__('exercise').Cache

cache = Cache()

s1 = cache.store("first")
print(s1)
s2 = cache.store("secont")
print(s2)
s3 = cache.store("third")
print(s3)

inputs = cache._redis.lrange("{}:inputs".format(cache.store.__qualname__), 0, -1)
outputs = cache._redis.lrange("{}:outputs".format(cache.store.__qualname__), 0, -1)

print("inputs: {}".format(inputs))
print("outputs: {}".format(outputs))

bob@dylan:~$ ./main.py
04f8dcaa-d354-4221-87f3-4923393a25ad
a160a8a8-06dc-4934-8e95-df0cb839644b
15a8fd87-1f55-4059-86aa-9d1a0d4f2aea
inputs: [b"('first',)", b"('secont',)", b"('third',)"]
outputs: [b'04f8dcaa-d354-4221-87f3-4923393a25ad', b'a160a8a8-06dc-4934-8e95-df0cb839644b', b'15a8fd87-1f55-4059-86aa-9d1a0d4f2aea']
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `0x0B_redis_basic`
- File: `exercise.py`


---
### 4. Retrieving lists

In this tasks, we will implement a <!--plain-NL-->`replay`<!--inline-NL--> function to display the history of calls of a particular function.<!--plain-NL-->

Use keys generated in previous tasks to generate the following output:<!--plain-NL-->

```
>>> cache = Cache()
>>> cache.store("foo")
>>> cache.store("bar")
>>> cache.store(42)
>>> replay(cache.store)
Cache.store was called 3 times:
Cache.store(*('foo',)) -> 13bf32a9-a249-4664-95fc-b1062db2038f
Cache.store(*('bar',)) -> dcddd00c-4219-4dd7-8877-66afbe8e7df8
Cache.store(*(42,)) -> 5e752f2b-ecd8-4925-a3ce-e2efdee08d20

```

Tip: use <!--plain-NL-->`lrange`<!--inline-NL--> and <!--plain-NL-->`zip`<!--inline-NL--> to loop over inputs and outputs.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `0x0B_redis_basic`
- File: `exercise.py`