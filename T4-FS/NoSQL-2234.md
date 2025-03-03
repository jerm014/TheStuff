# Project 2234: NoSQL
----

## Resources

**Read or watch**:

* [NoSQL Databases Explained](https://riak.com/resources/nosql-databases/)
* [What is NoSQL ?](https://www.youtube.com/watch?v=qUV2j3XBRHc)
* [MongoDB with Python Crash Course - Tutorial for Beginners](https://www.youtube.com/watch?v=E-1xI85Zog8)
* [MongoDB Tutorial 2 : Insert, Update, Remove, Query](https://www.youtube.com/watch?v=CB9G5Dvv-EE)
* [Aggregation](https://www.mongodb.com/docs/manual/aggregation/)
* [Introduction to MongoDB and Python](https://realpython.com/introduction-to-mongodb-and-python/)
* [mongo Shell Methods](https://www.mongodb.com/docs/manual/reference/method/)
* [The mongo Shell](https://www.mongodb.com/docs/mongodb-shell/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What NoSQL means
* What is difference between SQL and NoSQL
* What is ACID
* What is a document storage
* What are NoSQL types
* What are benefits of a NoSQL database
* How to query information from a NoSQL database
* How to insert/update/delete information from a NoSQL database
* How to use MongoDB
## Requirements

### MongoDB Command File

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`MongoDB`(version 4.4)
* All your files should end with a new line
* The first line of all your files should be a comment:`// my comment`
* A`README.md`file, at the root of the folder of the project, is mandatory
* The length of your files will be tested using`wc`
### Python Scripts

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`python3`(version 3.9) and`PyMongo`(version 4.8.0)
* All your files should end with a new line
* The first line of all your files should be exactly`#!/usr/bin/env python3`
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`pycodestyle`style (version 2.5.*)
* The length of your files will be tested using`wc`
* All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
* All your functions should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`
* Your code should not be executed when imported (by using`if __name__ == "__main__"`:)
## More Info

### Install MongoDB 4.4 in Ubuntu 20.04

[Official installation guide](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/)


----
## Tasks
---
### 0. List all databases

Write a script that lists all databases in MongoDB.<!--plain-NL-->

```
guillaume@ubuntu:~/$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `0-list_databases`


---
### 1. Create a database

Write a script that creates or uses the database <!--plain-NL-->`my_db`<!--inline-NL-->:<!--plain-NL-->

```
guillaume@ubuntu:~/$ cat 0-list_databases | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
admin        0.000GB
config       0.000GB
local        0.000GB
logs         0.005GB
bye
guillaume@ubuntu:~/$
guillaume@ubuntu:~/$ cat 1-use_or_create_database | mongo
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 3.6.3
switched to db my_db
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `1-use_or_create_database`


---
### 2. Insert document

Write a script that inserts a document in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The document must have one attribute `name` with value “Holberton school”
- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 2-insert | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
WriteResult({ "nInserted" : 1 })
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `2-insert`


---
### 3. All documents

Write a script that lists all documents in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 3-all | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `3-all`


---
### 4. All matches

Write a script that lists all documents with <!--plain-NL-->`name="Holberton school"`<!--inline-NL--> in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school" }
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `4-match`


---
### 5. Count

Write a script that displays the number of documents in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 5-count | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
1
bye
guillaume@ubuntu:~/$

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `5-count`


---
### 6. Update

Write a script that adds a new attribute to a document in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The script should update only document with `name="Holberton school"` (all of them)
- The update should add the attribute `address` with the value “972 Mission street”
- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 6-update | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
WriteResult({ "nMatched" : 1, "nUpserted" : 0, "nModified" : 1 })
bye
guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "_id" : ObjectId("5a8fad532b69437b63252406"), "name" : "Holberton school", "address" : "972 Mission street" }
bye
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `6-update`


---
### 7. Delete by match

Write a script that deletes all documents with <!--plain-NL-->`name="Holberton school"`<!--inline-NL--> in the collection <!--plain-NL-->`school`<!--inline-NL-->:<!--plain-NL-->

- The database name will be passed as option of `mongo` command

```
guillaume@ubuntu:~/$ cat 7-delete | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
{ "acknowledged" : true, "deletedCount" : 1 }
bye
guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ cat 4-match | mongo my_db
MongoDB shell version v3.6.3
connecting to: mongodb://127.0.0.1:27017/my_db
MongoDB server version: 3.6.3
bye
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `7-delete`


---
### 8. List all documents in Python

Write a Python function that lists all documents in a collection:<!--plain-NL-->

- Prototype: `def list_all(mongo_collection):`
- Return an empty list if no document in the collection
- `mongo_collection` will be the `pymongo` collection object

```
guillaume@ubuntu:~/$ cat 8-main.py
#!/usr/bin/env python3
""" 8-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {}".format(school.get('_id'), school.get('name')))

guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ ./8-main.py
[5a8f60cfd4321e1403ba7ab9] Holberton school
[5a8f60cfd4321e1403ba7aba] UCSD
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `8-all.py`


---
### 9. Insert a document in Python

Write a Python function that inserts a new document in a collection based on <!--plain-NL-->`kwargs`<!--inline-NL-->:<!--plain-NL-->

- Prototype: `def insert_school(mongo_collection, **kwargs):`
- `mongo_collection` will be the `pymongo` collection object
- Returns the new `_id`

```
guillaume@ubuntu:~/$ cat 9-main.py
#!/usr/bin/env python3
""" 9-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
insert_school = __import__('9-insert_school').insert_school

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    new_school_id = insert_school(school_collection, name="UCSF", address="505 Parnassus Ave")
    print("New school created: {}".format(new_school_id))

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('address', "")))

guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ ./9-main.py
New school created: 5a8f60cfd4321e1403ba7abb
[5a8f60cfd4321e1403ba7ab9] Holberton school
[5a8f60cfd4321e1403ba7aba] UCSD
[5a8f60cfd4321e1403ba7abb] UCSF 505 Parnassus Ave
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `9-insert_school.py`


---
### 10. Change school topics

Write a Python function that changes all topics of a school document based on the name:<!--plain-NL-->

- Prototype: `def update_topics(mongo_collection, name, topics):`
- `mongo_collection` will be the `pymongo` collection object
- `name` (string) will be the school name to update
- `topics` (list of strings) will be the list of topics approached in the school

```
guillaume@ubuntu:~/$ cat 10-main.py
#!/usr/bin/env python3
""" 10-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
update_topics = __import__('10-update_topics').update_topics

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school
    update_topics(school_collection, "Holberton school", ["Sys admin", "AI", "Algorithm"])

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

    update_topics(school_collection, "Holberton school", ["iOS"])

    schools = list_all(school_collection)
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ ./10-main.py
[5a8f60cfd4321e1403ba7abb] UCSF 
[5a8f60cfd4321e1403ba7aba] UCSD 
[5a8f60cfd4321e1403ba7ab9] Holberton school ['Sys admin', 'AI', 'Algorithm']
[5a8f60cfd4321e1403ba7abb] UCSF 
[5a8f60cfd4321e1403ba7aba] UCSD 
[5a8f60cfd4321e1403ba7ab9] Holberton school ['iOS']
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `10-update_topics.py`


---
### 11. Where can I learn Python?

Write a Python function that returns the list of school having a specific topic:<!--plain-NL-->

- Prototype: `def schools_by_topic(mongo_collection, topic):`
- `mongo_collection` will be the `pymongo` collection object
- `topic` (string) will be topic searched

```
guillaume@ubuntu:~/$ cat 11-main.py
#!/usr/bin/env python3
""" 11-main """
from pymongo import MongoClient
list_all = __import__('8-all').list_all
insert_school = __import__('9-insert_school').insert_school
schools_by_topic = __import__('11-schools_by_topic').schools_by_topic

if __name__ == "__main__":
    client = MongoClient('mongodb://127.0.0.1:27017')
    school_collection = client.my_db.school

    j_schools = [
        { 'name': "Holberton school", 'topics': ["Algo", "C", "Python", "React"]},
        { 'name': "UCSF", 'topics': ["Algo", "MongoDB"]},
        { 'name': "UCLA", 'topics': ["C", "Python"]},
        { 'name': "UCSD", 'topics': ["Cassandra"]},
        { 'name': "Stanford", 'topics': ["C", "React", "Javascript"]}
    ]
    for j_school in j_schools:
        insert_school(school_collection, **j_school)

    schools = schools_by_topic(school_collection, "Python")
    for school in schools:
        print("[{}] {} {}".format(school.get('_id'), school.get('name'), school.get('topics', "")))

guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ ./11-main.py
[5a90731fd4321e1e5a3f53e3] Holberton school ['Algo', 'C', 'Python', 'React']
[5a90731fd4321e1e5a3f53e5] UCLA ['C', 'Python']
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `11-schools_by_topic.py`


---
### 12. Log stats

Write a Python script that provides some stats about Nginx logs stored in MongoDB:<!--plain-NL-->

- Database: `logs`
- Collection: `nginx`
- Display (same as the example):


first line: `x logs` where `x` is the number of documents in this collection
second line: `Methods:`
5 lines with the number of documents with the `method` = `["GET", "POST", "PUT", "PATCH", "DELETE"]` in this order (see example below - warning: it’s a tabulation before each line) 
one line with the number of documents with:


`method=GET`
`path=/status`
- first line: `x logs` where `x` is the number of documents in this collection
- second line: `Methods:`
- 5 lines with the number of documents with the `method` = `["GET", "POST", "PUT", "PATCH", "DELETE"]` in this order (see example below - warning: it’s a tabulation before each line)
- one line with the number of documents with:


`method=GET`
`path=/status`
- `method=GET`
- `path=/status`

- first line: `x logs` where `x` is the number of documents in this collection
- second line: `Methods:`
- 5 lines with the number of documents with the `method` = `["GET", "POST", "PUT", "PATCH", "DELETE"]` in this order (see example below - warning: it’s a tabulation before each line)
- one line with the number of documents with:


`method=GET`
`path=/status`
- `method=GET`
- `path=/status`

- `method=GET`
- `path=/status`

You can use this dump as data sample: <!--plain-->[dump.zip](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2020/6/645541f867bb79ae47b7a80922e9a48604a569b9.zip?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20250303%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20250303T204802Z&X-Amz-Expires=345600&X-Amz-SignedHeaders=host&X-Amz-Signature=d8414c27324d3ade735817706ba2f87c7b19d64bc2cc1e568cdeae7dca698336) <!--link--> <!--plain-->

The output of your script <!--plain-NL-->**must be exactly the same as the example**<!--code-NL-->

```
guillaume@ubuntu:~/$ curl -o dump.zip -s "https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-webstack/411/dump.zip"
guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ unzip dump.zip
Archive:  dump.zip
   creating: dump/
   creating: dump/logs/
  inflating: dump/logs/nginx.metadata.json  
  inflating: dump/logs/nginx.bson    
guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ mongorestore dump
2018-02-23T20:12:37.807+0000    preparing collections to restore from
2018-02-23T20:12:37.816+0000    reading metadata for logs.nginx from dump/logs/nginx.metadata.json
2018-02-23T20:12:37.825+0000    restoring logs.nginx from dump/logs/nginx.bson
2018-02-23T20:12:40.804+0000    [##......................]  logs.nginx  1.21MB/13.4MB  (9.0%)
2018-02-23T20:12:43.803+0000    [#####...................]  logs.nginx  2.88MB/13.4MB  (21.4%)
2018-02-23T20:12:46.803+0000    [#######.................]  logs.nginx  4.22MB/13.4MB  (31.4%)
2018-02-23T20:12:49.803+0000    [##########..............]  logs.nginx  5.73MB/13.4MB  (42.7%)
2018-02-23T20:12:52.803+0000    [############............]  logs.nginx  7.23MB/13.4MB  (53.8%)
2018-02-23T20:12:55.803+0000    [###############.........]  logs.nginx  8.53MB/13.4MB  (63.5%)
2018-02-23T20:12:58.803+0000    [#################.......]  logs.nginx  10.1MB/13.4MB  (74.9%)
2018-02-23T20:13:01.803+0000    [####################....]  logs.nginx  11.3MB/13.4MB  (83.9%)
2018-02-23T20:13:04.803+0000    [######################..]  logs.nginx  12.8MB/13.4MB  (94.9%)
2018-02-23T20:13:06.228+0000    [########################]  logs.nginx  13.4MB/13.4MB  (100.0%)
2018-02-23T20:13:06.230+0000    no indexes to restore
2018-02-23T20:13:06.231+0000    finished restoring logs.nginx (94778 documents)
2018-02-23T20:13:06.232+0000    done
guillaume@ubuntu:~/$ 
guillaume@ubuntu:~/$ ./12-log_stats.py 
94778 logs
Methods:
    method GET: 93842
    method POST: 229
    method PUT: 0
    method PATCH: 0
    method DELETE: 0
47415 status check
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `NoSQL`
- File: `12-log_stats.py`