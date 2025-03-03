# Project 2353: Developer tools
----


![1](2353_1.jpeg)

In this project, you will analyze this website[https://dev-tools.hbtn.info/](https://dev-tools.hbtn.info/).

## Resources

**Read or watch**:

* [Chrome DevTools | Tools for Web Developers | Google Developers](https://developers.google.com/web/tools/chrome-devtools/)
* [Introduction | Down and Dirty with Chrome Developer Tools](https://blittle.github.io/chrome-dev-tools/)
* [Firefox Developer Tools | MDN](https://firefox-source-docs.mozilla.org/devtools-user/index.html)
* [Dev Tips - Developer Tips by Umar Hansa](https://umaar.com/dev-tips/)
* [Get Started With Viewing And Changing CSS | Tools for Web Developers](https://developers.google.com/web/tools/chrome-devtools/css)
* [Keeping it simple with the JavaScript console - LogRocket Blog](https://blog.logrocket.com/keeping-it-simple-with-the-javascript-console/)
* [Inspect Network Activity - Chrome DevTools 101](https://www.youtube.com/watch?v=e1gAyQuIFQo&feature=youtu.be)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

### General

* What Developer Tools in your browser are
* How to open the Developer Tools on Chrome, Firefox, Safari, and Edge.
* How to use the elements tab to edit HTML and CSS
* How to audit a page according to the tips suggested by Lighthouse
* How to create and run snippets on a page
* How to get information about files and server configurations
* How to block requests
* How to know how much JavaScript or CSS is used on a page
* How to detect 404 issues
* How to move elements on a webpage
## Requirements

### General

* A`README.md`file, at the root of the folder of the project, is mandatory
* Use the newest version of Google Chrome browser (`78.0.3904.70`or later).
* Screenshots can be taken via the OS, not necessary via the DevTools. These screenshots are used to see how and where you are doing/playing with the DevTools.

----
## Tasks
---
### 0. Responsive device

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Take a screenshot of the website using the device toolbar
Choose iPhone X and show the size in your screenshot (selected device or size in pixel of the rendering)<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `0-responsive_device.png`


---
### 1. Change the background color

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Change the background-color of the body to use <!--plain-NL-->`#4233bd`<!--inline-NL-->
Take a screenshot of the <!--plain-NL-->`PORTFOLIO`<!--inline-NL--> section<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `1-change_bg_color.png`


---
### 2. Force element state

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Force the hover state of the “cake” block in the section Portfolio
Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `2-pathways_menu.png`


---
### 3. Copy all the styles of the button

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Select the <!--plain-NL-->`Download me!`<!--inline-NL--> and copy all the CSS styling that is applied on this button.<!--plain-NL-->

Your answer file must contain all CSS styling one per line like this example:<!--plain-NL-->

```
$ head -2 3-button_styles
border-radius: 1px;
color: #FF00FF;
$

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `3-button_styles`


---
### 4. Change button styles

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

- All primary buttons (`btn-primary`) should have the `#0080ee` color as a background color
- All outlined buttons light (`btn-outline-light`) should have `#0020aa` for the text color
- Screenshot all buttons that changed and merge it to one image

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `4-new_buttons.png`


---
### 5. Remove part of the website

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Remove the <!--plain-NL-->`div`<!--inline-NL--> of the “cake” box in the section Portfolio<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `5-deleted_elements.png`


---
### 6. Where is it coming from?

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

- On the right panel, click on the `Computed tab`
- Then, select the `h2` with the text `ABOUT`
- Search for `margin-bottom`

Which file is that declaration coming from?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `6-declaration_file`


---
### 7. How many listeners

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

How many times click events are referenced in JavaScript files?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `7-number_of_listeners`


---
### 8. What is the HSL code

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Select the primary button “Send” <!--plain-NL-->

What is the equivalent value of the hexadecimal background-color, in HSL? <!--plain-NL-->

(format of your answer should be: <!--plain-NL-->`hsl(<VALUES>);`<!--inline-NL-->, example: <!--plain-NL-->`hsl(241, 23%, 24%);`<!--inline-NL--> following by a new line)<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `8-hsl`


---
### 9. The max-width of the container

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the <!--plain-NL-->`max-width`<!--inline-NL--> for the first <!--plain-NL-->`.container`<!--inline-NL--> in the section “About”? (your browser width must be between 1250px and 1440px and with a zoom at 100%)<!--plain-NL-->

(format of your answer should be <!--plain-NL-->`max-width: <VALUE>;`<!--inline-NL-->, example: <!--plain-NL-->`max-width: 670px`<!--inline-NL-->)<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `9-max_width`


---
### 10. Moving around

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Switch the sections of “About” and “Portfolio”<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `10-moved_around.png`


---
### 11. Coverage

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

How big, in bytes, is the <!--plain-NL-->`freelancer.css`<!--inline-NL--> file?<!--plain-NL-->

Answer file must contain the value in Byte (example: <!--plain-NL-->`6144`<!--inline-NL--> for 6KB)<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `11-coverage`


---
### 12. Emulate the print version of the webpage

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Under Rendering, change the CSS media type emulation to “print” and take a screenshot of the home page.<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `12-print_version.png`


---
### 13. Using the console

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Select the Avatar image in the header and type <!--plain-NL-->`$0`<!--inline-NL--> in the console. Enter. <!--plain-NL-->

What does it return?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `13-logo_dollar0`


---
### 14. Write code in the console

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Write in the console <!--plain-NL-->`console.log(document.title)`<!--inline-NL-->, what is returned?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `14-doc_title`


---
### 15. Holberton web framework

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Which front-end framework could we guess this page is using?<!--plain-NL-->

In your answer file only put the letter of the multiple choice answer from below:<!--plain-NL-->

- A. React JS
- B. Material Design
- C. Bootstrap
- D. Angular JS

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `15-hbtn_framework`


---
### 16. Homepage weight

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the total weight of the page (with all the elements)?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `16-weight.png`


---
### 17. Number of requests

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the number of requests done when accessing this page?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `17-requests.png`


---
### 18. Number of CSS files

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

How many CSS resources are loaded on this page?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `18-css_loaded`


---
### 19. Number of images

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

How many image resources are loaded on this page?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `19-images_loaded`


---
### 20. Favicon image type

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the <!--plain-NL-->`type`<!--inline-NL--> value of the favicon image?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `20-favicon_type`


---
### 21. Font library

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Holberton School website uses a font library for their icons, which one is it?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `21-hbtn_font_lib`


---
### 22. XHR calls

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the name of the resource that generates 1 XHR calls? <!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `22-xhr_calls`


---
### 23. Audits panel

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

What is the notation for <!--plain-NL-->`Performance`<!--inline-NL--> (for desktop mode and no throttling - also called Lighthouse)?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `23-performance_audit.png`


---
### 24. Static assets

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

How many static assets need a better cache policy?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `24-static_assets_audit.png`


---
### 25. Accessibility

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

When you run an accessibility audit, what is the contrast issue?<!--plain-NL-->

In your answer file only put the letter of the multiple choice answer from below:<!--plain-NL-->

- A. Image elements do not have [alt] attributes
- B. Links do not have a discernible name
- C. Background and foreground colors do not have a sufficient contrast ratio.

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `25-contrast_issue`


---
### 26. No alt

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Which classes are on the images that have no <!--plain-NL-->`alt`<!--inline-NL--> attribute?<!--plain-NL-->

Your answer file must contains all classes, example: <!--plain-NL-->`.my_class.my_second`<!--inline-NL--> if 2 classes<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `26-no_alt`


---
### 27. Best practices

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Which attribute is missing on all the links with the target <!--plain-NL-->`_blank`<!--inline-NL-->?<!--plain-NL-->

In your answer file only put the letter of the multiple choice answer from below:<!--plain-NL-->

- A. `rel="noopener"`
- B. `rel="noreferrer"`
- C. A and B

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `27-missing_attr`


---
### 28. SEO

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Which <!--plain-NL-->`<a>`<!--inline-NL--> links don’t have enough text description?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `28-unclear_desc.png`


---
### 29. Sources

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

The <!--plain-NL-->`sources`<!--inline-NL--> panel allow you to edit files, add breakpoints to analyse your JavaScript code and create snippets.<!--plain-NL-->

- Create a new snippet called `allcolors.js`
- Copy-paste the code on this page
- Run the code
- Take a screenshot of the result in your console

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `29-how_many_colors.png`


---
### 30. Block CSS files

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Block all CSS requests<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `30-no_css.png`


---
### 31. Application panel

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

The <!--plain-NL-->`application`<!--inline-NL--> panel gives you access to the storage (cookies, sessions, cache…) and some other options as Services Workers and more recently, notifications.<!--plain-NL-->

What is the only key present in the session storage for this page?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `31-session_storage_key`


---
### 32. Service workers

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

Does this page have any service workers? <!--plain-NL-->`Yes`<!--inline-NL--> or <!--plain-NL-->`No`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `32-service_workers`


---
### 33. Security

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

The <!--plain-NL-->`security`<!--inline-NL--> panel allows you to make sure HTTPS is properly implement on a webpage.<!--plain-NL-->

Which organization issued the SSL certificate for this page?<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `33-ssl_cert`


---
### 34. Expiration date

Go to <!--plain-NL-->`https://dev-tools.hbtn.info/`<!--inline-NL-->

When does the SSL certificate expire?<!--plain-NL-->

Take a screenshot of it<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `developer_tools`
- File: `34-ssl_expiration.png`