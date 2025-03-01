# Project 2135: AirBnB clone - Web dynamic
----


*For this project, we expect you to look at this concept:*

* [AirBnB clone](/concepts/865)
## Resources

**Read or watch**:

* [Selector](https://jquery-tutorial.net/selectors/using-elements-ids-and-classes/)
* [Get and set content](https://jquery-tutorial.net/dom-manipulation/getting-and-setting-content/)
* [Manipulate CSS classes](https://jquery-tutorial.net/dom-manipulation/getting-and-setting-css-classes/)
* [Manipulate DOM elements](https://jquery-tutorial.net/dom-manipulation/the-append-and-prepend-methods/)
* [Document ready](https://learn.jquery.com/using-jquery-core/document-ready/)
* [Introduction](https://jquery-tutorial.net/ajax/introduction/)
* [GET & POST request](https://jquery-tutorial.net/ajax/the-get-and-post-methods/)
* [HTTP access control (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* How cool it is to request your own API
* How to modify an HTML element style
* How to get and update an HTML element content
* How to modify the DOM
* How to make a`GET`request with JQuery Ajax
* How to make a`POST`request with JQuery Ajax
* How to listen/bind to DOM events
* How to listen/bind to user events
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be interpreted on Chrome (version 57.0)
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should be`semistandard`compliant with the flag`--global $`:`semistandard *.js --global $`
* All your JavaScript must be in the folder`scripts`
* You must use JQuery version 3.x
* You are not allowed to use`var`
* HTML should not reload for each action: DOM manipulation, update values, fetch data…
### GitHub

**There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.**

## More Info

### Import JQuery

``
```
<head>
    <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
</head>
```
### Before starting the project…

You will work on a codebase using[Flasgger](https://github.com/flasgger/flasgger), you will need to install it locally first before starting the RestAPI:

``
```
$ sudo apt-get install -y python3-lxml
$ sudo pip3 install flask_cors # if it was not installed yet
$ sudo pip3 install flasgger
```

If the RestAPI is not starting, please read the error message. Based on the(ses) error message(s), you will have to troubleshoot potential dependencies issues.

Here some solutions:

#### `jsonschema`exception

``
```
$ sudo pip3 uninstall -y jsonschema 
$ sudo pip3 install jsonschema==3.0.1
```
#### `No module named 'pathlib2'`

``
```
$ sudo pip3 install pathlib2
```
### Expose ports from your Vagrant

In your`Vagrantfile`, add this line for each port forwarded

``
```
# I expose the port 5001 of my vm to the port 5001 on my computer
config.vm.network :forwarded_port, guest: 5001, host: 5001
```

if you need to expose other ports, same line but you will need to replace the “guest port” (inside your vagrant) and your “host port” (outside your vagrant, used from your browser for example)

It’s important in your project, to use the AirBnB API with the port`5001`

![1](2135_1.png)

### 

**It is your responsibility to request a review for this project from a peer before the project’s deadline. If no peers have been reviewed, you should request a review from a TA or staff member.**


----
## Tasks
---
### 0. Last clone!

A new codebase again? Yes!

For this project you will fork this codebase:

- Update the repository name to `AirBnB_clone_v4`
- Update the `README.md`:


Add yourself as an author of the project
Add new information about your new contribution
Make it better!
- Add yourself as an author of the project
- Add new information about your new contribution
- Make it better!
- If you’re the owner of this codebase, create a new repository called `AirBnB_clone_v4` and copy over all files from `AirBnB_clone_v3`
- If you didn’t install Flasgger from the previous project, it’s time! `sudo pip3 install flasgger`

- Add yourself as an author of the project
- Add new information about your new contribution
- Make it better!

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`


---
### 1. Cash only

Write a script that starts a Flask web application:

If 100-hbnb.html is not present, use 8-hbnb.html instead

One problem now is the asset caching done by Flask.

To avoid that, you will add a query string to each asset:

In 0-hbnb.py, add a variable cache_id to the render_template. The value of this variable must be an UUID (uuid.uuid4())

In 0-hbnb.html, add this variable cache_id as query string to each <link> tag URL

- Based on `web_flask`, copy: `web_flask/static`, `web_flask/templates/100-hbnb.html`, `web_flask/__init__.py` and `web_flask/100-hbnb.py` into the `web_dynamic` folder
- Rename `100-hbnb.py` to `0-hbnb.py`
- Rename `100-hbnb.html` to `0-hbnb.html`
- Update `0-hbnb.py` to replace the existing route to `/0-hbnb/`

```
guillaume@ubuntu:~/AirBnB_v4$ HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_dynamic.0-hbnb
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```

```
guillaume@ubuntu:~/AirBnB_v4$ curl -s -XGET http://0.0.0.0:5000/0-hbnb/ | head -6
<!DOCTYPE HTML>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" type="text/css" href="../static/styles/4-common.css?e211c9eb-7d17-4f12-85eb-4d50fa50cb1d" />
    <link rel="stylesheet" type="text/css" href="../static/styles/3-header.css?e211c9eb-7d17-4f12-85eb-4d50fa50cb1d" />
guillaume@ubuntu:~/AirBnB_v4$ curl -s -XGET http://0.0.0.0:5000/0-hbnb/ | head -6
<!DOCTYPE HTML>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" type="text/css" href="../static/styles/4-common.css?f834413e-0aa9-4767-b64a-c92db9cb1f82" />
    <link rel="stylesheet" type="text/css" href="../static/styles/3-header.css?f834413e-0aa9-4767-b64a-c92db9cb1f82" />
guillaume@ubuntu:~/AirBnB_v4$ 

```

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`
- Directory: `web_dynamic`
- File: `0-hbnb.py, templates/0-hbnb.html`


---
### 2. Select some Amenities to be comfortable!

![1](2135_1.jpg)

![2](2135_2.jpg)

![3](2135_3.jpg)

For the moment the filters section is static, let’s make it dynamic!

Replace the route 0-hbnb with 1-hbnb in the file 1-hbnb.py (based on 0-hbnb.py)

Create a new template 1-hbnb.html (based on 0-hbnb.html) and update it:

Write a JavaScript script (static/scripts/1-hbnb.js):

As example:



- Import JQuery in the `&lt;head&gt;` tag
- Import the JavaScript `static/scripts/1-hbnb.js` in the `&lt;head&gt;` tag


In 1-hbnb.html and the following HTML files, add this variable cache_id as query string to the above `&lt;script&gt;` tag
- In 1-hbnb.html and the following HTML files, add this variable cache_id as query string to the above `&lt;script&gt;` tag
- Add a `&lt;input type="checkbox"&gt;` tag to the `li` tag of each amenity
- The new checkbox must be at 10px on the left of the Amenity name
- Add to the `input` tags of each amenity (`&lt;li&gt;` tag) the attribute `data-id=":amenity_id"` =&gt; this will allow us to retrieve the Amenity ID from the DOM
- Add to the `input` tags of each amenity (`&lt;li&gt;` tag) the attribute `data-name=":amenity_name"` =&gt; this will allow us to retrieve the Amenity name from the DOM

- In 1-hbnb.html and the following HTML files, add this variable cache_id as query string to the above `&lt;script&gt;` tag

- Your script must be executed only when DOM is loaded
- You must use JQuery
- Listen for changes on each `input` checkbox tag:


if the checkbox is checked, you must store the Amenity ID in a variable (dictionary or list)
if the checkbox is unchecked, you must remove the Amenity ID from the variable 
update the `h4` tag inside the `div` Amenities with the list of Amenities checked
- if the checkbox is checked, you must store the Amenity ID in a variable (dictionary or list)
- if the checkbox is unchecked, you must remove the Amenity ID from the variable
- update the `h4` tag inside the `div` Amenities with the list of Amenities checked

- if the checkbox is checked, you must store the Amenity ID in a variable (dictionary or list)
- if the checkbox is unchecked, you must remove the Amenity ID from the variable
- update the `h4` tag inside the `div` Amenities with the list of Amenities checked

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`
- Directory: `web_dynamic`
- File: `1-hbnb.py, templates/1-hbnb.html, static/scripts/1-hbnb.js`


---
### 3. API status

![4](2135_4.jpg)

![5](2135_5.jpg)

Before requesting the HBNB API, it’s better to know the status of this one.

Update the API entry point (api/v1/app.py) by replacing the current CORS CORS(app, origins="0.0.0.0") by CORS(app, resources={r"/api/v1/*": {"origins": "*"}}).

Change the route 1-hbnb to 2-hbnb in the file 2-hbnb.py (based on 1-hbnb.py)

Create a new template 2-hbnb.html (based on 1-hbnb.html) and update it:

Write a JavaScript script (static/scripts/2-hbnb.js):

To start the API in the port 5001:

For example:



- Import the JavaScript `static/scripts/2-hbnb.js` in the `&lt;head&gt;` tag (instead of `1-hbnb.js`)
- Add a new `div` element in the `header` tag:


Attribute ID should be `api_status`
Align to the right
Circle of 40px diameter
Center vertically
At 30px of the right border
Background color #cccccc
- Attribute ID should be `api_status`
- Align to the right
- Circle of 40px diameter
- Center vertically
- At 30px of the right border
- Background color #cccccc
- Also add a class `available` for this new element in `web_dynamic/static/styles/3-header.css`:


Background color #ff545f
- Background color #ff545f

- Attribute ID should be `api_status`
- Align to the right
- Circle of 40px diameter
- Center vertically
- At 30px of the right border
- Background color #cccccc

- Background color #ff545f

- Based on `1-hbnb.js`
- Request `http://0.0.0.0:5001/api/v1/status/`:


If in the status is “OK”, add the class `available` to the `div#api_status` 
Otherwise, remove the class `available` to the `div#api_status`
- If in the status is “OK”, add the class `available` to the `div#api_status`
- Otherwise, remove the class `available` to the `div#api_status`

- If in the status is “OK”, add the class `available` to the `div#api_status`
- Otherwise, remove the class `available` to the `div#api_status`

```
guillaume@ubuntu:~/AirBnB_v4$ HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db HBNB_API_PORT=5001 python3 -m api.v1.app
...

```

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`
- File: `api/v1/app.py, web_dynamic/2-hbnb.py, web_dynamic/templates/2-hbnb.html, web_dynamic/static/styles/3-header.css, web_dynamic/static/scripts/2-hbnb.js`


---
### 4. Fetch places

Replace the route 2-hbnb with 3-hbnb in the file 3-hbnb.py (based on 2-hbnb.py)

Create a new template 3-hbnb.html (based on 2-hbnb.html) and update it:

Write a JavaScript script (static/scripts/3-hbnb.js):

The final result must be the same as previously, but now, places are loaded from the front-end, not from the back-end!

- Import the JavaScript `static/scripts/3-hbnb.js` in the `&lt;head&gt;` tag (instead of `2-hbnb.js`)
- Remove the entire Jinja section of displaying all places (all `article` tags)

- Based on `2-hbnb.js`
- Request `http://0.0.0.0:5001/api/v1/places_search/`: 


Description of this endpoint here. **If this endpoint is not available, you will have to add it to the API** (you can work all together for creating this endpoint)
Send a `POST` request with `Content-Type: application/json` and an empty dictionary in the body - cURL version: `curl "http://0.0.0.0:5001/api/v1/places_search" -XPOST -H "Content-Type: application/json" -d '{}'`
Loop into the result of the request and create an `article` tag representing a `Place` in the `section.places`. (you can remove the Owner tag in the place description)
- Description of this endpoint here. **If this endpoint is not available, you will have to add it to the API** (you can work all together for creating this endpoint)
- Send a `POST` request with `Content-Type: application/json` and an empty dictionary in the body - cURL version: `curl "http://0.0.0.0:5001/api/v1/places_search" -XPOST -H "Content-Type: application/json" -d '{}'`
- Loop into the result of the request and create an `article` tag representing a `Place` in the `section.places`. (you can remove the Owner tag in the place description)

- Description of this endpoint here. **If this endpoint is not available, you will have to add it to the API** (you can work all together for creating this endpoint)
- Send a `POST` request with `Content-Type: application/json` and an empty dictionary in the body - cURL version: `curl "http://0.0.0.0:5001/api/v1/places_search" -XPOST -H "Content-Type: application/json" -d '{}'`
- Loop into the result of the request and create an `article` tag representing a `Place` in the `section.places`. (you can remove the Owner tag in the place description)

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`
- File: `web_dynamic/3-hbnb.py, web_dynamic/templates/3-hbnb.html, web_dynamic/static/scripts/3-hbnb.js`


---
### 5. Filter places by Amenity

Replace the route 3-hbnb with 4-hbnb in the file 4-hbnb.py (based on 3-hbnb.py)

Create a new template 4-hbnb.html (based on 3-hbnb.html) and update it:

Write a JavaScript script (static/scripts/4-hbnb.js):

Now you have the first filter implemented, enjoy!

- Import the JavaScript `static/scripts/4-hbnb.js` in the `&lt;head&gt;` tag (instead of `3-hbnb.js`)

- Based on `3-hbnb.js`
- When the `button` tag is clicked, a new POST request to `places_search` should be made with the list of Amenities checked

**Repo:**

- GitHub repository: `atlas-AirBnB_clone_v4`
- File: `web_dynamic/4-hbnb.py, web_dynamic/templates/4-hbnb.html, web_dynamic/static/scripts/4-hbnb.js`