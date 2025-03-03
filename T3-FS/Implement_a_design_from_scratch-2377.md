# Project 2377: Implement a design from scratch
----


*For this project, we expect you to look at this concept:*

* [Implement a design](/concepts/963)

In this project, you will implement from scratch, without any library, a web page. You will use all HTML/CSS/Accessibility/Responsive design knowledges that you learned previously.

You won’t have a lot of instruction, you are free to implement it the way that you want - the objective is simple: Have a fully functional web page that looks the same as the designer file.

Here the final result:

![1](2377_1.jpg)

This webpage has been designed by Nicolas Philippot, UI/UX designer. You can find final screens[here](https://intranet-projects-files.s3.amazonaws.com/holbertonschool-webstack/622/Archive.zip)

### Requirements

* you are not allowed to import external CSS framework (like Bootstrap)
* you are not to use Javascript

----
## Tasks
---
### 0. Read and be familiar with Figma

Create an account in <!--plain-->[Figma](https://www.figma.com/) <!--link--> and open this <!--plain-->[project](https://www.figma.com/file/FfnVADRC9xgI3yiZliTBYZ/Holberton-School---Headphone-company) <!--link--> and “Duplicate to your Drafts” to have access to all design details.<!--plain-->

If you can’t access to it, please find here the <!--plain-->[Figma file](https://intranet-projects-files.s3.amazonaws.com/holbertonschool-webstack/Holberton+School+-+Headphone+company.fig) <!--link-->



![1](2377_1.png)

Important notes with Figma:<!--plain-NL-->

- if your computer doesn’t have missing fonts, you can find them here: source-sans-pro and Spin-Cycle-OT
- some values are in float - feel free to round them

For this task, please write an amazing <!--plain-NL-->`README.md`<!--inline-NL-->

**Interactions note:**<!--code-NL-->

- the web page must switch to the mobile version when the screen width is 480px or less
- links hover/active: `#FF6565`
- button hover/active: `opacity: 0.9`
- max width of the content: 1000px centered in the page

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `README.md`


---
### 1. Header

Building a web page the right way, is not easy - expect if you put in place strong foundations:<!--plain-NL-->

- reset CSS styling
- use variables
- simple/“as generic as you can” CSS selectors
- avoid using super specific CSS selectors as much as possible
- simple HTML structure - `div` containers are your friend!

Last advice: Personally, I always start to build a web page from outside to inside and from top to bottom. 
But you can try to other way - it’s fine - but you should structure the way that you will implement a component and not get lost with HTML tags.<!--plain-NL-->

Now, your turn!<!--plain-NL-->

For this first task: <!--plain-NL-->**create the header/hero piece**<!--code-NL-->

Here an archive of all assets needed: <!--plain-->[images_.zip](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2020/3/d1597894d79386c83b9b.zip?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20250303%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20250303T182941Z&X-Amz-Expires=345600&X-Amz-SignedHeaders=host&X-Amz-Signature=8a9f776163c0b554e7f40c4af94e6f6f357df0f212b21e937768d4cc3f2241f2) <!--link-->

**Desktop:**<!--code-NL-->



![1](2377_1.gif)

**Mobile:**<!--code-NL-->



![2](2377_2.gif)

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `0-index.html, 0-styles.css`


---
### 2. "What we do..." section

Copy files from the previous task.<!--plain-NL-->

For this second task: <!--plain-NL-->**create the “What we do…” section**<!--code-NL-->

In this section, you will need custom font icons. Here the archive of it: <!--plain-->[holberton_school-icon.zip](https://s3.eu-west-3.amazonaws.com/hbtn.intranet/uploads/misc/2020/3/7159d988278de54d859d.zip?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4MYA5JM5DUTZGMZG%2F20250303%2Feu-west-3%2Fs3%2Faws4_request&X-Amz-Date=20250303T182941Z&X-Amz-Expires=345600&X-Amz-SignedHeaders=host&X-Amz-Signature=36025a35869b8e57ba93ebb07aac8f33ab8f2b8f341d2fded399c6f758430c5c) <!--link--> 
Inside you will find demo page of how to use it.<!--plain-->

**Important:**<!--code-NL--> try to build as generic as you can… you will probably need some components in next section.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `1-index.html, 1-styles.css`


---
### 3. "Our results" section

Copy files from the previous task.<!--plain-NL-->

For this third task: <!--plain-NL-->**create the “Our results” section**<!--code-NL-->

Now you can reuse components form the previous task!<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `2-index.html, 2-styles.css`


---
### 4. Contact us

Copy files from the previous task.<!--plain-NL-->

A good landing page has always a contact form.<!--plain-NL-->

You are free to add any animations and/or constraints on fields.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `3-index.html, 3-styles.css`


---
### 5. Footer

Copy files from the previous task.<!--plain-NL-->

Last piece of the page… the Footer!<!--plain-NL-->

When you are done, here the result:<!--plain-NL-->

**Desktop:**<!--code-NL-->



![3](2377_3.gif)

**Mobile:**<!--code-NL-->



![4](2377_4.gif)

And you are done! <!--plain-NL-->

**Good job!**<!--code-NL-->

**Repo:**

- GitHub repository: `atlas-headphones`
- File: `4-index.html, 4-styles.css`