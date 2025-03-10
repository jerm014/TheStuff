# Project 2137: Sass & Scss
----



![1](2137_1.jpg)

## Resources

**Read or watch**:

* [Sass Basics](https://sass-lang.com/guide/)
* [Sass flow control directives: @if, @for, @each and @while](https://sass-lang.com/documentation/at-rules/control/)
* [Sass references](https://sass-lang.com/documentation/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What Sass means
* How to write Sass & Scss file
* What is the difference between Sass and Scss
* What is the Sass preprocessing
* How to declare a variable
* How to use nested definition
* How to import a Sass file
* How to use mixins
* How to declare extend/inheritance styles
* How to manipulate operators
## Requirements

### General

* Allowed editors:`vi`,`vim`,`emacs`
* All your files will be executed on Ubuntu 20.04 LTS using`Sass 1.82.0`(or higher)
* All your files should end with a new line
* All your Scss files should have a comment at the beginning (i.e. syntax above)
* All your files should start by a comment describing the task
* A`README.md`file, at the root of the folder of the project, is mandatory
* The length of your files will be tested using`wc`
## More Info

### Comments for your Scss file:

**All your Scss file must start with a comment block**

``
```
$ cat my_styles.scss
/* My style */
body {
    .container {
        color: #3D3D3D;
    }
}
$
```
### Install Sass/Scss on Ubuntu 20.04 LTS

``
```
$ curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ sudo npm install -g npm@10
$ sudo npm install -g sass@^1.82.0
$ sass --version
1.82.0 compiled with dart2js 3.5.4
```

![2](2137_2.jpg)

**Great!**You've completed the quiz successfully! Keep going!#### Question #0

What Sass means?

 * Super Awesome StyleSheets

 * Syntactically Augmented StyleSheets

 * Syntactically Awesome StyleSheets

 * Simply Awesome StyleSheets

#### Question #1

Who designed Sass?

 * Natalie Weizenbaum

 * Hampton Catlin

 * Guido van Rossum

#### Question #2

How to declare variable?

 * `var my_var`

 * `$my_var`

 * `let my_var`

 * `int my_var`

 * `const my_var`

#### Question #3

How to import a file?

 * `@import 'my_file';`

 * `@import 'my_file.scss';`

 * `#import 'my_file';`

 * `from my_file import *`

#### Question #4

How to create a �for each� loop?

 * `@for $my_item in $my_list`

 * `@foreach $my_item in $my_list`

 * `@for $my_item each in $my_list`

 * `@each $my_item in $my_list`

#### Question #5

How to create a �while� loop?

 * `@while $i is under 10`

 * `@while $i < 10`

 * `@while $i < 10 then`

 * `@for $i < 10`

#### Question #6

Does Sass allow function creation?

 * Yes

 * No


----
## Tasks
---
### 0. Always debugging!

Write a Sass file that prints <!--plain-NL-->`Hello world`<!--inline-NL--> in the debug output.<!--plain-NL-->

```
guillaume@ubuntu:~/$ sass 0-debug_log.scss | head -n 0
0-debug_log.scss:2 DEBUG: Hello world
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `0-debug_log.scss`


---
### 1. Color variable

Write a Sass file that assigns the text color <!--plain-NL-->`#3D3D3D`<!--inline-NL--> to the HTML tags <!--plain-NL-->`body`<!--inline-NL--> and <!--plain-NL-->`p`<!--inline-NL-->.<!--plain-NL-->

- You must use a Sass variable

```
guillaume@ubuntu:~/$ sass 1-color_variable.scss | tail -n +2
body {
  color: #3D3D3D; }

p {
  color: #3D3D3D; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `1-color_variable.scss`


---
### 2. Colors

Write a Sass file that assigns:<!--plain-NL-->

- The text color `#3D3D3D` to the HTML tags `body` and `p`
- The background color `#6D6D6D` to the HTML tags `body` and `h2`
- You must use 2 Sass variables

```
guillaume@ubuntu:~/$ sass 2-color_variables.scss | tail -n +2
body {
  color: #3D3D3D;
  background-color: #6D6D6D; }

p {
  color: #3D3D3D; }

h2 {
  background-color: #6D6D6D; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `2-color_variables.scss`


---
### 3. Nested tag

Write a Sass file that assigns:<!--plain-NL-->

- No margin or padding in `body` tags
- Margin `10px` to all of the `p` tags inside `body` tags
- You must use nested declarations

```
guillaume@ubuntu:~/$ sass 3-nested_tag.scss | tail -n +2
body {
  margin: 0px;
  padding: 0px; }
  body p {
    margin: 10px; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `3-nested_tag.scss`


---
### 4. Nested class

Write a Sass file that assigns:<!--plain-NL-->

- Text color `#3D3D3D` to elements inside `body` tags
- Text color `#FF0000` to any elements of class `.red` inside `body` tags
- You must use nested declarations

```
guillaume@ubuntu:~/$ sass 4-nested_class.scss | tail -n +2
body {
  color: #3D3D3D; }
  body .red {
    color: #FF0000; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `4-nested_class.scss`


---
### 5. Nested child

Write a Sass file that assigns:<!--plain-NL-->

- Text color `#3D3D3D` to elements inside `body` tags
- Text color `#FF0000` to any elements of class `.red` that are the first children of the `body`
- You must use nested declarations

```
guillaume@ubuntu:~/$ sass 5-nested_child.scss | tail -n +2
body {
  color: #3D3D3D; }
  body > .red {
    color: #FF0000; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `5-nested_child.scss`


---
### 6. Nested hover

Write a Sass file that assigns:<!--plain-NL-->

- Text color `#FF0000` to `button` tags
- When the user hovers over `button` tags, text color should change to `#00FF00`
- You must use nested declarations

```
guillaume@ubuntu:~/$ sass 6-nested_hover.scss | tail -n +2
button {
  color: #FF0000; }
  button:hover {
    color: #00FF00; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `6-nested_hover.scss`


---
### 7. Nested and nested again

Write a Sass file that assigns:<!--plain-NL-->

- Font size `14px` to all `body` tags
- Font size `16px` to all `h1` tags inside `body` tags
- Font size `12px` to `h1` tags of class `.smaller`  inside  `body` tags
- You must use nested declarations

```
guillaume@ubuntu:~/$ sass 7-nested_deeper.scss | tail -n +2
body {
  font-size: 14px; }
  body h1 {
    font-size: 16px; }
    body h1.smaller {
      font-size: 12px; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `7-nested_deeper.scss`


---
### 8. Margin mixin

Write a Sass file that assigns:<!--plain-NL-->

- Margin left and right at `10px` to `body` tags
- Margin left and right at `15px` to `div` tags
- You must use a mixin

```
guillaume@ubuntu:~/$ sass 8-mixin_margins.scss | tail -n +2
body {
  margin-left: 10px;
  margin-right: 10px; }

div {
  margin-left: 15px;
  margin-right: 15px; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `8-mixin_margins.scss`


---
### 9. Extended

Write a Sass file that assigns:<!--plain-NL-->

- Font size `12px` to all tags of class `.info`
- Text color `#00FF00` to all tags of class `.success` and extend style of the class `.info`
- Text color `#FF0000` to all tags of class `.warning` and extend style of the class `.info`

```
guillaume@ubuntu:~/$ sass 9-extend_list.scss | tail -n +2
.info, .success, .warning {
  font-size: 12px; }

.success {
  color: #00FF00; }

.warning {
  color: #FF0000; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `9-extend_list.scss`


---
### 10. Import colors

Write a Sass file that assigns:<!--plain-NL-->

- Text color `$red` from `10-colors.scss` to the class `.red`
- Text color `$green` from `10-colors.scss` to the class `.green`
- Text color `$blue` from `10-colors.scss` to the class `.blue`
- You must use `@import`

```
guillaume@ubuntu:~/$ cat 10-colors.scss
/* All my colors */
$red: #FF0000;
$green: #00FF00;
$blue: #0000FF;
guillaume@ubuntu:~/$ sass 10-import_colors.scss | tail -n +3
.red {
  color: #FF0000; }

.green {
  color: #00FF00; }

.blue {
  color: #0000FF; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `10-import_colors.scss`


---
### 11. For each

Write a Sass file that creates a class for each name in the list <!--plain-NL-->`$list-names`<!--inline-NL--> and assigns the background image based on the name (example below):<!--plain-NL-->

- You must use `@import`
- You must use `@each` statement

```
guillaume@ubuntu:~/$ cat 11-photos.scss 
/* All names */
$list-names: julien john sam damian;
guillaume@ubuntu:~/$ sass 11-loop_photos.scss | tail -n +3
.photo-julien {
  background: image-url("photos/julien.jpg") no-repeat; }

.photo-john {
  background: image-url("photos/john.jpg") no-repeat; }

.photo-sam {
  background: image-url("photos/sam.jpg") no-repeat; }

.photo-damian {
  background: image-url("photos/damian.jpg") no-repeat; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `11-loop_photos.scss`


---
### 12. Loop Headers

Write a Sass file that creates <!--plain-NL-->`H*`<!--inline-NL--> tags, where �*� is the size of the font used.<!--plain-NL-->

- `h1` must have font size equal to `1px`, `h2` must have font size equal to `2px`, etc.
- You must create `H*` tags from 1 to 5
- You must use `@for` statement

```
guillaume@ubuntu:~/$ sass 12-loop_header.scss | tail -n +2
h1 {
  font-size: 1px; }

h2 {
  font-size: 2px; }

h3 {
  font-size: 3px; }

h4 {
  font-size: 4px; }

h5 {
  font-size: 5px; }
guillaume@ubuntu:~/$ 

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `sass_scss`
- File: `12-loop_header.scss`