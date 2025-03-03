# Project 2350: User authentication service
----


![1](2350_1.jpg)

In the industry, you should**not**implement your own authentication system and use a module or framework that doing it for you (like in Python-Flask:[Flask-User](https://flask-user.readthedocs.io/en/latest/)). Here, for the learning purpose, we will walk through each step of this mechanism to understand it by doing.

## Resources

**Read or watch:**

* [Flask documentation](https://flask.palletsprojects.com/en/stable/quickstart/)
* [Requests module](https://requests.kennethreitz.org/en/latest/user/quickstart/)
* [HTTP status codes](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* How to declare API routes in a Flask app
* How to get and set cookies
* How to retrieve request form data
* How to return various HTTP status codes
## Requirements

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.5)
* You should use`SQLAlchemy`
* All your files must be executable
* The length of your files will be tested using`wc`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your classes should have a documentation (`python3 -c 'print(__import__("my_module").MyClass.__doc__)'`)
* All your functions (inside and outside a class) should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`and`python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'`)
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
* All your functions should be type annotated
* The flask app should only interact with`Auth`and never with`DB`directly.
* Only public methods of`Auth`and`DB`should be used outside these classes
## Setup

You will need to install`bcrypt`

`
```
pip3 install bcrypt
```

----
## Tasks
---
### 0. User model

In this task you will create a SQLAlchemy model named <!--plain-->`User`<!--inline--> for a database table named <!--plain-->`users`<!--inline--> (by using the <!--plain-->[mapping declaration](https://docs.sqlalchemy.org/en/13/orm/tutorial.html#declare-a-mapping) <!--link--> of SQLAlchemy). <!--plain-->

The model will have the following attributes:<!--plain-NL-->

- `id`, the integer primary key
- `email`, a non-nullable string
- `hashed_password`, a non-nullable string
- `session_id`, a nullable string
- `reset_token`, a nullable string

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from user import User

print(User.__tablename__)

for column in User.__table__.columns:
    print("{}: {}".format(column, column.type))

bob@dylan:~$ python3 main.py
users
users.id: INTEGER
users.email: VARCHAR(250)
users.hashed_password: VARCHAR(250)
users.session_id: VARCHAR(250)
users.reset_token: VARCHAR(250)
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `user.py`


---
### 1. create user

In this task, you will complete the <!--plain-NL-->`DB`<!--inline-NL--> class provided below to implement the <!--plain-NL-->`add_user`<!--inline-NL--> method.<!--plain-NL-->

```
"""DB module
"""
from sqlalchemy import create_engine
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker
from sqlalchemy.orm.session import Session

from user import Base


class DB:
    """DB class
    """

    def __init__(self) -> None:
        """Initialize a new DB instance
        """
        self._engine = create_engine("sqlite:///a.db", echo=True)
        Base.metadata.drop_all(self._engine)
        Base.metadata.create_all(self._engine)
        self.__session = None

    @property
    def _session(self) -> Session:
        """Memoized session object
        """
        if self.__session is None:
            DBSession = sessionmaker(bind=self._engine)
            self.__session = DBSession()
        return self.__session

```

Note that <!--plain-NL-->`DB._session`<!--inline-NL--> is a private property and hence should NEVER be used from outside the <!--plain-NL-->`DB`<!--inline-NL--> class.<!--plain-NL-->

Implement the <!--plain-NL-->`add_user`<!--inline-NL--> method, which has two required string arguments: <!--plain-NL-->`email`<!--inline-NL--> and <!--plain-NL-->`hashed_password`<!--inline-NL-->, and returns a <!--plain-NL-->`User`<!--inline-NL--> object. The method should save the user to the database. No validations are required at this stage.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""

from db import DB
from user import User

my_db = DB()

user_1 = my_db.add_user("test@test.com", "SuperHashedPwd")
print(user_1.id)

user_2 = my_db.add_user("test1@test.com", "SuperHashedPwd1")
print(user_2.id)

bob@dylan:~$ python3 main.py
1
2
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `db.py`


---
### 2. Find user

In this task you will implement the <!--plain-NL-->`DB.find_user_by`<!--inline-NL--> method. This method takes in arbitrary keyword arguments and returns the first row found in the <!--plain-NL-->`users`<!--inline-NL--> table as filtered by the method’s input arguments. No validation of input arguments required at this point.<!--plain-NL-->

Make sure that SQLAlchemy’s <!--plain-NL-->`NoResultFound`<!--inline-NL--> and <!--plain-NL-->`InvalidRequestError`<!--inline-NL--> are raised when no results are found, or when wrong query arguments are passed, respectively.<!--plain-NL-->

**Warning:**<!--code-NL-->

- `NoResultFound` has been moved from `sqlalchemy.orm.exc` to `sqlalchemy.exc` between the version 1.3.x and 1.4.x of SQLAchemy - please make sure you are importing it from `sqlalchemy.orm.exc`

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from db import DB
from user import User

from sqlalchemy.exc import InvalidRequestError
from sqlalchemy.orm.exc import NoResultFound


my_db = DB()

user = my_db.add_user("test@test.com", "PwdHashed")
print(user.id)

find_user = my_db.find_user_by(email="test@test.com")
print(find_user.id)

try:
    find_user = my_db.find_user_by(email="test2@test.com")
    print(find_user.id)
except NoResultFound:
    print("Not found")

try:
    find_user = my_db.find_user_by(no_email="test@test.com")
    print(find_user.id)
except InvalidRequestError:
    print("Invalid")        

bob@dylan:~$ python3 main.py
1
1
Not found
Invalid
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `db.py`


---
### 3. update user

In this task, you will implement the <!--plain-NL-->`DB.update_user`<!--inline-NL--> method that takes as argument a required <!--plain-NL-->`user_id`<!--inline-NL--> integer and arbitrary keyword arguments, and returns <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

The method will use <!--plain-NL-->`find_user_by`<!--inline-NL--> to locate the user to update, then will update the user’s attributes as passed in the method’s arguments then commit changes to the database.<!--plain-NL-->

If an argument that does not correspond to a user attribute is passed, raise a <!--plain-NL-->`ValueError`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from db import DB
from user import User

from sqlalchemy.exc import InvalidRequestError
from sqlalchemy.orm.exc import NoResultFound


my_db = DB()

email = 'test@test.com'
hashed_password = "hashedPwd"

user = my_db.add_user(email, hashed_password)
print(user.id)

try:
    my_db.update_user(user.id, hashed_password='NewPwd')
    print("Password updated")
except ValueError:
    print("Error")

bob@dylan:~$ python3 main.py
1
Password updated
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `db.py`


---
### 4. Hash password

In this task you will define a <!--plain-NL-->`_hash_password`<!--inline-NL--> method that takes in a <!--plain-NL-->`password`<!--inline-NL--> string arguments and returns bytes.<!--plain-NL-->

The returned bytes is a salted hash of the input password, hashed with <!--plain-NL-->`bcrypt.hashpw`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from auth import _hash_password

print(_hash_password("Hello Holberton"))

bob@dylan:~$ python3 main.py
b'$2b$12$eUDdeuBtrD41c8dXvzh95ehsWYCCAi4VH1JbESzgbgZT.eMMzi.G2'
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 5. Register user

In this task, you will implement the <!--plain-NL-->`Auth.register_user`<!--inline-NL--> in the <!--plain-NL-->`Auth`<!--inline-NL--> class provided below:<!--plain-NL-->

```
from db import DB


class Auth:
    """Auth class to interact with the authentication database.
    """

    def __init__(self):
        self._db = DB()

```

Note that <!--plain-NL-->`Auth._db`<!--inline-NL--> is a private property and should NEVER be used from outside the class.<!--plain-NL-->

`Auth.register_user`<!--inline-NL--> should take mandatory <!--plain-NL-->`email`<!--inline-NL--> and <!--plain-NL-->`password`<!--inline-NL--> string arguments and return a <!--plain-NL-->`User`<!--inline-NL--> object.<!--plain-NL-->

If a user already exist with the passed email, raise a <!--plain-NL-->`ValueError`<!--inline-NL--> with the message <!--plain-NL-->`User <user's email> already exists`<!--inline-NL-->.<!--plain-NL-->

If not, hash the password with <!--plain-NL-->`_hash_password`<!--inline-NL-->, save the user to the database using <!--plain-NL-->`self._db`<!--inline-NL--> and return the <!--plain-NL-->`User`<!--inline-NL--> object.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from auth import Auth

email = 'me@me.com'
password = 'mySecuredPwd'

auth = Auth()

try:
    user = auth.register_user(email, password)
    print("successfully created a new user!")
except ValueError as err:
    print("could not create a new user: {}".format(err))

try:
    user = auth.register_user(email, password)
    print("successfully created a new user!")
except ValueError as err:
    print("could not create a new user: {}".format(err))        

bob@dylan:~$ python3 main.py
successfully created a new user!
could not create a new user: User me@me.com already exists
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 6. Basic Flask app

In this task, you will set up a basic Flask app.<!--plain-NL-->

Create a Flask app that has a single <!--plain-NL-->`GET`<!--inline-NL--> route (<!--plain-NL-->`"/"`<!--inline-NL-->) and use <!--plain-NL-->`flask.jsonify`<!--inline-NL--> to return a JSON payload of the form:<!--plain-NL-->

```
{"message": "Bienvenue"}

```

Add the following code at the end of the module:<!--plain-NL-->

```
if __name__ == "__main__":
    app.run(host="0.0.0.0", port="5000")

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 7. Register user

In this task, you will implement the end-point to register a user. Define a <!--plain-NL-->`users`<!--inline-NL--> function that implements the <!--plain-NL-->`POST /users`<!--inline-NL--> route.<!--plain-NL-->

Import the <!--plain-NL-->`Auth`<!--inline-NL--> object and instantiate it at the root of the module as such:<!--plain-NL-->

```
from auth import Auth


AUTH = Auth()

```

The end-point should expect two form data fields: <!--plain-NL-->`"email"`<!--inline-NL--> and <!--plain-NL-->`"password"`<!--inline-NL-->. If the user does not exist, the end-point should register it and respond with the following JSON payload:<!--plain-NL-->

```
{"email": "<registered email>", "message": "user created"}

```

If the user is already registered, catch the exception and return a JSON payload of the form<!--plain-NL-->

```
{"message": "email already registered"}

```

and return a 400 status code<!--plain-NL-->

Remember that you should only use <!--plain-NL-->`AUTH`<!--inline-NL--> in this app. <!--plain-NL-->`DB`<!--inline-NL--> is a lower abstraction that is proxied by <!--plain-NL-->`Auth`<!--inline-NL-->.<!--plain-NL-->

*Terminal 1:*<!--italics-NL-->

```
bob@dylan:~$ python3 app.py 
* Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: This is a development server. Do not use it in a production deployment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)


```

Terminal 2:<!--plain-NL-->

```
bob@dylan:~$ curl -XPOST localhost:5000/users -d 'email=bob@me.com' -d 'password=mySuperPwd' -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> POST /users HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Content-Length: 40
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 40 out of 40 bytes
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 52
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:03:18 GMT
< 
{"email":"bob@me.com","message":"user created"}

bob@dylan:~$
bob@dylan:~$ curl -XPOST localhost:5000/users -d 'email=bob@me.com' -d 'password=mySuperPwd' -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> POST /users HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Content-Length: 40
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 40 out of 40 bytes
* HTTP 1.0, assume close after body
< HTTP/1.0 400 BAD REQUEST
< Content-Type: application/json
< Content-Length: 39
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:03:33 GMT
< 
{"message":"email already registered"}
bob@dylan:~$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 8. Credentials validation

In this task, you will implement the <!--plain-NL-->`Auth.valid_login`<!--inline-NL--> method. It should expect <!--plain-NL-->`email`<!--inline-NL--> and <!--plain-NL-->`password`<!--inline-NL--> required arguments and return a boolean.<!--plain-NL-->

Try locating the user by email. If it exists, check the password with <!--plain-NL-->`bcrypt.checkpw`<!--inline-NL-->. If it matches return <!--plain-NL-->`True`<!--inline-NL-->. In any other case, return <!--plain-NL-->`False`<!--inline-NL-->.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from auth import Auth

email = 'bob@bob.com'
password = 'MyPwdOfBob'
auth = Auth()

auth.register_user(email, password)

print(auth.valid_login(email, password))

print(auth.valid_login(email, "WrongPwd"))

print(auth.valid_login("unknown@email", password))

bob@dylan:~$ python3 main.py
True
False
False
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 9. Generate UUIDs

In this task you will implement a <!--plain-NL-->`_generate_uuid`<!--inline-NL--> function in the <!--plain-NL-->`auth`<!--inline-NL--> module. The function should return a string representation of a new UUID. Use the <!--plain-NL-->`uuid`<!--inline-NL--> module.<!--plain-NL-->

Note that the method is private to the <!--plain-NL-->`auth`<!--inline-NL--> module and should <!--plain-NL-->**NOT**<!--code-NL--> be used outside of it.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 10. Get session ID

In this task, you will implement the <!--plain-NL-->`Auth.create_session`<!--inline-NL--> method. It takes an <!--plain-NL-->`email`<!--inline-NL--> string argument and returns the session ID as a string.<!--plain-NL-->

The method should find the user corresponding to the email, generate a new UUID and store it in the database as the user’s <!--plain-NL-->`session_id`<!--inline-NL-->, then return the session ID.<!--plain-NL-->

Remember that only public methods of <!--plain-NL-->`self._db`<!--inline-NL--> can be used.<!--plain-NL-->

```
bob@dylan:~$ cat main.py
#!/usr/bin/env python3
"""
Main file
"""
from auth import Auth

email = 'bob@bob.com'
password = 'MyPwdOfBob'
auth = Auth()

auth.register_user(email, password)

print(auth.create_session(email))
print(auth.create_session("unknown@email.com"))

bob@dylan:~$ python3 main.py
5a006849-343e-4a48-ba4e-bbd523fcca58
None
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 11. Log in

In this task, you will implement a <!--plain-NL-->`login`<!--inline-NL--> function to respond to the <!--plain-NL-->`POST /sessions`<!--inline-NL--> route.<!--plain-NL-->

The request is expected to contain form data with <!--plain-NL-->`"email"`<!--inline-NL--> and a <!--plain-NL-->`"password"`<!--inline-NL--> fields.<!--plain-NL-->

If the login information is incorrect, use <!--plain-NL-->`flask.abort`<!--inline-NL--> to respond with a 401 HTTP status.<!--plain-NL-->

Otherwise, create a new session for the user, store it the session ID as a cookie with key <!--plain-NL-->`"session_id"`<!--inline-NL--> on the response and return a JSON payload of the form<!--plain-NL-->

```
{"email": "<user email>", "message": "logged in"}

```

```
bob@dylan:~$ curl -XPOST localhost:5000/users -d 'email=bob@bob.com' -d 'password=mySuperPwd'
{"email":"bob@bob.com","message":"user created"}
bob@dylan:~$ 
bob@dylan:~$  curl -XPOST localhost:5000/sessions -d 'email=bob@bob.com' -d 'password=mySuperPwd' -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> POST /sessions HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Content-Length: 37
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 37 out of 37 bytes
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 46
< Set-Cookie: session_id=163fe508-19a2-48ed-a7c8-d9c6e56fabd1; Path=/
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:12:34 GMT
< 
{"email":"bob@bob.com","message":"logged in"}
* Closing connection 0
bob@dylan:~$ 
bob@dylan:~$ curl -XPOST localhost:5000/sessions -d 'email=bob@bob.com' -d 'password=BlaBla' -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> POST /sessions HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Content-Length: 34
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 34 out of 34 bytes
* HTTP 1.0, assume close after body
< HTTP/1.0 401 UNAUTHORIZED
< Content-Type: text/html; charset=utf-8
< Content-Length: 338
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:12:45 GMT
< 
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>401 Unauthorized</title>
<h1>Unauthorized</h1>
<p>The server could not verify that you are authorized to access the URL requested. You either supplied the wrong credentials (e.g. a bad password), or your browser doesn't understand how to supply the credentials required.</p>
* Closing connection 0
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 12. Find user by session ID

In this task, you will implement the <!--plain-NL-->`Auth.get_user_from_session_id`<!--inline-NL--> method. It takes a single <!--plain-NL-->`session_id`<!--inline-NL--> string argument and returns the corresponding <!--plain-NL-->`User`<!--inline-NL--> or <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

If the session ID is <!--plain-NL-->`None`<!--inline-NL--> or no user is found, return <!--plain-NL-->`None`<!--inline-NL-->. Otherwise return the corresponding user.<!--plain-NL-->

Remember to only use public methods of <!--plain-NL-->`self._db`<!--inline-NL-->.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 13. Destroy session

In this task, you will implement <!--plain-NL-->`Auth.destroy_session`<!--inline-NL-->. The method takes a single <!--plain-NL-->`user_id`<!--inline-NL--> integer argument and returns <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

The method updates the corresponding user’s session ID to <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

Remember to only use public methods of <!--plain-NL-->`self._db`<!--inline-NL-->.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 14. Log out

In this task, you will implement a <!--plain-NL-->`logout`<!--inline-NL--> function to respond to the <!--plain-NL-->`DELETE /sessions`<!--inline-NL--> route.<!--plain-NL-->

The request is expected to contain the session ID as a cookie with key <!--plain-NL-->`"session_id"`<!--inline-NL-->.<!--plain-NL-->

Find the user with the requested session ID. If the user exists destroy the session and redirect the user to <!--plain-NL-->`GET /`<!--inline-NL-->. If the user does not exist, respond with a 403 HTTP status.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 15. User profile

In this task, you will implement a <!--plain-NL-->`profile`<!--inline-NL--> function to respond to the <!--plain-NL-->`GET /profile`<!--inline-NL--> route.<!--plain-NL-->

The request is expected to contain a <!--plain-NL-->`session_id`<!--inline-NL--> cookie. Use it to find the user. If the user exist, respond with a 200 HTTP status and the following JSON payload:<!--plain-NL-->

```
{"email": "<user email>"}

```

If the session ID is invalid or the user does not exist, respond with a 403 HTTP status.<!--plain-NL-->

```
bob@dylan:~$ curl -XPOST localhost:5000/sessions -d 'email=bob@bob.com' -d 'password=mySuperPwd' -v
Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> POST /sessions HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Content-Length: 37
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 37 out of 37 bytes
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 46
< Set-Cookie: session_id=75c89af8-1729-44d9-a592-41b5e59de9a1; Path=/
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:15:57 GMT
< 
{"email":"bob@bob.com","message":"logged in"}
* Closing connection 0
bob@dylan:~$
bob@dylan:~$ curl -XGET localhost:5000/profile -b "session_id=75c89af8-1729-44d9-a592-41b5e59de9a1"
{"email": "bob@bob.com"}
bob@dylan:~$ 
bob@dylan:~$ curl -XGET localhost:5000/profile -b "session_id=nope" -v
Note: Unnecessary use of -X or --request, GET is already inferred.
*   Trying 127.0.0.1...
* TCP_NODELAY set
* Connected to localhost (127.0.0.1) port 5000 (#0)
> GET /profile HTTP/1.1
> Host: localhost:5000
> User-Agent: curl/7.58.0
> Accept: */*
> Cookie: session_id=75c89af8-1729-44d9-a592-41b5e59de9a
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 403 FORBIDDEN
< Content-Type: text/html; charset=utf-8
< Content-Length: 234
< Server: Werkzeug/1.0.1 Python/3.7.3
< Date: Wed, 19 Aug 2020 00:16:43 GMT
< 
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2 Final//EN">
<title>403 Forbidden</title>
<h1>Forbidden</h1>
<p>You don't have the permission to access the requested resource. It is either read-protected or not readable by the server.</p>
* Closing connection 0

bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 16. Generate reset password token

In this task, you will implement the <!--plain-NL-->`Auth.get_reset_password_token`<!--inline-NL--> method. It take an <!--plain-NL-->`email`<!--inline-NL--> string argument and returns a string.<!--plain-NL-->

Find the user corresponding to the email. If the user does not exist, raise a <!--plain-NL-->`ValueError`<!--inline-NL--> exception. If it exists, generate a UUID and update the user’s <!--plain-NL-->`reset_token`<!--inline-NL--> database field. Return the token.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 17. Get reset password token

In this task, you will implement a <!--plain-NL-->`get_reset_password_token`<!--inline-NL--> function to respond to the <!--plain-NL-->`POST /reset_password`<!--inline-NL--> route.<!--plain-NL-->

The request is expected to contain form data with the <!--plain-NL-->`"email"`<!--inline-NL--> field.<!--plain-NL-->

If the email is not registered, respond with a 403 status code. Otherwise, generate a token and respond with a 200 HTTP status and the following JSON payload:<!--plain-NL-->

```
{"email": "<user email>", "reset_token": "<reset token>"}

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`


---
### 18. Update password

In this task, you will implement the <!--plain-NL-->`Auth.update_password`<!--inline-NL--> method. It takes <!--plain-NL-->`reset_token`<!--inline-NL--> string argument and a <!--plain-NL-->`password`<!--inline-NL--> string argument and returns <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

Use the <!--plain-NL-->`reset_token`<!--inline-NL--> to find the corresponding user. If it does not exist, raise a <!--plain-NL-->`ValueError`<!--inline-NL--> exception.<!--plain-NL-->

Otherwise, hash the password and update the user’s <!--plain-NL-->`hashed_password`<!--inline-NL--> field with the new hashed password and the <!--plain-NL-->`reset_token`<!--inline-NL--> field to <!--plain-NL-->`None`<!--inline-NL-->.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `auth.py`


---
### 19. Update password end-point

In this task you will implement the <!--plain-NL-->`update_password`<!--inline-NL--> function in the <!--plain-NL-->`app`<!--inline-NL--> module to respond to the <!--plain-NL-->`PUT /reset_password`<!--inline-NL--> route.<!--plain-NL-->

The request is expected to contain form data with fields <!--plain-NL-->`"email"`<!--inline-NL-->, <!--plain-NL-->`"reset_token"`<!--inline-NL--> and <!--plain-NL-->`"new_password"`<!--inline-NL-->.<!--plain-NL-->

Update the password. If the token is invalid, catch the exception and respond with a 403 HTTP code.<!--plain-NL-->

If the token is valid, respond with a 200 HTTP code and the following JSON payload:<!--plain-NL-->

```
{"email": "<user email>", "message": "Password updated"}

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `user_authentication_service`
- File: `app.py`