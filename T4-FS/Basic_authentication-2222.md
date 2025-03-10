# Project 2222: Basic authentication
----

## Background Context

In this project, you will learn what the authentication process means and implement a**Basic Authentication**on a simple API.

In the industry, you should**not**implement your own Basic authentication system and use a module or framework that doing it for you (like in Python-Flask:[Flask-HTTPAuth](https://flask-httpauth.readthedocs.io/en/latest/)). Here, for the learning purpose, we will walk through each step of this mechanism to understand it by doing.

![1](2222_1.png)

## Resources

**Read or watch**:

* [REST API Authentication Mechanisms](https://www.youtube.com/watch?v=501dpx2IjGY)
* [Base64 in Python](https://docs.python.org/3.9/library/base64.html)
* [HTTP header Authorization](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization)
* [Flask](https://palletsprojects.com/projects/flask/)
* [Base64 - concept](https://en.wikipedia.org/wiki/Base64)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What authentication means
* What Base64 is
* How to encode a string in Base64
* What Basic authentication means
* How to send the Authorization header
## Requirements

### Python Scripts

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.5)
* All your files must be executable
* The length of your files will be tested using`wc`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it�s a real sentence explaining what�s the purpose of the module, class or method (the length of it will be verified)

----
## Tasks
---
### 0. Simple-basic-API

Download and start your project from this <!--plain-->[archive.zip](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2020/11/ec2f874b061bd3a2915949f081f4f5f055104f20.zip?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20250303%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20250303T204335Z&X-Amz-Expires=345600&X-Amz-SignedHeaders=host&X-Amz-Signature=d61a5d3bf1e08a16469942c47dc3bb3f9aeb4bf4d70942d4eb6ccada17bba61e) <!--link-->

In this archive, you will find a simple API with one model: <!--plain-NL-->`User`<!--inline-NL-->. Storage of these users is done via a serialization/deserialization in files.<!--plain-NL-->

```
bob@dylan:~$ pip3 install -r requirements.txt
...
bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Serving Flask app "app" (lazy loading)
...
bob@dylan:~$

```

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/status HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 16
< Access-Control-Allow-Origin: *
< Server: Werkzeug/1.0.1 Python/3.7.5
< Date: Mon, 18 May 2020 20:29:21 GMT
< 
{"status":"OK"}
* Closing connection 0
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`


---
### 1. Error handler: Unauthorized

What the HTTP status code for a request unauthorized? <!--plain-NL-->`401`<!--inline-NL--> of course!<!--plain-NL-->

Edit <!--plain-NL-->`api/v1/app.py`<!--inline-NL-->:<!--plain-NL-->

- Add a new error handler for this status code, the response must be:


a JSON: `{"error": "Unauthorized"}`
status code `401`
you must use `jsonify` from Flask
- a JSON: `{"error": "Unauthorized"}`
- status code `401`
- you must use `jsonify` from Flask

- a JSON: `{"error": "Unauthorized"}`
- status code `401`
- you must use `jsonify` from Flask

For testing this new error handler, add a new endpoint in <!--plain-NL-->`api/v1/views/index.py`<!--inline-NL-->:<!--plain-NL-->

- Route: `GET /api/v1/unauthorized`
- This endpoint must raise a 401 error by using `abort` - Custom Error Pages

By calling <!--plain-NL-->`abort(401)`<!--inline-NL-->, the error handler for 401 will be executed.<!--plain-NL-->

In the first terminal:<!--plain-NL-->

```
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

In a second terminal:<!--plain-NL-->

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/unauthorized"
{
  "error": "Unauthorized"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/unauthorized" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/unauthorized HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 401 UNAUTHORIZED
< Content-Type: application/json
< Content-Length: 30
< Server: Werkzeug/0.12.1 Python/3.4.3
< Date: Sun, 24 Sep 2017 22:50:40 GMT
< 
{
  "error": "Unauthorized"
}
* Closing connection 0
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/app.py, api/v1/views/index.py`


---
### 2. Error handler: Forbidden

What the HTTP status code for a request where the user is authenticate but not allowed to access to a resource? <!--plain-NL-->`403`<!--inline-NL--> of course!<!--plain-NL-->

Edit <!--plain-NL-->`api/v1/app.py`<!--inline-NL-->:<!--plain-NL-->

- Add a new error handler for this status code, the response must be:


a JSON: `{"error": "Forbidden"}`
status code `403`
you must use `jsonify` from Flask
- a JSON: `{"error": "Forbidden"}`
- status code `403`
- you must use `jsonify` from Flask

- a JSON: `{"error": "Forbidden"}`
- status code `403`
- you must use `jsonify` from Flask

For testing this new error handler, add a new endpoint in <!--plain-NL-->`api/v1/views/index.py`<!--inline-NL-->:<!--plain-NL-->

- Route: `GET /api/v1/forbidden`
- This endpoint must raise a 403 error by using `abort` - Custom Error Pages

By calling <!--plain-NL-->`abort(403)`<!--inline-NL-->, the error handler for 403 will be executed.<!--plain-NL-->

In the first terminal:<!--plain-NL-->

```
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

In a second terminal:<!--plain-NL-->

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/forbidden"
{
  "error": "Forbidden"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/forbidden" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/forbidden HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 403 FORBIDDEN
< Content-Type: application/json
< Content-Length: 27
< Server: Werkzeug/0.12.1 Python/3.4.3
< Date: Sun, 24 Sep 2017 22:54:22 GMT
< 
{
  "error": "Forbidden"
}
* Closing connection 0
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/app.py, api/v1/views/index.py`


---
### 3. Auth class

Now you will create a class to manage the API authentication.<!--plain-NL-->

- Create a folder `api/v1/auth`
- Create an empty file `api/v1/auth/__init__.py`
- Create the class `Auth`:


in the file `api/v1/auth/auth.py`
import `request` from `flask`
class name `Auth`
public method `def require_auth(self, path: str, excluded_paths: List[str]) -&gt; bool:` that returns `False` - `path` and `excluded_paths` will be used later, now, you don�t need to take care of them
public method `def authorization_header(self, request=None) -&gt; str:` that returns `None` - `request` will be the Flask request object
public method `def current_user(self, request=None) -&gt; TypeVar('User'):` that returns `None` - `request` will be the Flask request object
- in the file `api/v1/auth/auth.py`
- import `request` from `flask`
- class name `Auth`
- public method `def require_auth(self, path: str, excluded_paths: List[str]) -&gt; bool:` that returns `False` - `path` and `excluded_paths` will be used later, now, you don�t need to take care of them
- public method `def authorization_header(self, request=None) -&gt; str:` that returns `None` - `request` will be the Flask request object
- public method `def current_user(self, request=None) -&gt; TypeVar('User'):` that returns `None` - `request` will be the Flask request object

- in the file `api/v1/auth/auth.py`
- import `request` from `flask`
- class name `Auth`
- public method `def require_auth(self, path: str, excluded_paths: List[str]) -&gt; bool:` that returns `False` - `path` and `excluded_paths` will be used later, now, you don�t need to take care of them
- public method `def authorization_header(self, request=None) -&gt; str:` that returns `None` - `request` will be the Flask request object
- public method `def current_user(self, request=None) -&gt; TypeVar('User'):` that returns `None` - `request` will be the Flask request object

This class is the template for all authentication system you will implement.<!--plain-NL-->

```
bob@dylan:~$ cat main_0.py
#!/usr/bin/env python3
""" Main 0
"""
from api.v1.auth.auth import Auth

a = Auth()

print(a.require_auth("/api/v1/status/", ["/api/v1/status/"]))
print(a.authorization_header())
print(a.current_user())

bob@dylan:~$ 
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_0.py
False
None
None
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth, api/v1/auth/__init__.py, api/v1/auth/auth.py`


---
### 4. Define which routes don't need authentication

Update the method <!--plain-NL-->`def require_auth(self, path: str, excluded_paths: List[str]) -> bool:`<!--inline-NL--> in <!--plain-NL-->`Auth`<!--inline-NL--> that returns <!--plain-NL-->`True`<!--inline-NL--> if the <!--plain-NL-->`path`<!--inline-NL--> is not in the list of strings <!--plain-NL-->`excluded_paths`<!--inline-NL-->:<!--plain-NL-->

- Returns `True` if `path` is `None`
- Returns `True` if `excluded_paths` is `None` or empty
- Returns `False` if `path` is in `excluded_paths`
- You can assume `excluded_paths` contains string path always ending by a `/`
- This method must be slash tolerant: `path=/api/v1/status` and `path=/api/v1/status/` must be returned `False` if `excluded_paths` contains `/api/v1/status/`

```
bob@dylan:~$ cat main_1.py
#!/usr/bin/env python3
""" Main 1
"""
from api.v1.auth.auth import Auth

a = Auth()

print(a.require_auth(None, None))
print(a.require_auth(None, []))
print(a.require_auth("/api/v1/status/", []))
print(a.require_auth("/api/v1/status/", ["/api/v1/status/"]))
print(a.require_auth("/api/v1/status", ["/api/v1/status/"]))
print(a.require_auth("/api/v1/users", ["/api/v1/status/"]))
print(a.require_auth("/api/v1/users", ["/api/v1/status/", "/api/v1/stats"]))

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_1.py
True
True
True
False
False
True
True
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/auth.py`


---
### 5. Request validation!

Now you will validate all requests to secure the API:<!--plain-NL-->

Update the method <!--plain-NL-->`def authorization_header(self, request=None) -> str:`<!--inline-NL--> in <!--plain-NL-->`api/v1/auth/auth.py`<!--inline-NL-->:<!--plain-NL-->

- If `request` is `None`, returns `None`
- If `request` doesn�t contain the header key `Authorization`, returns `None`
- Otherwise, return the value of the header request `Authorization`

Update the file <!--plain-NL-->`api/v1/app.py`<!--inline-NL-->:<!--plain-NL-->

- Create a variable `auth` initialized to `None` after the `CORS` definition
- Based on the environment variable `AUTH_TYPE`, load and assign the right instance of authentication to `auth`

if `auth`:


import `Auth` from `api.v1.auth.auth`
create an instance of `Auth` and assign it to the variable `auth`
- if `auth`:


import `Auth` from `api.v1.auth.auth`
create an instance of `Auth` and assign it to the variable `auth`
- import `Auth` from `api.v1.auth.auth`
- create an instance of `Auth` and assign it to the variable `auth`

- if `auth`:


import `Auth` from `api.v1.auth.auth`
create an instance of `Auth` and assign it to the variable `auth`
- import `Auth` from `api.v1.auth.auth`
- create an instance of `Auth` and assign it to the variable `auth`

- import `Auth` from `api.v1.auth.auth`
- create an instance of `Auth` and assign it to the variable `auth`

Now the biggest piece is the filtering of each request. For that you will use the Flask method <!--plain-->[before_request](https://flask.palletsprojects.com/en/stable/api/) <!--link-->

- Add a method in `api/v1/app.py` to handler `before_request`

if `auth` is `None`, do nothing
if `request.path` is not part of this list `['/api/v1/status/', '/api/v1/unauthorized/', '/api/v1/forbidden/']`, do nothing - you must use the method `require_auth` from the `auth` instance
if `auth.authorization_header(request)` returns `None`, raise the error `401` - you must use `abort`
if `auth.current_user(request)` returns `None`, raise the error `403` - you must use `abort`
- if `auth` is `None`, do nothing
- if `request.path` is not part of this list `['/api/v1/status/', '/api/v1/unauthorized/', '/api/v1/forbidden/']`, do nothing - you must use the method `require_auth` from the `auth` instance
- if `auth.authorization_header(request)` returns `None`, raise the error `401` - you must use `abort`
- if `auth.current_user(request)` returns `None`, raise the error `403` - you must use `abort`

- if `auth` is `None`, do nothing
- if `request.path` is not part of this list `['/api/v1/status/', '/api/v1/unauthorized/', '/api/v1/forbidden/']`, do nothing - you must use the method `require_auth` from the `auth` instance
- if `auth.authorization_header(request)` returns `None`, raise the error `401` - you must use `abort`
- if `auth.current_user(request)` returns `None`, raise the error `403` - you must use `abort`

In the first terminal:<!--plain-NL-->

```
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 AUTH_TYPE=auth python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

In a second terminal:<!--plain-NL-->

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status"
{
  "status": "OK"
}
bob@dylan:~$ 
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status/"
{
  "status": "OK"
}
bob@dylan:~$ 
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users"
{
  "error": "Unauthorized"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Test"
{
  "error": "Forbidden"
}
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/app.py, api/v1/auth/auth.py`


---
### 6. Basic auth

Create a class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that inherits from <!--plain-NL-->`Auth`<!--inline-NL-->. For the moment this class will be empty.<!--plain-NL-->

Update <!--plain-NL-->`api/v1/app.py`<!--inline-NL--> for using <!--plain-NL-->`BasicAuth`<!--inline-NL--> class instead of <!--plain-NL-->`Auth`<!--inline-NL--> depending of the value of the environment variable <!--plain-NL-->`AUTH_TYPE`<!--inline-NL-->, If <!--plain-NL-->`AUTH_TYPE`<!--inline-NL--> is equal to <!--plain-NL-->`basic_auth`<!--inline-NL-->:<!--plain-NL-->

- import `BasicAuth` from `api.v1.auth.basic_auth`
- create an instance of `BasicAuth` and assign it to the variable `auth`

Otherwise, keep the previous mechanism with <!--plain-NL-->`auth`<!--inline-NL--> an instance of <!--plain-NL-->`Auth`<!--inline-NL-->.<!--plain-NL-->

In the first terminal:<!--plain-NL-->

```
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 AUTH_TYPE=basic_auth python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

In a second terminal:<!--plain-NL-->

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status"
{
  "status": "OK"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status/"
{
  "status": "OK"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users"
{
  "error": "Unauthorized"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Test"
{
  "error": "Forbidden"
}
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/app.py, api/v1/auth/basic_auth.py`


---
### 7. Basic - Base64 part

Add the method <!--plain-NL-->`def extract_base64_authorization_header(self, authorization_header: str) -> str:`<!--inline-NL--> in the class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that returns the Base64 part of the <!--plain-NL-->`Authorization`<!--inline-NL--> header for a Basic Authentication:<!--plain-NL-->

- Return `None` if `authorization_header` is `None`
- Return `None` if `authorization_header` is not a string
- Return `None` if `authorization_header` doesn�t start by `Basic` (with a space at the end)
- Otherwise, return the value after `Basic` (after the space)
- You can assume `authorization_header` contains only one `Basic`

```
bob@dylan:~$ cat main_2.py
#!/usr/bin/env python3
""" Main 2
"""
from api.v1.auth.basic_auth import BasicAuth

a = BasicAuth()

print(a.extract_base64_authorization_header(None))
print(a.extract_base64_authorization_header(89))
print(a.extract_base64_authorization_header("Holberton School"))
print(a.extract_base64_authorization_header("Basic Holberton"))
print(a.extract_base64_authorization_header("Basic SG9sYmVydG9u"))
print(a.extract_base64_authorization_header("Basic SG9sYmVydG9uIFNjaG9vbA=="))
print(a.extract_base64_authorization_header("Basic1234"))

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_2.py
None
None
None
Holberton
SG9sYmVydG9u
SG9sYmVydG9uIFNjaG9vbA==
None
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/basic_auth.py`


---
### 8. Basic - Base64 decode

Add the method <!--plain-NL-->`def decode_base64_authorization_header(self, base64_authorization_header: str) -> str:`<!--inline-NL--> in the class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that returns the decoded value of a Base64 string <!--plain-NL-->`base64_authorization_header`<!--inline-NL-->:<!--plain-NL-->

- Return `None` if `base64_authorization_header` is `None`
- Return `None` if `base64_authorization_header` is not a string
- Return `None` if `base64_authorization_header` is not a valid Base64 - you can use `try/except`
- Otherwise, return the decoded value as UTF8 string - you can use `decode('utf-8')`

```
bob@dylan:~$ cat main_3.py
#!/usr/bin/env python3
""" Main 3
"""
from api.v1.auth.basic_auth import BasicAuth

a = BasicAuth()

print(a.decode_base64_authorization_header(None))
print(a.decode_base64_authorization_header(89))
print(a.decode_base64_authorization_header("Holberton School"))
print(a.decode_base64_authorization_header("SG9sYmVydG9u"))
print(a.decode_base64_authorization_header("SG9sYmVydG9uIFNjaG9vbA=="))
print(a.decode_base64_authorization_header(a.extract_base64_authorization_header("Basic SG9sYmVydG9uIFNjaG9vbA==")))

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_3.py
None
None
None
Holberton
Holberton School
Holberton School
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/basic_auth.py`


---
### 9. Basic - User credentials

Add the method <!--plain-NL-->`def extract_user_credentials(self, decoded_base64_authorization_header: str) -> (str, str)`<!--inline-NL--> in the class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that returns the user email and password from the Base64 decoded value.<!--plain-NL-->

- This method must return 2 values
- Return `None, None` if `decoded_base64_authorization_header` is `None`
- Return `None, None` if `decoded_base64_authorization_header` is not a string
- Return `None, None` if `decoded_base64_authorization_header` doesn�t contain `:`
- Otherwise, return the user email and the user password - these 2 values must be separated by a `:`
- You can assume `decoded_base64_authorization_header` will contain only one `:`

```
bob@dylan:~$ cat main_4.py
#!/usr/bin/env python3
""" Main 4
"""
from api.v1.auth.basic_auth import BasicAuth

a = BasicAuth()

print(a.extract_user_credentials(None))
print(a.extract_user_credentials(89))
print(a.extract_user_credentials("Holberton School"))
print(a.extract_user_credentials("Holberton:School"))
print(a.extract_user_credentials("bob@gmail.com:toto1234"))

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_4.py
(None, None)
(None, None)
(None, None)
('Holberton', 'School')
('bob@gmail.com', 'toto1234')
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/basic_auth.py`


---
### 10. Basic - User object

Add the method <!--plain-NL-->`def user_object_from_credentials(self, user_email: str, user_pwd: str) -> TypeVar('User'):`<!--inline-NL--> in the class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that returns the <!--plain-NL-->`User`<!--inline-NL--> instance based on his email and password.<!--plain-NL-->

- Return `None` if `user_email` is `None` or not a string
- Return `None` if `user_pwd` is `None` or not a string
- Return `None` if your database (file) doesn�t contain any `User` instance with email equal to `user_email` - you should use the class method `search` of the `User` to lookup the list of users based on their email. Don�t forget to test all cases: �what if there is no user in DB?�, etc.
- Return `None` if `user_pwd` is not the password of the `User` instance found - you must use the method `is_valid_password` of `User`
- Otherwise, return the `User` instance

```
bob@dylan:~$ cat main_5.py
#!/usr/bin/env python3
""" Main 5
"""
import uuid
from api.v1.auth.basic_auth import BasicAuth
from models.user import User

""" Create a user test """
user_email = str(uuid.uuid4())
user_clear_pwd = str(uuid.uuid4())
user = User()
user.email = user_email
user.first_name = "Bob"
user.last_name = "Dylan"
user.password = user_clear_pwd
print("New user: {}".format(user.display_name()))
user.save()

""" Retreive this user via the class BasicAuth """

a = BasicAuth()

u = a.user_object_from_credentials(None, None)
print(u.display_name() if u is not None else "None")

u = a.user_object_from_credentials(89, 98)
print(u.display_name() if u is not None else "None")

u = a.user_object_from_credentials("email@notfound.com", "pwd")
print(u.display_name() if u is not None else "None")

u = a.user_object_from_credentials(user_email, "pwd")
print(u.display_name() if u is not None else "None")

u = a.user_object_from_credentials(user_email, user_clear_pwd)
print(u.display_name() if u is not None else "None")

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_5.py 
New user: Bob Dylan
None
None
None
None
Bob Dylan
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/basic_auth.py`


---
### 11. Basic - Overload current_user - and BOOM!

Now, you have all pieces for having a complete Basic authentication.<!--plain-NL-->

Add the method <!--plain-NL-->`def current_user(self, request=None) -> TypeVar('User')`<!--inline-NL--> in the class <!--plain-NL-->`BasicAuth`<!--inline-NL--> that overloads <!--plain-NL-->`Auth`<!--inline-NL--> and retrieves the <!--plain-NL-->`User`<!--inline-NL--> instance for a request:<!--plain-NL-->

- You must use `authorization_header`
- You must use `extract_base64_authorization_header`
- You must use `decode_base64_authorization_header`
- You must use `extract_user_credentials`
- You must use `user_object_from_credentials`

With this update, now your API is fully protected by a Basic Authentication. Enjoy!<!--plain-NL-->

In the first terminal:<!--plain-NL-->

```
bob@dylan:~$ cat main_6.py
#!/usr/bin/env python3
""" Main 6
"""
import base64
from api.v1.auth.basic_auth import BasicAuth
from models.user import User

""" Create a user test """
user_email = "bob@hbtn.io"
user_clear_pwd = "H0lbertonSchool98!"
user = User()
user.email = user_email
user.password = user_clear_pwd
print("New user: {} / {}".format(user.id, user.display_name()))
user.save()

basic_clear = "{}:{}".format(user_email, user_clear_pwd)
print("Basic Base64: {}".format(base64.b64encode(basic_clear.encode('utf-8')).decode("utf-8")))

bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 ./main_6.py 
New user: 9375973a-68c7-46aa-b135-29f79e837495 / bob@hbtn.io
Basic Base64: Ym9iQGhidG4uaW86SDBsYmVydG9uU2Nob29sOTgh
bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 AUTH_TYPE=basic_auth python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

In a second terminal:<!--plain-NL-->

```
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status"
{
  "status": "OK"
}
bob@dylan:~$ 
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users"
{
  "error": "Unauthorized"
}
bob@dylan:~$ 
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Test"
{
  "error": "Forbidden"
}
bob@dylan:~$ 
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Basic test"
{
  "error": "Forbidden"
}
bob@dylan:~$
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Basic Ym9iQGhidG4uaW86SDBsYmVydG9uU2Nob29sOTgh"
[
  {
    "created_at": "2017-09-25 01:55:17", 
    "email": "bob@hbtn.io", 
    "first_name": null, 
    "id": "9375973a-68c7-46aa-b135-29f79e837495", 
    "last_name": null, 
    "updated_at": "2017-09-25 01:55:17"
  }
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `Basic_authentication`
- File: `api/v1/auth/basic_auth.py`