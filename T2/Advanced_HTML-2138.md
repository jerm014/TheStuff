# Project 2138: Advanced HTML
----

* [Quiz](#quiz)

*For this project, we expect you to look at this concept:*

* [HTML - elements of a web page](/concepts/870)

![1](2138_1.jpg)

# Welcome!

In this project, you will learn how to use HTML tags to structure a web page. No CSS, no styling - don’t worry, the final page will be “ugly” it’s normal, it’s not the purpose of this project.

Important note:**details are important!**lowercase vs uppercase / wrong letter… be careful!

## Resources

**Read or watch**:

* [HTML 5.2](https://html.spec.whatwg.org/multipage/)
* [HTML: HyperText Markup Language | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [HTML Reference - A free guide to all HTML elements and attributes](https://htmlreference.io/)
* [Can I use… Support tables for HTML5, CSS3, etc](https://caniuse.com/)
* [HTML Cheat Sheet - WebsiteSetup](https://websitesetup.org/html5-cheat-sheet/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* Which guidelines to follow for HTML
* How to create the skeleton of an HTML5 page
* How to use semantic HTML tags to structure a web page
* Which use cases to use`div`vs`span`
* The semantic value’s of`header`,`main`,`footer`,`article`,`nav`,`section`,`aside`
* How to use headings (and why it’s important to follow the hierarchical order)
* How to make lists in HTML
* The differences between medias (SVG, GIF, PNG, JPG)
* How to structure data in a table
* How to integrate a video in a webpage
* How to integrate an audio file in a webpage
* How to embed external content
* How to correctly structure an HTML page
## Requirements

* A`README.md`file at the root of the folder of the project is mandatory
* Your code should be W3C compliant and validate with[W3C-Validator](https://github.com/hs-hq/W3C-Validator)
* `Techium`will be the name of the company we will use across our webpages.
## Sitemap of the project

![1](2138_1.png)

## Wireframe of`Techium`project

![2](2138_2.png)

**Great!**You've completed the quiz successfully! Keep going!#### Question #0

Which information can we find in the tag`head`? Please select all correct answers

 * metadata

 * navigation

 * link to Twitter

 * link to stylesheets

#### Question #1

Which tag should we use to change the browser tab text?

 * `<head>`

 * `<title>`

 * `<tab>`

 * `<browser>`

#### Question #2

How many levels are available in HTML5 for section headings?

 * 1

 * 2

 * 4

 * 6

 * 8

 * 10

#### Question #3

Which tag should we use to draw an horizontal line? (usually used to separate topics in a paragraph)

 * `<line>`

 * `<br>`

 * `<break>`

 * `<hr>`

#### Question #4

Which tag should we use to group elements in an unordered list?

 * `<li>`

 * `<ul>`

 * `<ol>`

 * `<table>`

 * `<unordered list>`

 * `<list>`

#### Question #5

Which tag should we use to create an hyperlink?

 * `<link>`

 * `<to>`

 * `<p>`

 * `<div>`

 * `<a>`

#### Question #6

Which tag should we use to change the font weight of a text?
Please select all correct answers
 * `<h1>`

 * `<b>`

 * `<i>`

 * `<em>`

 * `<strong>`

 * `<bold>`

#### Question #7

Which tag should we use to embed an image?

 * `<img>`

 * `<iframe>`

 * `<div>`

 * `<caption>`

#### Question #8

Which tag should we use to embed another website?

 * `<div>`

 * `<a>`

 * `<iframe>`

 * `<p>`

 * `<code>`


----
## Tasks
---
### 0. Create your first webpage

Create your first HTML file 0-index.html with:

W3C won’t pass - you can ignore it

- Add the doctype on the first line (without any comment)
- After the doctype, open and close a `html` tag
- Add the language tag, specify English for ISO language code and add the direction tag (ltr or rtl) on the `html` tag.
- Open your file in your browser (the page should be blank)

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `0-index.html`


---
### 1. Structure your webpage

Copy the content of 0-index.html into 1-index.html

Create the head and body sections

W3C won’t pass - you can ignore it

- inside the `html` tag, create the `head` and `body` tags (empty) in this order

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `1-index.html`


---
### 2. The head - meta charset, viewport, title, description, favicons

![2](2138_2.jpg)

Copy the content of 1-index.html into 2-index.html



Meta charset:

Viewport:

Title:

Description:

Favicons:

- add a `meta` tag inside the `head`:


add the `charset` attribute with the value `utf-8`
- add the `charset` attribute with the value `utf-8`

- add the `charset` attribute with the value `utf-8`

- add a `meta` tag inside the `head`:


add an attribute `name` on the tag and specify that it is the meta `viewport`
add the key `width` with the value `device-width`
add the key `initial-scale` with the value `1.0`
add the key `viewport-fit` with the value `cover`
- add an attribute `name` on the tag and specify that it is the meta `viewport`
- add the key `width` with the value `device-width`
- add the key `initial-scale` with the value `1.0`
- add the key `viewport-fit` with the value `cover`

- add an attribute `name` on the tag and specify that it is the meta `viewport`
- add the key `width` with the value `device-width`
- add the key `initial-scale` with the value `1.0`
- add the key `viewport-fit` with the value `cover`

- add the `title` tag just after the meta viewport with value: `Homepage - Techium`

- add a `meta` tag inside the `head` section


add an attribute `name` on the tag and specify that is the meta `description`
add another attribute called `content`
add the following description: `Techium is a digital agency`
- add an attribute `name` on the tag and specify that is the meta `description`
- add another attribute called `content`
- add the following description: `Techium is a digital agency`

- add an attribute `name` on the tag and specify that is the meta `description`
- add another attribute called `content`
- add the following description: `Techium is a digital agency`

- download the image above to use as a favicon
- Use the tool at https://realfavicongenerator.net/ to generate all the favicon formats
- take the `favicon.ico` and `favicon.png` and place these at the root of your project directory, so that it is siblings with your `[0-9]+-index.html` files.
- inside the `head`, create 2 `link` tags with these 3 attributes: `rel`, `type`, and `href`.


the first `link` tag:


rel: `icon`
type: `image/x-icon`
href: `./favicon.ico`

the second `link` tag:


rel: `icon`
type: `image/png`
href: `./favicon.png`
- the first `link` tag:


rel: `icon`
type: `image/x-icon`
href: `./favicon.ico`
- rel: `icon`
- type: `image/x-icon`
- href: `./favicon.ico`
- the second `link` tag:


rel: `icon`
type: `image/png`
href: `./favicon.png`
- rel: `icon`
- type: `image/png`
- href: `./favicon.png`

- the first `link` tag:


rel: `icon`
type: `image/x-icon`
href: `./favicon.ico`
- rel: `icon`
- type: `image/x-icon`
- href: `./favicon.ico`
- the second `link` tag:


rel: `icon`
type: `image/png`
href: `./favicon.png`
- rel: `icon`
- type: `image/png`
- href: `./favicon.png`

- rel: `icon`
- type: `image/x-icon`
- href: `./favicon.ico`

- rel: `icon`
- type: `image/png`
- href: `./favicon.png`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `2-index.html`


---
### 3. Simple header, main, footer

Copy the content of 2-index.html into 3-index.html

Header:

Main:

Footer:

- create the `header` of your page between the open and close `body` tag
- put the text `Header` inside the header

- create the `main` tag after the `header` tag


put the text `Main content` inside your `main` tags
- put the text `Main content` inside your `main` tags

- put the text `Main content` inside your `main` tags

- create the `footer` tag after the `main` tag


put the text `Footer` inside the `footer` tags
- put the text `Footer` inside the `footer` tags

- put the text `Footer` inside the `footer` tags

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `3-index.html`


---
### 4. Aside

Copy the contents of 3-index.html into article.html

- change the `&lt;title&gt;` to put: `Article - Techium`
- inside the `main` tags


after the text, create the `aside` tags with text `Aside`
- after the text, create the `aside` tags with text `Aside`

- after the text, create the `aside` tags with text `Aside`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `article.html`


---
### 5. Section

Copy the content of 3-index.html into 5-index.html

Does not need to pass W3C

- inside your `&lt;main&gt;` section


remove the text in `main`, create these sections:


create first section and put the text `Hero section` inside
create second section and put the text `Services section` inside
create third section and put the text `Works section` inside
create fourth section and put the text `About section` inside
create fifth section and put the text `Latest news section` inside
create sixth section and put the text `Testimonials section` inside
create seventh section and put the text `Contact section` inside
- remove the text in `main`, create these sections:


create first section and put the text `Hero section` inside
create second section and put the text `Services section` inside
create third section and put the text `Works section` inside
create fourth section and put the text `About section` inside
create fifth section and put the text `Latest news section` inside
create sixth section and put the text `Testimonials section` inside
create seventh section and put the text `Contact section` inside
- create first section and put the text `Hero section` inside
- create second section and put the text `Services section` inside
- create third section and put the text `Works section` inside
- create fourth section and put the text `About section` inside
- create fifth section and put the text `Latest news section` inside
- create sixth section and put the text `Testimonials section` inside
- create seventh section and put the text `Contact section` inside

- remove the text in `main`, create these sections:


create first section and put the text `Hero section` inside
create second section and put the text `Services section` inside
create third section and put the text `Works section` inside
create fourth section and put the text `About section` inside
create fifth section and put the text `Latest news section` inside
create sixth section and put the text `Testimonials section` inside
create seventh section and put the text `Contact section` inside
- create first section and put the text `Hero section` inside
- create second section and put the text `Services section` inside
- create third section and put the text `Works section` inside
- create fourth section and put the text `About section` inside
- create fifth section and put the text `Latest news section` inside
- create sixth section and put the text `Testimonials section` inside
- create seventh section and put the text `Contact section` inside

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `5-index.html`


---
### 6. Work, News, Testimonial articles

Copy the content of 5-index.html into 6-index.html

Work articles:

News articles:

Testimonial articles:

W3C won’t pass - you can ignore it

- inside the section `Works section`

add 3 `article` tags


inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)
- add 3 `article` tags


inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)

- add 3 `article` tags


inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)

- inside each `article` write `Work #` where the hashtag will be the ordered number (1, 2, or 3)

- inside the section `Latest news section`

add 3 `article` tags


inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)
- add 3 `article` tags


inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)

- add 3 `article` tags


inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)

- inside each `article` write `Article #` where the hashtag will be the ordered number (1, 2, or 3)

- inside the section `Testimonials section`

add 3 `article` tags


inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)
- add 3 `article` tags


inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)

- add 3 `article` tags


inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)
- inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)

- inside each `article` write `Testimonial #` where the hashtag will be the ordered number (1, 2, or 3)

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `6-index.html`


---
### 7. Navigation

Copy the content of 6-index.html into 7-index.html

Does not need to pass W3C

- remove the `Header` text inside the `&lt;header&gt;`
- create the `nav` tag inside the `header` tag


it should remain empty for now
- it should remain empty for now

- it should remain empty for now

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `7-index.html`


---
### 8. Level 1 headings

Copy the content of 7-index.html into 8-index.html

Does not need to pass W3C

- create the level 1 heading inside your `main` before your sections


put text `Homepage` in your heading tag
- put text `Homepage` in your heading tag

- put text `Homepage` in your heading tag

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `8-index.html`


---
### 9. Level 2 headings

Copy the content of 8-index.html into 9-index.html

W3C won’t pass - you can ignore it

- in the `section` tag with the the text `Hero section`, remove the text and create a level 2 heading with text `We help you build your brand!`
- in the `section` tag with the the text `Services section`, remove the text and create a level 2 heading with text `Services`
- in the `section` tag with the the text `Works section`, remove the text and create a level 2 heading with text `Works`
- in the `section` tag with the the text `About section`, remove the text and create a level 2 heading with text `About Us`
- in the `section` tag with the the text `Latest news section`, remove the text and create a level 2 heading with text `Latest news`
- in the `section` tag with the the text `Testimonials section`, remove the text and create a level 2 heading with text `Testimonials`
- in the `section` tag with the the text `Contact section`, remove the text and create a level 2 heading with text `Contact`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `9-index.html`


---
### 10. Level 3 headings

Copy the content of 9-index.html into 10-index.html

Services headings:

Works headings:

About Us headings:

Latest news headings:

W3C does not need to pass here

- Inside the section containing the `h2` heading `Services`, add these elements right after the `h2`:


create a level 3 heading with text `Design &amp; Concept`
create a level 3 heading with text `Digital Strategy`
create a level 3 heading with text `Content Strategy`
create a level 3 heading with text `UX Design`
create a level 3 heading with text `Web Development`
create a level 3 heading with text `Social Media`
- create a level 3 heading with text `Design &amp; Concept`
- create a level 3 heading with text `Digital Strategy`
- create a level 3 heading with text `Content Strategy`
- create a level 3 heading with text `UX Design`
- create a level 3 heading with text `Web Development`
- create a level 3 heading with text `Social Media`

- create a level 3 heading with text `Design &amp; Concept`
- create a level 3 heading with text `Digital Strategy`
- create a level 3 heading with text `Content Strategy`
- create a level 3 heading with text `UX Design`
- create a level 3 heading with text `Web Development`
- create a level 3 heading with text `Social Media`

- Inside the section containing the `h2` heading `Works`:


in the first `article`, replace the text with a level 3 heading with text `Interior Design`
in the second `article`, replace the text with a level 3 heading with text `Web Development`
in the third `article`, replace the text with a level 3 heading with text `Personal Brand`
- in the first `article`, replace the text with a level 3 heading with text `Interior Design`
- in the second `article`, replace the text with a level 3 heading with text `Web Development`
- in the third `article`, replace the text with a level 3 heading with text `Personal Brand`

- in the first `article`, replace the text with a level 3 heading with text `Interior Design`
- in the second `article`, replace the text with a level 3 heading with text `Web Development`
- in the third `article`, replace the text with a level 3 heading with text `Personal Brand`

- Inside the section containing the `h2` heading `About Us`, after the `h2` heading, create these elements in this order:


 a level 3 heading with text `Who are we`
 a level 3 heading with text `Our culture`
 a level 3 heading with text `How we work`
- a level 3 heading with text `Who are we`
- a level 3 heading with text `Our culture`
- a level 3 heading with text `How we work`

- a level 3 heading with text `Who are we`
- a level 3 heading with text `Our culture`
- a level 3 heading with text `How we work`

- Inside the section containing the `h2` heading `Latest news`:


in the first `article` replace the text with a level 3 heading with text `Hoc loco tenere se Triarius non potuit.`
in the second `article` replace the text with a level 3 heading with text `Ut alios omittam, hunc appello, quem ille unum secutus est.`
in the third `article` replace the text with a level 3 heading with text `Bestiarum vero nullum iudicium puto.`
- in the first `article` replace the text with a level 3 heading with text `Hoc loco tenere se Triarius non potuit.`
- in the second `article` replace the text with a level 3 heading with text `Ut alios omittam, hunc appello, quem ille unum secutus est.`
- in the third `article` replace the text with a level 3 heading with text `Bestiarum vero nullum iudicium puto.`

- in the first `article` replace the text with a level 3 heading with text `Hoc loco tenere se Triarius non potuit.`
- in the second `article` replace the text with a level 3 heading with text `Ut alios omittam, hunc appello, quem ille unum secutus est.`
- in the third `article` replace the text with a level 3 heading with text `Bestiarum vero nullum iudicium puto.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `10-index.html`


---
### 11. styleguide

Copy the content of 3-index.html into 11-styleguide.html

- change the title to `Styleguide - Techium`
- remove the text from `header`, `main`, and `footer`
- create a new `&lt;section&gt;` inside your `main` tag


create a `header` in this `section`

in the `header` add a level 2 heading with text `Headings`

after the `header`:


add a level 1 heading with text `Heading level 1`
add a level 2 heading with text `Heading level 2`
add a level 3 heading with text `Heading level 3`
add a level 4 heading with text `Heading level 4`
add a level 5 heading with text `Heading level 5`
add a level 6 heading with text `Heading level 6`
- create a `header` in this `section`

in the `header` add a level 2 heading with text `Headings`
- in the `header` add a level 2 heading with text `Headings`
- after the `header`:


add a level 1 heading with text `Heading level 1`
add a level 2 heading with text `Heading level 2`
add a level 3 heading with text `Heading level 3`
add a level 4 heading with text `Heading level 4`
add a level 5 heading with text `Heading level 5`
add a level 6 heading with text `Heading level 6`
- add a level 1 heading with text `Heading level 1`
- add a level 2 heading with text `Heading level 2`
- add a level 3 heading with text `Heading level 3`
- add a level 4 heading with text `Heading level 4`
- add a level 5 heading with text `Heading level 5`
- add a level 6 heading with text `Heading level 6`

- create a `header` in this `section`

in the `header` add a level 2 heading with text `Headings`
- in the `header` add a level 2 heading with text `Headings`
- after the `header`:


add a level 1 heading with text `Heading level 1`
add a level 2 heading with text `Heading level 2`
add a level 3 heading with text `Heading level 3`
add a level 4 heading with text `Heading level 4`
add a level 5 heading with text `Heading level 5`
add a level 6 heading with text `Heading level 6`
- add a level 1 heading with text `Heading level 1`
- add a level 2 heading with text `Heading level 2`
- add a level 3 heading with text `Heading level 3`
- add a level 4 heading with text `Heading level 4`
- add a level 5 heading with text `Heading level 5`
- add a level 6 heading with text `Heading level 6`

- in the `header` add a level 2 heading with text `Headings`

- add a level 1 heading with text `Heading level 1`
- add a level 2 heading with text `Heading level 2`
- add a level 3 heading with text `Heading level 3`
- add a level 4 heading with text `Heading level 4`
- add a level 5 heading with text `Heading level 5`
- add a level 6 heading with text `Heading level 6`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `11-styleguide.html`


---
### 12. Paragraphs

Copy the content of 10-index.html into 12-index.html

About Us paragraphs:

Latest news paragraphs:

Contact paragraph:

Additional paragraphs:

Does not need to pass W3C

- in the `About Us` section


after the first `h3` (who are we) create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
after the second `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
after the third `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
- after the first `h3` (who are we) create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
- after the second `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
- after the third `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`

- after the first `h3` (who are we) create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
- after the second `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`
- after the third `h3` create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!`

- in the `Latest news` section


in the first `article`

create a paragraph with text `Career` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading

in the second `article`

create a paragraph with text `Digital Life` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading

in the third `article`

create a paragraph with text `Social` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading
- in the first `article`

create a paragraph with text `Career` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading
- create a paragraph with text `Career` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading
- in the second `article`

create a paragraph with text `Digital Life` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading
- create a paragraph with text `Digital Life` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading
- in the third `article`

create a paragraph with text `Social` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading
- create a paragraph with text `Social` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading

- in the first `article`

create a paragraph with text `Career` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading
- create a paragraph with text `Career` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading
- in the second `article`

create a paragraph with text `Digital Life` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading
- create a paragraph with text `Digital Life` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading
- in the third `article`

create a paragraph with text `Social` before the heading
create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading
- create a paragraph with text `Social` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading

- create a paragraph with text `Career` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?` after the heading

- create a paragraph with text `Digital Life` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?` after the heading

- create a paragraph with text `Social` before the heading
- create a paragraph with text `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.` after the heading

- in the `Contact` section after the heading


create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?`
- create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?`

- create a paragraph with the text: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?`

- below the level 2 `Services` heading add a paragraph with text `We work with you`
- below the level 2 `Works` heading add a paragraph with text `Take a look in our portfolio`
- below the level 2 `About Us` heading add a paragraph with text `Everything about us`
- below the level 2 `Testimonials` heading add a paragraph with text `We are more than a digital company`
- below the level 2 `Contact` heading add a paragraph with text `We like to know new people`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `12-index.html`


---
### 13. styleguide paragraphs

Copy the contents of 11-styleguide.html into 13-styleguide.html

- After the existing section containing `Headings`, create a new `section` in `main`

in this section create a `header`

Inside the header, create a level 2 heading with text `Paragraph`

after the `header` add a level 2 heading with text `Heading with a subtitle`
after the level 2 heading, add a paragraph with text `This is my subtitle`
after the last paragraph, add another paragraph with text: `Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.`
- in this section create a `header`

Inside the header, create a level 2 heading with text `Paragraph`
- Inside the header, create a level 2 heading with text `Paragraph`
- after the `header` add a level 2 heading with text `Heading with a subtitle`
- after the level 2 heading, add a paragraph with text `This is my subtitle`
- after the last paragraph, add another paragraph with text: `Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.`

- in this section create a `header`

Inside the header, create a level 2 heading with text `Paragraph`
- Inside the header, create a level 2 heading with text `Paragraph`
- after the `header` add a level 2 heading with text `Heading with a subtitle`
- after the level 2 heading, add a paragraph with text `This is my subtitle`
- after the last paragraph, add another paragraph with text: `Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.`

- Inside the header, create a level 2 heading with text `Paragraph`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `13-styleguide.html`


---
### 14. Span

Copy the contents of 12-index.html into 14-index.html

In the very first <header>,

Does not need to pass W3C

- before the `nav`, create a `span` with the text `Techium`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `14-index.html`


---
### 15. Div

Copy the contents of 14-index.html into 15-index.html

W3C does not need to pass

- Wrap the contents of the `header` element with a `div`
- Wrap the content of each `section` element within a `div`
- Finally, wrap the contents of the `&lt;footer&gt;` tag with a `div`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `15-index.html`


---
### 16. Structure your sections

Copy the contents of 15-index.html into 16-index.html

W3C does not need to pass

- in the `div` in the Services `section`

create a `header` tag that wraps the `h2` and the `p`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content
- in the `div` in the Works `section`

create a `header` tag that wraps the `h2` and the `p`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content
- in the `div` in the About Us `section`

create a `header` tag that wraps the `h2` and the `p`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content
- in the `div` in the Latest news `section`

create a `header` tag that wraps the `h2`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2`
- create a `div` sibling to the `header` that wraps the rest of the content
- in the `div` in the Testimonials `section`

create a `header` tag that wraps the `h2` and the `p`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content
- in the `div` in the Contact `section`

create a `header` tag that wraps the `h2` and the first `p`
create a `div` sibling to the `header` that wraps the rest of the content
- create a `header` tag that wraps the `h2` and the first `p`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2` and the `p`
- create a `div` sibling to the `header` that wraps the rest of the content

- create a `header` tag that wraps the `h2` and the first `p`
- create a `div` sibling to the `header` that wraps the rest of the content

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `16-index.html`


---
### 17. Comments

Copy the content of 16-index.html into 17-index.html

Does not need to pass W3C

- before the `header` add a line break and a comment saying `Header` to help with scanning your code
- before the `main` add a line break and a comment saying `Main` to help with scanning your code
- before the `footer` add a line break and a comment saying `Footer` to help with scanning your code
- before the `Hero section` add a line break and a comment saying `Hero section`
- before the `Services section` add a line break and a comment saying `Services section`
- before the `Works section` add a line break and a comment saying `Works section`
- before the `About Us section` add a line break and a comment saying `About Us section`
- before the `Latest news section` add a line break and a comment saying `Latest news section`
- before the `Testimonials section` add a line break and a comment saying `Testimonials section`
- before the `Contact section` add a line break and a comment saying `Contact section`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `17-index.html`


---
### 18. link your logo

Copy the content of 17-index.html into 18-index.html

W3C does not need to pass

- in the `header`, wrap the `span` with a link that redirects to the page at the root of your folder (`/`)
- wrap the link with a `div`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `18-index.html`


---
### 19. Create new pages

Copy the content of 18-index.html into about.html, latest_news.html and contact.html

Does not need to pass W3C

- change the title of `about.html` to replace `Homepage` with `About`
- change the title of `latest_news.html` to replace `Homepage` with `Latest news`
- change the title of `contact.html` to replace `Homepage` with `Contact`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `about.html, latest_news.html, contact.html`


---
### 20. Add links

Copy the content of 18-index.html into 20-index.html

For now, the anchor links will not work. We will make them work in the CSS project.

Does not need to pass W3C

- in your `nav` tags


create a link to `/` with the text `Home`
create an anchor to `services` with the text `Services`
create an anchor to `works` with the text `Works`
create an anchor to `about` with the text `About`
create an anchor to `latest_news` with the text `Latest news`
create an anchor to `testimonials` with the text `Testimonials`
create an anchor to `contact` with the text `Contact`
- create a link to `/` with the text `Home`
- create an anchor to `services` with the text `Services`
- create an anchor to `works` with the text `Works`
- create an anchor to `about` with the text `About`
- create an anchor to `latest_news` with the text `Latest news`
- create an anchor to `testimonials` with the text `Testimonials`
- create an anchor to `contact` with the text `Contact`

- create a link to `/` with the text `Home`
- create an anchor to `services` with the text `Services`
- create an anchor to `works` with the text `Works`
- create an anchor to `about` with the text `About`
- create an anchor to `latest_news` with the text `Latest news`
- create an anchor to `testimonials` with the text `Testimonials`
- create an anchor to `contact` with the text `Contact`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `20-index.html`


---
### 21. Add social media links

Copy the content of 20-index.html into 21-index.html

W3C won’t pass - you can ignore it

- in the `div` in the `footer`

remove any text you have
create a link to `https://www.facebook.com/HolbertonSchool/` with the text `Facebook`
create a link to `https://twitter.com/holbertonschool` with the text `Twitter`
create a link to `https://www.instagram.com/holbertonschool/` with the text `Instagram`
- remove any text you have
- create a link to `https://www.facebook.com/HolbertonSchool/` with the text `Facebook`
- create a link to `https://twitter.com/holbertonschool` with the text `Twitter`
- create a link to `https://www.instagram.com/holbertonschool/` with the text `Instagram`

- remove any text you have
- create a link to `https://www.facebook.com/HolbertonSchool/` with the text `Facebook`
- create a link to `https://twitter.com/holbertonschool` with the text `Twitter`
- create a link to `https://www.instagram.com/holbertonschool/` with the text `Instagram`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `21-index.html`


---
### 22. "Button" links

Copy the content of 21-index.html into 22-index.html

Does not need to pass W3C

- in the Hero `section`, after the heading


create a link to `#` with the text `Get started`
- create a link to `#` with the text `Get started`
- in the About Us `section`, after the `div` containing the level 3 headings and paragraphs


create a link to `about.html` with the text `Learn more about us`
- create a link to `about.html` with the text `Learn more about us`
- in the Contact `section`, after the `div` containing the paragraph


create a link to `contact.html` with text `Get in touch`
- create a link to `contact.html` with text `Get in touch`

- create a link to `#` with the text `Get started`

- create a link to `about.html` with the text `Learn more about us`

- create a link to `contact.html` with text `Get in touch`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `22-index.html`


---
### 23. Services, Works, Latest news links

Copy the content of 22-index.html into 23-index.html

Does not need to pass W3C

- in the Services `section`

in each level 3 heading, create a link to `#` around the text already in the heading
- in each level 3 heading, create a link to `#` around the text already in the heading
- in the Works `section`

in each level 3 heading, create a link to `#` around the text already in the heading
- in each level 3 heading, create a link to `#` around the text already in the heading
- in the Latest news `section`

in each level 3 heading, create a link to `#` around the text already in the heading
- in each level 3 heading, create a link to `#` around the text already in the heading

- in each level 3 heading, create a link to `#` around the text already in the heading

- in each level 3 heading, create a link to `#` around the text already in the heading

- in each level 3 heading, create a link to `#` around the text already in the heading

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `23-index.html`


---
### 24. List the links

Copy the content of 23-index.html into 24-index.html

W3C does not need to pass

- in the `nav`

create an unordered list, put each anchor tag (Home, Services, Works, …) as an individual list item
- create an unordered list, put each anchor tag (Home, Services, Works, …) as an individual list item
- in the `div` in the `footer`

create an unordered list and put each anchor tag (Facebook, Twitter, …) as an individual list item
- create an unordered list and put each anchor tag (Facebook, Twitter, …) as an individual list item

- create an unordered list, put each anchor tag (Home, Services, Works, …) as an individual list item

- create an unordered list and put each anchor tag (Facebook, Twitter, …) as an individual list item

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `24-index.html`


---
### 25. Secondary navigation menu

Copy the content of 24-index.html into 25-index.html

- inside the `footer`, after the `div`

create a new `div`
in the new `div` create an unordered list with the following links:


link to `#` with text `Terms of Use`
link to `#` with text `Privacy Policy`
link to `#` with text `Cookie Policy`
- create a new `div`
- in the new `div` create an unordered list with the following links:


link to `#` with text `Terms of Use`
link to `#` with text `Privacy Policy`
link to `#` with text `Cookie Policy`
- link to `#` with text `Terms of Use`
- link to `#` with text `Privacy Policy`
- link to `#` with text `Cookie Policy`

- create a new `div`
- in the new `div` create an unordered list with the following links:


link to `#` with text `Terms of Use`
link to `#` with text `Privacy Policy`
link to `#` with text `Cookie Policy`
- link to `#` with text `Terms of Use`
- link to `#` with text `Privacy Policy`
- link to `#` with text `Cookie Policy`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `25-index.html`


---
### 26. Examples of lists for the styleguide

Copy the content of 13-styleguide.html into 26-styleguide.html

Example of unordered list:

Example of ordered list:

Example of definition list:

- inside `main` after Paragraph `section`, add :


a new line and a comment with text `Lists`
after, create a new `section` with inside:


create a `header` with inside a level 2 heading with the text `Lists`
after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- a new line and a comment with text `Lists`
- after, create a new `section` with inside:


create a `header` with inside a level 2 heading with the text `Lists`
after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- create a `header` with inside a level 2 heading with the text `Lists`
- after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`

- a new line and a comment with text `Lists`
- after, create a new `section` with inside:


create a `header` with inside a level 2 heading with the text `Lists`
after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- create a `header` with inside a level 2 heading with the text `Lists`
- after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`

- create a `header` with inside a level 2 heading with the text `Lists`
- after the new `header`, create a `div` with inside:


a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`

- a level 3 heading with text `Unordered`

under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`
- under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`

- under it, add an unordered list with these items: `Dolor pulvinar etiam magna etiam.`, `Sagittis adipiscing lorem eleifend.`, `Felis enim feugiat dolore viverra.`

- after previous unordered list, in the same `div`

add a level 3 heading with text `Ordered`

add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- add a level 3 heading with text `Ordered`

add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- `Dolor pulvinar etiam magna etiam.`
- `Sagittis adipiscing lorem eleifend.`
- `Felis enim feugiat dolore viverra.`

- add a level 3 heading with text `Ordered`

add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- `Dolor pulvinar etiam magna etiam.`
- `Sagittis adipiscing lorem eleifend.`
- `Felis enim feugiat dolore viverra.`

- add an ordered list with these items:


`Dolor pulvinar etiam magna etiam.`
`Sagittis adipiscing lorem eleifend.`
`Felis enim feugiat dolore viverra.`
- `Dolor pulvinar etiam magna etiam.`
- `Sagittis adipiscing lorem eleifend.`
- `Felis enim feugiat dolore viverra.`

- after previous ordered list, in the same `div`

add a heading level 3 with text `Definition`
add a definition list with these items:


Term: `Definition List title`, Definition: `Definition text.`
Term: `Startup`, Definition: `A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.`
Term: `Water`, Definition: `A colorless, transparent, odorless liquid that forms the seas, lakes, rivers, and rain and is the basis of the fluids of living organisms.`
- add a heading level 3 with text `Definition`
- add a definition list with these items:


Term: `Definition List title`, Definition: `Definition text.`
Term: `Startup`, Definition: `A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.`
Term: `Water`, Definition: `A colorless, transparent, odorless liquid that forms the seas, lakes, rivers, and rain and is the basis of the fluids of living organisms.`
- Term: `Definition List title`, Definition: `Definition text.`
- Term: `Startup`, Definition: `A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.`
- Term: `Water`, Definition: `A colorless, transparent, odorless liquid that forms the seas, lakes, rivers, and rain and is the basis of the fluids of living organisms.`

- add a heading level 3 with text `Definition`
- add a definition list with these items:


Term: `Definition List title`, Definition: `Definition text.`
Term: `Startup`, Definition: `A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.`
Term: `Water`, Definition: `A colorless, transparent, odorless liquid that forms the seas, lakes, rivers, and rain and is the basis of the fluids of living organisms.`
- Term: `Definition List title`, Definition: `Definition text.`
- Term: `Startup`, Definition: `A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.`
- Term: `Water`, Definition: `A colorless, transparent, odorless liquid that forms the seas, lakes, rivers, and rain and is the basis of the fluids of living organisms.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `26-styleguide.html`


---
### 27. Separate content

Copy the content of 25-index.html into 27-index.html

W3C does not need to pass.

- in the `footer` between the two `div`s:


add a horizontal rule
after the horizontal rule add a paragraph with text `© 2020 Techium, made with <heart> by students at Holberton School.`
- add a horizontal rule
- after the horizontal rule add a paragraph with text `© 2020 Techium, made with <heart> by students at Holberton School.`

- add a horizontal rule
- after the horizontal rule add a paragraph with text `© 2020 Techium, made with <heart> by students at Holberton School.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `27-index.html`


---
### 28. Horizontal rule example

Copy the content of 26-styleguide.html into 28-styleguide.html

- in `main` after Lists `section`

add a new line and a comment with the text `Horizontal rule`
create a new `section`

create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
after the `header` create a `div` and put a horizontal rule in it
- add a new line and a comment with the text `Horizontal rule`
- create a new `section`

create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
after the `header` create a `div` and put a horizontal rule in it
- create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
- after the `header` create a `div` and put a horizontal rule in it

- add a new line and a comment with the text `Horizontal rule`
- create a new `section`

create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
after the `header` create a `div` and put a horizontal rule in it
- create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
- after the `header` create a `div` and put a horizontal rule in it

- create a `header` and inside it add a level 2 heading with the text `Horizontal rule`
- after the `header` create a `div` and put a horizontal rule in it

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `28-styleguide.html`


---
### 29. Client quotes

Copy the content of 27-index.html into 29-index.html

W3C does not need to pass

- in the Testimonials `section`

in the first `article`

replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`

in the second `article`

replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`

in the third `article`

replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`
- in the first `article`

replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`
- replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`
- in the second `article`

replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`
- replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`
- in the third `article`

replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`
- replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`

- in the first `article`

replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`
- replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`
- in the second `article`

replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`
- replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`
- in the third `article`

replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`
- replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`

- replace the text with a blockquote with text `I am completely blown away. Thanks to Techium, we've just launched our 5th website!` and cite author `Yuri Y.`

- replace the text with a blockquote with text `Thank you so much for your help. Techium company is awesome!` and cite author `Dorrie S.`

- replace the text with a blockquote with text `I love your system. Definitely worth the investment. I'd be lost without Techium company.` and cite author `Sven H.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `29-index.html`


---
### 30. Examples of quotes

Copy the content of 28-styleguide.html into 30-styleguide.html

Example of inline quote:

Example of blockquote:

- inside `main` after Horizontal rule `section`

add a new line and a comment with text `Blockquotes`
create a new `section`

in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- add a new line and a comment with text `Blockquotes`
- create a new `section`

in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
- after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- in the `div` add a level 3 heading with the text `Inline quote`
- add an inline quote with the text `Stay hungry. Stay foolish.`

- add a new line and a comment with text `Blockquotes`
- create a new `section`

in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
- after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- in the `div` add a level 3 heading with the text `Inline quote`
- add an inline quote with the text `Stay hungry. Stay foolish.`

- in the `section` create a `header`, in the `header` create a level 2 heading with text `Blockquotes`
- after the `header`, create a `div`

in the `div` add a level 3 heading with the text `Inline quote`
add an inline quote with the text `Stay hungry. Stay foolish.`
- in the `div` add a level 3 heading with the text `Inline quote`
- add an inline quote with the text `Stay hungry. Stay foolish.`

- in the `div` add a level 3 heading with the text `Inline quote`
- add an inline quote with the text `Stay hungry. Stay foolish.`

- after the inline quote `div`, create another `div`

in the new `div` add a level 3 heading with the text `Blockquote`
add a multiline quote with the text `I will be the leader of a company that ends up being worth billions of dollars, because I got the answers. I understand culture. I am the nucleus. I think that’s a responsibility that I have, to push possibilities, to show people, this is the level that things could be at.` and cite `Kanye West, Musician`
- in the new `div` add a level 3 heading with the text `Blockquote`
- add a multiline quote with the text `I will be the leader of a company that ends up being worth billions of dollars, because I got the answers. I understand culture. I am the nucleus. I think that’s a responsibility that I have, to push possibilities, to show people, this is the level that things could be at.` and cite `Kanye West, Musician`

- in the new `div` add a level 3 heading with the text `Blockquote`
- add a multiline quote with the text `I will be the leader of a company that ends up being worth billions of dollars, because I got the answers. I understand culture. I am the nucleus. I think that’s a responsibility that I have, to push possibilities, to show people, this is the level that things could be at.` and cite `Kanye West, Musician`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `30-styleguide.html`


---
### 31. Address and latest news authors

Copy the content of 29-index.html into 31-index.html

W3C does not need to pass

- in the `footer`

right after open `footer` tag, put the following address: `234 Washington Street` (line-break) `Urbana, Illinois`
- right after open `footer` tag, put the following address: `234 Washington Street` (line-break) `Urbana, Illinois`
- in the Latest news `section`

in the first `article`, after the last paragraph, add the author name in small print: `By Kelly D.`
in the second `article`, after the last paragraph, add the author name in small print: `By William A.`
in the third `article`, after the last paragraph, add the author name in small print: `By Frances J.`
- in the first `article`, after the last paragraph, add the author name in small print: `By Kelly D.`
- in the second `article`, after the last paragraph, add the author name in small print: `By William A.`
- in the third `article`, after the last paragraph, add the author name in small print: `By Frances J.`

- right after open `footer` tag, put the following address: `234 Washington Street` (line-break) `Urbana, Illinois`

- in the first `article`, after the last paragraph, add the author name in small print: `By Kelly D.`
- in the second `article`, after the last paragraph, add the author name in small print: `By William A.`
- in the third `article`, after the last paragraph, add the author name in small print: `By Frances J.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `31-index.html`


---
### 32. Typography section - using the correct tags

Copy the content of 30-styleguide.html into 32-styleguide.html

inside main after the Blockquotes section

create a new section

W3C does not need to pass

- inside `main` after the Blockquotes `section`

add a new line and a comment with text `Typography`
create a new `section`

in the section create a `header` and inside it add a level 2 heading with the text `Typography`
after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
create another `div`, in the new `div` nest this code block using the `pre` HTML tag:

 &lt;code&gt;
     &lt;h2&gt;My title&lt;/h2&gt;
     &lt;p&gt;Proin lacus turpis, feugiat sit amet sollicitudin non, volutpat in libero. Aenean hendrerit ultrices nulla ac lobortis. Vestibulum consectetur nibh vel ante rhoncus faucibus.&lt;/p&gt;
 &lt;/code&gt;


create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.
- add a new line and a comment with text `Typography`
- create a new `section`

in the section create a `header` and inside it add a level 2 heading with the text `Typography`
after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
create another `div`, in the new `div` nest this code block using the `pre` HTML tag:

 &lt;code&gt;
     &lt;h2&gt;My title&lt;/h2&gt;
     &lt;p&gt;Proin lacus turpis, feugiat sit amet sollicitudin non, volutpat in libero. Aenean hendrerit ultrices nulla ac lobortis. Vestibulum consectetur nibh vel ante rhoncus faucibus.&lt;/p&gt;
 &lt;/code&gt;


create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.
- in the section create a `header` and inside it add a level 2 heading with the text `Typography`
- after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
- create another `div`, in the new `div` nest this code block using the `pre` HTML tag:
- create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.

- add a new line and a comment with text `Typography`
- create a new `section`

in the section create a `header` and inside it add a level 2 heading with the text `Typography`
after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
create another `div`, in the new `div` nest this code block using the `pre` HTML tag:

 &lt;code&gt;
     &lt;h2&gt;My title&lt;/h2&gt;
     &lt;p&gt;Proin lacus turpis, feugiat sit amet sollicitudin non, volutpat in libero. Aenean hendrerit ultrices nulla ac lobortis. Vestibulum consectetur nibh vel ante rhoncus faucibus.&lt;/p&gt;
 &lt;/code&gt;


create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.
- in the section create a `header` and inside it add a level 2 heading with the text `Typography`
- after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
- create another `div`, in the new `div` nest this code block using the `pre` HTML tag:
- create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.

- in the section create a `header` and inside it add a level 2 heading with the text `Typography`
- after the `header` create a `div`, inside the `div` add this text with the correct HTML tag: `320 Stewart Avenue, Unit 12 (line break) New York City NY 10001`, the city, state, and postal code should be on a separate line
- create another `div`, in the new `div` nest this code block using the `pre` HTML tag:

- create another `div`, in the new  `div` add this paragraph of text with the correct HTML tag: `Curabitur sit amet turpis cursus massa mollis highlighted. Duis finibus leo massa, eget dapibus erat finibus sed. Aenean condimentum sapien magna, eleifend highlighted mi consequat ut. Cras nec quam sed sapien ultricies highlighted ut sed metus.` Each occurrence of the word `highlighted` should be highlighted.

```
 <code>
     <h2>My title</h2>
     <p>Proin lacus turpis, feugiat sit amet sollicitudin non, volutpat in libero. Aenean hendrerit ultrices nulla ac lobortis. Vestibulum consectetur nibh vel ante rhoncus faucibus.</p>
 </code>

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `32-styleguide.html`


---
### 33. Table

![3](2138_3.jpg)

Copy the content of 32-styleguide.html into 33-styleguide.html



The <th> tags containing Title, Director, Release Date should have a scope attribute set to col
The <th> tags containing the names of the movies should have a scope attribute set to row

Due to previous task, does not have to pass W3C

- inside `main` after Typography `section`

add a new line and a comment with text `Table`
create a new `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
after the `header`, create a `table`, reproduce in HTML the visual below
- add a new line and a comment with text `Table`
- create a new `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
after the `header`, create a `table`, reproduce in HTML the visual below
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
- after the `header`, create a `table`, reproduce in HTML the visual below

- add a new line and a comment with text `Table`
- create a new `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
after the `header`, create a `table`, reproduce in HTML the visual below
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
- after the `header`, create a `table`, reproduce in HTML the visual below

- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Table`
- after the `header`, create a `table`, reproduce in HTML the visual below

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `33-styleguide.html`


---
### 34. Details

Copy the content of 33-styleguide.html into 34-styleguide.html

Due to earlier task, does not have to pass W3C

- in `main` tag after Table `section`

add a new line and a comment with text `Details`
create a new `section`

create a `header`, in the `header` add a level 2 heading with the text `Details`
after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- add a new line and a comment with text `Details`
- create a new `section`

create a `header`, in the `header` add a level 2 heading with the text `Details`
after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- create a `header`, in the `header` add a level 2 heading with the text `Details`
- after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- in the `div` add a level 3 heading with text `Default`
- add a details element and specify `Show/Hide me` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- add a level 3 heading with text `Open`
- add a details element that is open by default and specify `Always open` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

- add a new line and a comment with text `Details`
- create a new `section`

create a `header`, in the `header` add a level 2 heading with the text `Details`
after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- create a `header`, in the `header` add a level 2 heading with the text `Details`
- after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- in the `div` add a level 3 heading with text `Default`
- add a details element and specify `Show/Hide me` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- add a level 3 heading with text `Open`
- add a details element that is open by default and specify `Always open` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

- create a `header`, in the `header` add a level 2 heading with the text `Details`
- after the `header` create a `div`

in the `div` add a level 3 heading with text `Default`
add a details element and specify `Show/Hide me` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- in the `div` add a level 3 heading with text `Default`
- add a details element and specify `Show/Hide me` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- create another `div`

add a level 3 heading with text `Open`
add a details element that is open by default and specify `Always open` in the `summary`
add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`
- add a level 3 heading with text `Open`
- add a details element that is open by default and specify `Always open` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

- in the `div` add a level 3 heading with text `Default`
- add a details element and specify `Show/Hide me` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

- add a level 3 heading with text `Open`
- add a details element that is open by default and specify `Always open` in the `summary`
- add this text after the `summary`: `Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `34-styleguide.html`


---
### 35. Replace text logo with image logo

![3](2138_3.png)



Copy the content of 31-index.html into 35-index.html

W3C does not need to pass

- in `header`

find the `span` with the name of the website
replace it with the image above
make sure the image is in the same directory as all of your other files and that the file name is `logo-black.png`
alt: `Techium logo`
don’t forget to specify width of `160` and height of `40`
- find the `span` with the name of the website
- replace it with the image above
- make sure the image is in the same directory as all of your other files and that the file name is `logo-black.png`
- alt: `Techium logo`
- don’t forget to specify width of `160` and height of `40`
- in `footer`, after the opening tag and before the address


insert the logo image
alt: `Techium logo`
don’t forget to specify the width and height (same as in header)
- insert the logo image
- alt: `Techium logo`
- don’t forget to specify the width and height (same as in header)

- find the `span` with the name of the website
- replace it with the image above
- make sure the image is in the same directory as all of your other files and that the file name is `logo-black.png`
- alt: `Techium logo`
- don’t forget to specify width of `160` and height of `40`

- insert the logo image
- alt: `Techium logo`
- don’t forget to specify the width and height (same as in header)

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `35-index.html`


---
### 36. Add images to your sections

Copy the content of 35-index.html into 36-index.html

You can use image generators to get images for this task. For avatar images you can download them on UI Faces. Just make sure you rename your images to match the task requirements.

Add three images in the Works section:

Add one image in the About Us section:

Add three images in the Latest news section:

Add three images in the Testimonials section:

Does not need to pass W3C

- in the Works `section`

before the first level 3 heading create a `div`

add `images/pic-work-01.jpg` inside the `div`
alt: empty

before the second level 3 heading create a `div`

add `images/pic-work-02.jpg` inside the `div`
alt: empty

before the third level 3 heading create a `div`

add `images/pic-work-03.jpg` inside the `div`
alt: empty
- before the first level 3 heading create a `div`

add `images/pic-work-01.jpg` inside the `div`
alt: empty
- add `images/pic-work-01.jpg` inside the `div`
- alt: empty
- before the second level 3 heading create a `div`

add `images/pic-work-02.jpg` inside the `div`
alt: empty
- add `images/pic-work-02.jpg` inside the `div`
- alt: empty
- before the third level 3 heading create a `div`

add `images/pic-work-03.jpg` inside the `div`
alt: empty
- add `images/pic-work-03.jpg` inside the `div`
- alt: empty

- before the first level 3 heading create a `div`

add `images/pic-work-01.jpg` inside the `div`
alt: empty
- add `images/pic-work-01.jpg` inside the `div`
- alt: empty
- before the second level 3 heading create a `div`

add `images/pic-work-02.jpg` inside the `div`
alt: empty
- add `images/pic-work-02.jpg` inside the `div`
- alt: empty
- before the third level 3 heading create a `div`

add `images/pic-work-03.jpg` inside the `div`
alt: empty
- add `images/pic-work-03.jpg` inside the `div`
- alt: empty

- add `images/pic-work-01.jpg` inside the `div`
- alt: empty

- add `images/pic-work-02.jpg` inside the `div`
- alt: empty

- add `images/pic-work-03.jpg` inside the `div`
- alt: empty

- in the About Us `section` before the first level 3 heading inside the `div`

add the image `images/pic-about-us.jpg`

alt: empty
width: `460`
height: `447`
- add the image `images/pic-about-us.jpg`

alt: empty
width: `460`
height: `447`
- alt: empty
- width: `460`
- height: `447`

- add the image `images/pic-about-us.jpg`

alt: empty
width: `460`
height: `447`
- alt: empty
- width: `460`
- height: `447`

- alt: empty
- width: `460`
- height: `447`

- in the Latest news `section`

in the first `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-01.jpg`
alt: empty
width: `305`
height: `205`

in the second `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-02.jpg`
alt: empty
width: `305`
height: `205`

in the third `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-03.jpg`
alt: empty
width: `305`
height: `205`
- in the first `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-01.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-01.jpg`
- alt: empty
- width: `305`
- height: `205`
- in the second `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-02.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-02.jpg`
- alt: empty
- width: `305`
- height: `205`
- in the third `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-03.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-03.jpg`
- alt: empty
- width: `305`
- height: `205`

- in the first `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-01.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-01.jpg`
- alt: empty
- width: `305`
- height: `205`
- in the second `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-02.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-02.jpg`
- alt: empty
- width: `305`
- height: `205`
- in the third `article`, before the first paragraph, create a `div`

in the `div` add the image `images/pic-blog-03.jpg`
alt: empty
width: `305`
height: `205`
- in the `div` add the image `images/pic-blog-03.jpg`
- alt: empty
- width: `305`
- height: `205`

- in the `div` add the image `images/pic-blog-01.jpg`
- alt: empty
- width: `305`
- height: `205`

- in the `div` add the image `images/pic-blog-02.jpg`
- alt: empty
- width: `305`
- height: `205`

- in the `div` add the image `images/pic-blog-03.jpg`
- alt: empty
- width: `305`
- height: `205`

- in the Testimonials `section`

in the first `article` before the quote, add the image `images/pic-person-01.jpg`

alt: `Yuri Y. avatar`
width: `100px`
height: `100px`

in the second `article` before the quote, add the image `images/pic-person-02.jpg`

alt: `Dorrie S. avatar`
width: `100px`
height: `100px`

in the third `article` before the quote, add the image `images/pic-person-03.jpg`

alt: `Sven H. avatar`
width: `100px`
height: `100px`
- in the first `article` before the quote, add the image `images/pic-person-01.jpg`

alt: `Yuri Y. avatar`
width: `100px`
height: `100px`
- alt: `Yuri Y. avatar`
- width: `100px`
- height: `100px`
- in the second `article` before the quote, add the image `images/pic-person-02.jpg`

alt: `Dorrie S. avatar`
width: `100px`
height: `100px`
- alt: `Dorrie S. avatar`
- width: `100px`
- height: `100px`
- in the third `article` before the quote, add the image `images/pic-person-03.jpg`

alt: `Sven H. avatar`
width: `100px`
height: `100px`
- alt: `Sven H. avatar`
- width: `100px`
- height: `100px`

- in the first `article` before the quote, add the image `images/pic-person-01.jpg`

alt: `Yuri Y. avatar`
width: `100px`
height: `100px`
- alt: `Yuri Y. avatar`
- width: `100px`
- height: `100px`
- in the second `article` before the quote, add the image `images/pic-person-02.jpg`

alt: `Dorrie S. avatar`
width: `100px`
height: `100px`
- alt: `Dorrie S. avatar`
- width: `100px`
- height: `100px`
- in the third `article` before the quote, add the image `images/pic-person-03.jpg`

alt: `Sven H. avatar`
width: `100px`
height: `100px`
- alt: `Sven H. avatar`
- width: `100px`
- height: `100px`

- alt: `Yuri Y. avatar`
- width: `100px`
- height: `100px`

- alt: `Dorrie S. avatar`
- width: `100px`
- height: `100px`

- alt: `Sven H. avatar`
- width: `100px`
- height: `100px`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `36-index.html`


---
### 37. Social icons

Copy the content of 36-index.html into index.html (the final file!)

inside the footer

W3C does not need to pass

- inside the `footer`

replace the text `Facebook` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

&lt;svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"&gt;
&lt;title&gt;
Facebook icon
&lt;/title&gt;
&lt;path d="M23.998 12c0-6.628-5.372-12-11.999-12C5.372 0 0 5.372 0 12c0 5.988 4.388 10.952 10.124 11.852v-8.384H7.078v-3.469h3.046V9.356c0-3.008 1.792-4.669 4.532-4.669 1.313 0 2.686.234 2.686.234v2.953H15.83c-1.49 0-1.955.925-1.955 1.874V12h3.328l-.532 3.469h-2.796v8.384c5.736-.9 10.124-5.864 10.124-11.853z"/&gt;
&lt;/svg&gt;


replace the text `Twitter` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

&lt;svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"&gt;
&lt;title&gt;
Twitter icon
&lt;/title&gt;
&lt;path d="M23.954 4.569a10 10 0 0 1-2.825.775 4.958 4.958 0 0 0 2.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 0 0-8.384 4.482C7.691 8.094 4.066 6.13 1.64 3.161a4.822 4.822 0 0 0-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 0 1-2.228-.616v.061a4.923 4.923 0 0 0 3.946 4.827 4.996 4.996 0 0 1-2.212.085 4.937 4.937 0 0 0 4.604 3.417 9.868 9.868 0 0 1-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 0 0 7.557 2.209c9.054 0 13.999-7.496 13.999-13.986 0-.209 0-.42-.015-.63a9.936 9.936 0 0 0 2.46-2.548l-.047-.02z"/&gt;
&lt;/svg&gt;


replace the text `Instagram` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

&lt;svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"&gt;
&lt;title&gt;
Instagram icon
&lt;/title&gt;
&lt;path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913a5.885 5.885 0 0 0 1.384 2.126A5.868 5.868 0 0 0 4.14 23.37c.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558a5.898 5.898 0 0 0 2.126-1.384 5.86 5.86 0 0 0 1.384-2.126c.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913a5.89 5.89 0 0 0-1.384-2.126A5.847 5.847 0 0 0 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227a3.81 3.81 0 0 1-.899 1.382 3.744 3.744 0 0 1-1.38.896c-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421a3.716 3.716 0 0 1-1.379-.899 3.644 3.644 0 0 1-.9-1.38c-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 1 0 0-12.324zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405a1.441 1.441 0 0 1-2.88 0 1.44 1.44 0 0 1 2.88 0z"/&gt;
&lt;/svg&gt;
- replace the text `Facebook` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:
- replace the text `Twitter` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:
- replace the text `Instagram` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

- replace the text `Facebook` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

- replace the text `Twitter` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

- replace the text `Instagram` with the SVG icon code and add width of `25px` and height of `25px` to the SVG tag:

```
<svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
<title>
Facebook icon
</title>
<path d="M23.998 12c0-6.628-5.372-12-11.999-12C5.372 0 0 5.372 0 12c0 5.988 4.388 10.952 10.124 11.852v-8.384H7.078v-3.469h3.046V9.356c0-3.008 1.792-4.669 4.532-4.669 1.313 0 2.686.234 2.686.234v2.953H15.83c-1.49 0-1.955.925-1.955 1.874V12h3.328l-.532 3.469h-2.796v8.384c5.736-.9 10.124-5.864 10.124-11.853z"/>
</svg>

```

```
<svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
<title>
Twitter icon
</title>
<path d="M23.954 4.569a10 10 0 0 1-2.825.775 4.958 4.958 0 0 0 2.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 0 0-8.384 4.482C7.691 8.094 4.066 6.13 1.64 3.161a4.822 4.822 0 0 0-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 0 1-2.228-.616v.061a4.923 4.923 0 0 0 3.946 4.827 4.996 4.996 0 0 1-2.212.085 4.937 4.937 0 0 0 4.604 3.417 9.868 9.868 0 0 1-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 0 0 7.557 2.209c9.054 0 13.999-7.496 13.999-13.986 0-.209 0-.42-.015-.63a9.936 9.936 0 0 0 2.46-2.548l-.047-.02z"/>
</svg>

```

```
<svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
<title>
Instagram icon
</title>
<path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913a5.885 5.885 0 0 0 1.384 2.126A5.868 5.868 0 0 0 4.14 23.37c.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558a5.898 5.898 0 0 0 2.126-1.384 5.86 5.86 0 0 0 1.384-2.126c.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913a5.89 5.89 0 0 0-1.384-2.126A5.847 5.847 0 0 0 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227a3.81 3.81 0 0 1-.899 1.382 3.744 3.744 0 0 1-1.38.896c-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421a3.716 3.716 0 0 1-1.379-.899 3.644 3.644 0 0 1-.9-1.38c-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 1 0 0-12.324zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405a1.441 1.441 0 0 1-2.88 0 1.44 1.44 0 0 1 2.88 0z"/>
</svg>

```

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `index.html`


---
### 38. Add a video player in the styleguide

Copy the content of 34-styleguide.html into 38-styleguide.html

Due to an earlier task, does not need to pass W3C

- in `main` after the Details `section`

add a new line and a comment with text `Video`
create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
add controls to the video
ensure that the video does a loop
display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
provide an alternative text: `Sorry, your browser doesn't support HTML5 video`
- add a new line and a comment with text `Video`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
add controls to the video
ensure that the video does a loop
display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
provide an alternative text: `Sorry, your browser doesn't support HTML5 video`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
- after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
- add controls to the video
- ensure that the video does a loop
- display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
- provide an alternative text: `Sorry, your browser doesn't support HTML5 video`

- add a new line and a comment with text `Video`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
add controls to the video
ensure that the video does a loop
display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
provide an alternative text: `Sorry, your browser doesn't support HTML5 video`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
- after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
- add controls to the video
- ensure that the video does a loop
- display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
- provide an alternative text: `Sorry, your browser doesn't support HTML5 video`

- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Video`
- after the `header` add the following video: `https://intranet-projects-files.s3.amazonaws.com/webstack/BigBuckBunny.mp4`
- add controls to the video
- ensure that the video does a loop
- display `https://intranet-projects-files.s3.amazonaws.com/webstack/thumbnail.jpg` when the video is downloading
- provide an alternative text: `Sorry, your browser doesn't support HTML5 video`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `38-styleguide.html`


---
### 39. Add an audio player in the styleguide

Copy the content of 38-styleguide.html into 39-styleguide.html

Due to an earlier task, does not need to pass W3C

- in `main` after Video `section`

add a new line and a comment with text `Audio`
create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
add controls to the audio player
provide an alternative text: `Sorry, your browser doesn't support audio element`
- add a new line and a comment with text `Audio`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
add controls to the audio player
provide an alternative text: `Sorry, your browser doesn't support audio element`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
- after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
- add controls to the audio player
- provide an alternative text: `Sorry, your browser doesn't support audio element`

- add a new line and a comment with text `Audio`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
add controls to the audio player
provide an alternative text: `Sorry, your browser doesn't support audio element`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
- after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
- add controls to the audio player
- provide an alternative text: `Sorry, your browser doesn't support audio element`

- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Audio`
- after the `header` add the following audio file: `https://intranet-projects-files.s3.amazonaws.com/webstack/TroubleChapter8_64kb.mp3`
- add controls to the audio player
- provide an alternative text: `Sorry, your browser doesn't support audio element`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `39-styleguide.html`


---
### 40. Add a iframe example in the styleguide

Copy the content of 39-styleguide.html into styleguide.html

W3C does not need to pass

And you are done!

- in `main` after the Audio `section`

add a new line and a comment with text `Iframe`
create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- add a new line and a comment with text `Iframe`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
- after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- title: `Holberton School`
- width: `350px`
- height: `200px`
- source: `https://www.youtube.com/embed/41N6bKO-NVI`
- fallback text: `Holberton Sally`

- add a new line and a comment with text `Iframe`
- create a `section`

in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
- after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- title: `Holberton School`
- width: `350px`
- height: `200px`
- source: `https://www.youtube.com/embed/41N6bKO-NVI`
- fallback text: `Holberton Sally`

- in the `section` create a `header`, in the `header` add a level 2 heading with the text `Iframe`
- after the `header` add a `div`

inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- title: `Holberton School`
- width: `350px`
- height: `200px`
- source: `https://www.youtube.com/embed/41N6bKO-NVI`
- fallback text: `Holberton Sally`

- inside the `div`, create an `iframe`

title: `Holberton School`
width: `350px`
height: `200px`
source: `https://www.youtube.com/embed/41N6bKO-NVI`
fallback text: `Holberton Sally`
- title: `Holberton School`
- width: `350px`
- height: `200px`
- source: `https://www.youtube.com/embed/41N6bKO-NVI`
- fallback text: `Holberton Sally`

- title: `Holberton School`
- width: `350px`
- height: `200px`
- source: `https://www.youtube.com/embed/41N6bKO-NVI`
- fallback text: `Holberton Sally`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `html_advanced`
- File: `styleguide.html`