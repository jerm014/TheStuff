# Project 2382: Build a web app in JavaScript
----


For this project You will use all HTML/CSS/Accessibility/Responsive design/Bootstrap/Javascript knowledges that you learned previously.

You won’t have a lot of instruction, you are free to implement it the way that you want - the objective is simple: Have fully functional web pages that look the same as the designer file.

Here the final result:

![1](2382_1.jpg)

This webpage has been designed by Nicolas Philippot, UI/UX designer. You can find final screens[here](https://intranet-projects-files.s3.amazonaws.com/holbertonschool-webstack/623/Archive.zip)

### Requirements

* You have to use Bootstrap
* Your`styles.css`must be as small as you can -**you must use as much as you can Bootstrap classes**
* You have to use JQuery
* Your`scripts.js`must contain all your Javascript part
* Your Javascript must be executed only when the document is loaded
### Imports

For this project, you will need: fonts from Google, JQuery, Bootstrap CSS/JS

``
```
<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css?family=Coiny&display=swap" rel="stylesheet">

<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">

<link rel="stylesheet" href="styles.css">
<script src="scripts.js"></script>
```

----
## Tasks
---
### 0. Fork me if you can!

For this project you will fork this <!--plain-->[codebase](https://github.com/jzamora5/holberton-smiling-school) <!--link-->:<!--plain-->

(<!--plain-NL-->`homepage.html`<!--inline-NL--> -> <!--plain-NL-->`0-homepage.html`<!--inline-NL-->)<!--plain-NL-->

(<!--plain-NL-->`pricing.html`<!--inline-NL--> -> <!--plain-NL-->`0-pricing.html`<!--inline-NL-->)<!--plain-NL-->

(<!--plain-NL-->`courses.html`<!--inline-NL--> -> <!--plain-NL-->`0-courses.html`<!--inline-NL-->)<!--plain-NL-->

- Update the repository name to `holbertonschool-smiling-school-javascript`
- Update the `README.md`:

Add yourself as an author of the project
- Add yourself as an author of the project

Update the repository name to <!--plain-NL-->`holbertonschool-smiling-school-javascript`<!--inline-NL-->

Update the <!--plain-NL-->`README.md`<!--inline-NL-->:<!--plain-NL-->

- Add yourself as an author of the project

**Interactions note:**<!--code-NL-->

- Web pages must switch to the tablet version when the screen width is 768px
- Web pages must switch to the mobile version when the screen width is 576px
- button hover/active: `opacity: 0.9`

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `0-homepage.html, 0-pricing.html, 0-courses.html, styles.css, README.md`


---
### 1. Homepage - quotes

From <!--plain-NL-->`0-homepage.html`<!--inline-NL-->, create <!--plain-NL-->`1-homepage.html`<!--inline-NL-->.<!--plain-NL-->

Replace static quotes by dynamic loading:<!--plain-NL-->

- URL: `https://smileschool-api.hbtn.info/quotes`
- No static quotes should be present in the quotes section
- During the Ajax request, a loader should be present
- Carousel should work like before

Example of my loader:<!--plain-NL-->

```
HTML:
<div class="loader"></div>

CSS:
.loader {
    border: 10px solid #f3f3f3;
    border-top: 10px solid #C271FF;
    border-radius: 50%;
    width: 80px;
    height: 80px;
    animation: spin 2s linear infinite;
    margin: auto;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

```

Final result:<!--plain-NL-->



![1](2382_1.gif)

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `1-homepage.html`


---
### 2. Homepage - popular tutorials

From <!--plain-NL-->`1-homepage.html`<!--inline-NL-->, create <!--plain-NL-->`2-homepage.html`<!--inline-NL-->.<!--plain-NL-->

Replace static video cards by dynamic loading:<!--plain-NL-->

- URL: `https://smileschool-api.hbtn.info/popular-tutorials`
- No static video cards should be present in the section
- During the Ajax request, a loader should be present
- Carousel should work by sliding card by card (like GIF below) - this kind of carousel is not unique, make it generic to reuse it easily!
- Don’t forget the responsive part!

Final result:<!--plain-NL-->



![2](2382_2.gif)

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `2-homepage.html`


---
### 3. Homepage - latest videos

From <!--plain-NL-->`2-homepage.html`<!--inline-NL-->, create <!--plain-NL-->`homepage.html`<!--inline-NL-->.<!--plain-NL-->

Replace static video card by dynamic loading:<!--plain-NL-->

- URL: `https://smileschool-api.hbtn.info/latest-videos`
- No static video cards should be present in the section
- During the Ajax request, a loader should be present
- Carousel should work by sliding card by card (like GIF below) - this kind of carousel is not unique, make it generic to reuse it easily!
- Don’t forget the responsive part!

Final result:<!--plain-NL-->



![3](2382_3.gif)

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `homepage.html`


---
### 4. Pricing - quotes

From <!--plain-NL-->`0-pricing.html`<!--inline-NL-->, create <!--plain-NL-->`pricing.html`<!--inline-NL-->.<!--plain-NL-->

Replace static quotes by dynamic loading:<!--plain-NL-->

- URL: `https://smileschool-api.hbtn.info/quotes`
- No static quotes should be present in the quotes section
- During the Ajax request, a loader should be present
- Carousel should work like before

Same as the <!--plain-NL-->`homepage.html`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `pricing.html`


---
### 5. Courses

From <!--plain-NL-->`0-courses.html`<!--inline-NL-->, create <!--plain-NL-->`courses.html`<!--inline-NL-->.<!--plain-NL-->

Replace static video card by dynamic loading:<!--plain-NL-->

- URL: `https://smileschool-api.hbtn.info/courses`

`GET` parameters:


`q`: search value (in our case, the value of the field KEYWORDS)
`topic`: topic filter value (in our case, the value of the field TOPICS)
`sort`: order of all courses (in our case, the value of the field SORT BY)
- `GET` parameters:


`q`: search value (in our case, the value of the field KEYWORDS)
`topic`: topic filter value (in our case, the value of the field TOPICS)
`sort`: order of all courses (in our case, the value of the field SORT BY)
- `q`: search value (in our case, the value of the field KEYWORDS)
- `topic`: topic filter value (in our case, the value of the field TOPICS)
- `sort`: order of all courses (in our case, the value of the field SORT BY)
- No static video cards should be present in the section
- During the Ajax request, a loader should be present
- Dropdowns are dynamic (coming from the API):


Topic: list of `topics`
Sort by: list of `sorts`
- Topic: list of `topics`
- Sort by: list of `sorts`
- Search value should be initialized by the value `q` in the API response
- The list of video cards is coming from `courses` in the API response
- API request must be done when:


Search value is changing
A new Topic is selected
A new Sort by is selected
- Search value is changing
- A new Topic is selected
- A new Sort by is selected

- `GET` parameters:


`q`: search value (in our case, the value of the field KEYWORDS)
`topic`: topic filter value (in our case, the value of the field TOPICS)
`sort`: order of all courses (in our case, the value of the field SORT BY)
- `q`: search value (in our case, the value of the field KEYWORDS)
- `topic`: topic filter value (in our case, the value of the field TOPICS)
- `sort`: order of all courses (in our case, the value of the field SORT BY)

- `q`: search value (in our case, the value of the field KEYWORDS)
- `topic`: topic filter value (in our case, the value of the field TOPICS)
- `sort`: order of all courses (in our case, the value of the field SORT BY)

- Topic: list of `topics`
- Sort by: list of `sorts`

- Search value is changing
- A new Topic is selected
- A new Sort by is selected



![4](2382_4.gif)

**Repo:**

- GitHub repository: `atlas-smiling-school-javascript`
- File: `courses.html`