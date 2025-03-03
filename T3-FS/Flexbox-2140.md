# Project 2140: Flexbox
----



![1](2140_1.jpg)

## Resources

**Read or watch**:

* [A Complete Guide to Flexbox | CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* [Flexbox Froggy - A game for learning CSS flexbox](http://flexboxfroggy.com/)
* [Flexbox Defense](http://www.flexboxdefense.com/)
* [Flexbox Cheatsheet](https://yoksel.github.io/flex-cheatsheet/)
* [CSS Flexible Box Layout - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
* [afonsopacifer/awesome-flexbox: A curated list of CSS Flexible Box Layout Module or only Flexbox.](https://github.com/afonsopacifer/awesome-flexbox)
* [Build with Flexbox](https://flexbox.buildwithreact.com/)
* [Flexplorer](https://bennettfeely.com/flexplorer/)
* [CSS Flexible Box Layout Module Level 1](https://www.w3.org/TR/css-flexbox-1/#flex)
* [FLEX: A simple visual cheatsheet for flexbox](https://flexbox.malven.co/)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* What is Flexbox?
* How to convert float positioning to a flex display
* How to horizontally and vertically align elements using Flexbox
* The difference between the main and cross axes
* Properties that work on flex elements vs flex container
* Shorthands for flex
* How to create a new page with flex in mind
## Requirements

* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project is mandatory
* You are**not allowed**to install, import or use external libraries. This website must be build with only HTML/CSS. No NodeJS, React, VueJS, Bootstrap, etc.
## Files

### Required images for your HTML files

Download the images linked in the[CSS Advanced](https://intranet.hbtn.io/projects/2144)and place them into an images directory at the root of the project.

If that link doesn’t work, use[this one](https://intranet-projects-files.s3.amazonaws.com/holbertonschool-webstack/601/images.zip)

### `HTML starter file`

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
    <title>Homepage - Techium</title>
    <meta name="description" content="Description of the page less than 150 characters">
    <link rel="icon" type="image/png" href="images/favicon.jpg">
    <link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700|Raleway:700&display=swap" rel="stylesheet">
    <link rel='stylesheet' href='styles.css'>
  </head>
  <body>
    <!– Header –>
    <header class="header" data-section-theme="dark">
      <div class="container">
        <div class="header-logo">
          <a href="#">
            <img src="images/logo-white.png" alt="Techium logo" width="160" height="40">
          </a>
        </div>
        <nav class="navbar-menu">
          <ul class="nav">
            <li class="nav-item">
              <a href="#" class="nav-link">Home</a>
            </li>
            <li class="nav-item">
              <a href="#services" class="nav-link">Services</a>
            </li>
            <li class="nav-item">
              <a href="#works" class="nav-link">Works</a>
            </li>
            <li class="nav-item">
              <a href="#about" class="nav-link">About</a>
            </li>
            <li class="nav-item">
              <a href="#latest_news" class="nav-link">Latest news</a>
            </li>
            <li class="nav-item">
              <a href="#testimonials" class="nav-link">Testimonials</a>
            </li>
            <li class="nav-item">
              <a href="#contact" class="nav-link">Contact</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <!– Main –>
    <main>
      <!– Hero section –>
      <section class="section-hero" data-section-theme="dark">
        <div class="container">
          <div class="section-body">
            <section class="section-inner">
              <h2 class="section-title">We help you build your brand</h2>
              <a href="#" class="button">Get Started</a>
            </section>
          </div>
        </div>
      </section>
      <!– Services section –>
      <section id="services" class="section">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">Services</h2>
            <p class="section-tagline">We work with you</p>
          </header>
          <div class="section-body">
            <ul class="row">
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">Design & Concept</a></h3>
                </div>
              </li>
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">Digital Strategy</a></h3>
                </div>
              </li>
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">Content Strategy</a></h3>
                </div>
              </li>
            </ul>
            <ul class="row">
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">UX Design</a></h3>
                </div>
              </li>
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">Web Development</a></h3>
                </div>
              </li>
              <li class="col-1-3">
                <div class="card-services">
                  <h3 class="card-title"><a href="#">Social Media</a></h3>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <!– Works section –>
      <section id="works" class="section" data-section-theme="dark">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">Works</h2>
            <p class="section-tagline">Take a look at our portfolio</p>
          </header>
          <div class="section-body">
            <ul class="row">
              <li class="col-1-3">
                <article class="card-work">
                  <div class="card-outer">
                    <div class="card-image">
                      <img src="images/pic-work-01.jpg" alt="">
                    </div>
                    <div class="card-inner">
                      <h3 class="card-title"><a href="#">Interior Design</a></h3>
                    </div>
                  </div>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-work">
                  <div class="card-outer">
                    <div class="card-image">
                      <img src="images/pic-work-02.jpg" alt="">
                    </div>
                    <div class="card-inner">
                      <h3 class="card-title"><a href="#">Web Development</a></h3>
                    </div>
                  </div>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-work">
                  <div class="card-outer">
                    <div class="card-image">
                      <img src="images/pic-work-03.jpg" alt="">
                    </div>
                    <div class="card-inner">
                      <h3 class="card-title"><a href="#">Personal Development</a></h3>
                    </div>
                  </div>
                </article>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <!– About Us section –>
      <section id="about" class="section">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">About Us</h2>
            <p class="section-tagline">Everything about us</p>
          </header>
          <div class="section-body">
            <div class="row">
              <div class="col-1-2">
                <img src="images/pic-about-01.jpg" alt="" width="460" height="460">
              </div>
              <div class="col-1-2">
                <h3>Who are we</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!</p>
                <h3>Our culture</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!</p>
                <h3>How we work</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum, omnis expedita! Eum, praesentium cumque accusantium rem, sit quaerat est nisi ratione, deserunt ducimus quidem iste dicta quibusdam atque maxime cum!</p>
              </div>
            </div>
          </div>
          <div class="section-footer">
            <a href="#" class="button">Learn more about us</a>
          </div>
        </div>
      </section>
      <!– Latest news section –>
      <section id="latest_news" class="section">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">Latest News</h2>
          </header>
          <div class="section-body">
            <ul class="row">
              <li class="col-1-3">
                <article class="card-blog">
                  <div>
                    <img src="images/pic-article-01.jpg" alt="" width="305" height="305">
                  </div>
                  <p class="card-category">Career</p>
                  <h3><a href="#">Hoc loco tenere se Triarius non potuit.</a></h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?</p>
                  <small>By Kelly D.</small>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-blog">
                  <div>
                    <img src="images/pic-article-02.jpg" alt="" width="305" height="305">
                  </div>
                  <p class="card-category">Digital Life</p>
                  <h3><a href="#">Ut alios omittam, hunc appello, quem ille unum secutus est.</a></h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?</p>
                  <small>By William A.</small>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-blog">
                  <div>
                    <img src="images/pic-article-03.jpg" alt="" width="305" height="305">
                  </div>
                  <p class="card-category">Social</p>
                  <h3><a href="#">Bestiarum vero nullum iudicium puto.</a></h3>
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Non igitur bene. Quid enim est a Chrysippo praetermissum in Stoicis? Pugnant Stoici cum Peripateticis. Prioris generis est docilitas, memoria; Apparet statim, quae sint officia, quae actiones.</p>
                  <small>By Frances J.</small>
                </article>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <!– Testimonials section –>
      <section id="testimonial" class="section">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">Testimonials</h2>
            <p class="section-tagline">We are more than a digital company</p>
          </header>
          <div class="section-body">
            <ul class="row">
              <li class="col-1-3">
                <article class="card-testimonial">
                  <img src="images/pic-person-01.jpg" alt="Yuri Y. avatar" width="100" height="100" class="card-avatar">
                  <blockquote class="card-quote">
                    <p>I am completely blown away. Thanks to Techium, we’ve just launched our 5th website!
                      <cite>Yuri Y.</cite>
                    </p>
                  </blockquote>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-testimonial">
                  <img src="images/pic-person-02.jpg" alt="Dorrie S. avatar" width="100" height="100" class="card-avatar">
                  <blockquote class="card-quote">
                    <p>Thank you so much for your help. Techium company is awesome!
                      <cite>Dorrie S.</cite>
                    </p>
                  </blockquote>
                </article>
              </li>
              <li class="col-1-3">
                <article class="card-testimonial">
                  <img src="images/pic-person-03.jpg" alt="Sven H. avatar" width="100" height="100" class="card-avatar">
                  <blockquote class="card-quote">
                    <p>I love your system. Definitely worth the investment. I’d be lost without Techium company.
                      <cite>Sven H.</cite>
                    </p>
                  </blockquote>
                </article>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <!– Contact section –>
      <section id="contact" class="section">
        <div class="container">
          <header class="section-header">
            <h2 class="section-title">Contact</h2>
            <p class="section-tagline">We’d love to hear from you!</p>
          </header>
          <div class="section-body">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id Sextilius factum negabat. Quo tandem modo? At eum nihili facit; Quae contraria sunt his, malane?</p>
          </div>
          <div class="section-footer">
            <a href="#" class="button">Get in touch</a>
          </div>
        </div>
      </section>
    </main>
    <!– Footer –>
    <footer class="footer" data-section-theme="dark">
      <div  class="container">
        <div class="row">
          <div class="col-1-2">
            <img src="images/logo-white.png" alt="Techium logo" width="160" height="40">
            <address class="footer-address">
              972 Mission St<br>
              San Francisco, CA<br>
              94103
            </address>
          </div>
          <div class="col-1-2">
            <ul class="social nav">
              <li class="social-item nav-item">
                <a href="https://www.facebook.com/HolbertonSchool/" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Facebook icon
                    </title>
                    <path d="M23.998 12c0-6.628-5.372-12-11.999-12C5.372 0 0 5.372 0 12c0 5.988 4.388 10.952 10.124 11.852v-8.384H7.078v-3.469h3.046V9.356c0-3.008 1.792-4.669 4.532-4.669 1.313 0 2.686.234 2.686.234v2.953H15.83c-1.49 0-1.955.925-1.955 1.874V12h3.328l-.532 3.469h-2.796v8.384c5.736-.9 10.124-5.864 10.124-11.853z"/>
                  </svg>
                </a>
              </li>
              <li class="social-item nav-item">
                <a href="https://twitter.com/holbertonschool" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Twitter icon
                    </title>
                    <path d="M23.954 4.569a10 10 0 0 1-2.825.775 4.958 4.958 0 0 0 2.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 0 0-8.384 4.482C7.691 8.094 4.066 6.13 1.64 3.161a4.822 4.822 0 0 0-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 0 1-2.228-.616v.061a4.923 4.923 0 0 0 3.946 4.827 4.996 4.996 0 0 1-2.212.085 4.937 4.937 0 0 0 4.604 3.417 9.868 9.868 0 0 1-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 0 0 7.557 2.209c9.054 0 13.999-7.496 13.999-13.986 0-.209 0-.42-.015-.63a9.936 9.936 0 0 0 2.46-2.548l-.047-.02z"/>
                  </svg>
                </a>
              </li>
              <li class="social-item nav-item">
                <a href="https://www.instagram.com/holbertonschool/" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Instagram icon
                    </title>
                    <path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913a5.885 5.885 0 0 0 1.384 2.126A5.868 5.868 0 0 0 4.14 23.37c.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558a5.898 5.898 0 0 0 2.126-1.384 5.86 5.86 0 0 0 1.384-2.126c.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913a5.89 5.89 0 0 0-1.384-2.126A5.847 5.847 0 0 0 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227a3.81 3.81 0 0 1-.899 1.382 3.744 3.744 0 0 1-1.38.896c-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421a3.716 3.716 0 0 1-1.379-.899 3.644 3.644 0 0 1-.9-1.38c-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 1 0 0-12.324zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405a1.441 1.441 0 0 1-2.88 0 1.44 1.44 0 0 1 2.88 0z"/>
                  </svg>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <hr>
        <div class="row">
          <div class="col-1-2">
            <p class="footer-copyright">© 2020 Techium, made with ? by students at Holberton School.</p>
          </div>
          <div class="col-1-2">
            <ul class="footer-nav nav">
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Terms of use</a>
              </li>
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Privacy Policy</a>
              </li>
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Cookie Policy</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </body>
</html>
```

### `CSS starter file`

```
/* SUMMARY
    1. GLOBAL
    2. LAYOUT
    3. SECTION
    4. CARD
*/

/*** 1. GLOBAL ***/

/* Reset / Normalize
   ============================= */

/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0}main{display:block}h1{font-size:2em;margin:.67em 0}hr{box-sizing:content-box;height:0;overflow:visible}pre{font-family:monospace,monospace;font-size:1em}a{background-color:transparent}abbr[title]{border-bottom:none;text-decoration:underline;text-decoration:underline dotted}b,strong{font-weight:bolder}code,kbd,samp{font-family:monospace,monospace;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}img{border-style:none}button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;line-height:1.15;margin:0}button,input{overflow:visible}button,select{text-transform:none}[type=button],[type=reset],[type=submit],button{-webkit-appearance:button}[type=button]::-moz-focus-inner,[type=reset]::-moz-focus-inner,[type=submit]::-moz-focus-inner,button::-moz-focus-inner{border-style:none;padding:0}[type=button]:-moz-focusring,[type=reset]:-moz-focusring,[type=submit]:-moz-focusring,button:-moz-focusring{outline:1px dotted ButtonText}fieldset{padding:.35em .75em .625em}legend{box-sizing:border-box;color:inherit;display:table;max-width:100%;padding:0;white-space:normal}progress{vertical-align:baseline}textarea{overflow:auto}[type=checkbox],[type=radio]{box-sizing:border-box;padding:0}[type=number]::-webkit-inner-spin-button,[type=number]::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}[type=search]::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}details{display:block}summary{display:list-item}template{display:none}[hidden]{display:none}

/* Variables
   ============================= */

   :root {
    --color-primary: #D73953;
    --color-black:  #090909;
    --color-white: #ffffff;
    --color-grey: #a0a0a0;
    --color-light-grey: #f3f3f3;
    --color-dark-grey: #353535;
  
    --text-color: var(--color-black);
  
    --font-family-base: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
    --font-family-title: 'Raleway', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  
    --font-size-small: 1.2rem;
    --font-size-medium: 1.6rem;
    --font-size-large: 1.8rem;
    --font-size-x-large: 2.3rem;
    --font-size-xx-large: 4.8rem;
  
    --font-weight-regular: 400;
    --font-weight-bold: 700;
  
    --line-height-small: 1.2;
    --line-height-base: 1.5;
    --line-height-big: 1.8;
  
    /** SECTION **/
    --section-padding: 5rem 0;
    --section-header-padding: 0 0 3rem;
    --section-header-align: center;
    --section-title-font-size: var(--font-size-xx-large);
    --section-title-font-weight: var(--font-weight-bold);
    --section-title-line-height: var(--line-height-small);
    --section-title-margin: 0;
    --section-title-color: var(--color-black);
    --section-tagline-transform: uppercase;
    --section-tagline-color: var(--color-primary);
    --section-tagline-font-family: var(--font-family-headings);
    --section-tagline-font-weight: var(--font-weight-bold);
    --section-tagline-margin: 0;
    --section-body-padding: 2rem 0 4rem;
    --section-footer-padding: 3rem 0 0;
    --section-footer-align: center;
  
    /** HEADER **/
    --header-padding: 4rem 0 0;
    --header-logo-position: relative;
    --header-logo-link-display: inline-block;
    --header-logo-link-position: absolute;
    --header-logo-link-top: -1rem;
    --header-logo-link-left: 0;
  
    /** FOOTER **/
    --footer-padding: 5rem 0 1rem;
  
    /** NAVBAR **/
    --nav-item-font-family: var(--font-family-headings);
    --nav-item-font-weight: var(--font-weight-bold);
    --nav-item-font-size: var(--font-size-medium);
    --nav-item-letter-spacing: .04rem;
    --nav-item-display: inline-block;
    --nav-item-margin: 0 2rem 0 0;
    --nav-item-link-hover: var(--color-white);
  
    /** BUTTON **/
    --button-display: inline-block;
    --button-padding: 1.5rem 3rem;
    --button-border: var(--color-primary) solid 0.2rem;
    --button-color: var(--color-black);
    --button-text-decoration: none;
    --button-font-size: var(--font-size-large);
    --button-hover-color: var(--color-white);
    --button-hover-text-decoration: none;
    --button-hover-background: var(--color-primary);
  
    /** MOTION **/
    --transition-duration: .3s;
    --transition-cubic-bezier: cubic-bezier(0.17, 0.67, 0, 1.01);
  }
  
  /* Base
      ============================= */
  
  *, *:before, *:after {
    box-sizing: border-box;
  }
  
  html {
  scroll-behavior: smooth;
  font-size: 62.5%;
  }
  
  body {
    color: var(--text-color);
    font-family: var(--font-family-base);
    font-size: var(--font-size-medium);
    font-weight: var(--font-weight-regular);
    line-height: var(--line-height-base);
  }
  
  h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-family-title);
    font-weight: var(--font-weight-bold);
  }
  
  a {
    color: var(--text-color);
    text-decoration: none;
  }
  
  a:visited {
    font-style: italic;
  }
  
  a:hover {
    text-decoration: underline;
  }
  
  a:active {
    background-color: var(--color-light-grey);
  }
  
  .button {
    display: var(--button-display);
    padding: var(--button-padding);
    border: var(--button-border);
    font-size: var(--button-font-size);
    color: var(--button-color);
    text-decoration: var(--button-text-decoration);
  }
  
  .button:hover {
    color: var(--button-hover-color);
    text-decoration: var(--button-hover-text-decoration);
    background: var(--button-hover-background);
    transition-duration: var(--transition-duration);
    transition-property: color, background-color;
  }
  
  /* Helpers
      ============================= */
  
  .visually-hidden:not(:focus):not(:active) {
    position: absolute !important;
    height: 1px;
    width: 1px;
    overflow: hidden;
    clip: rect(1px, 1px, 1px, 1px);
    white-space: nowrap;
  }
  
  /*** 2. LAYOUT ***/
  
  /* Layout
      ============================= */
  
  .container {
    width: 960px;
    margin-left: auto;
    margin-right: auto;
  }
  
  /* Grid
      ============================= */
  
  ul.row {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  
  .row::after {
    content: '';
    display: table;
    clear: both;
  }
  
  [class*='col-'] {
    float: left;
    padding: 0.5rem;
  }
  
  .col-1-3 {
    width: 33.33%;
  }
  
  .col-1-2 {
    width: 50%;
  }
  
  /* Navbar
      ============================= */
  
  .navbar-menu {
    float: right;
  }
  
  .nav {
    margin: 0;
    padding: 0;
    list-style: none;
    text-align: center;
  }
  
  .nav .nav-item {
    font-family: var(--nav-item-font-family);
    font-weight: var(--nav-item-font-weight);
    font-size: var(--nav-item-font-size);
    letter-spacing: var(--nav-item-letter-spacing);
    display: var(--nav-item-display);
    margin: var(--nav-item-margin);
  }
  
  .nav .nav-link {
    display: block;
    padding: 0.5rem 0;
    position: relative;
  }
  
  .nav .nav-link:hover {
    color: var(--nav-item-link-hover);
    text-decoration: none;
  }
  
  .nav .nav-link::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: var(--color-white);
    width: 0;
    height: 0.2rem;
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .nav .nav-item:hover .nav-link::before {
    background-color: var(--color-primary);
    width: 100%;
  }
  
  /* Header
      ============================= */
  
  .header {
    padding: var(--header-padding);
         position: relative;
         z-index: 3;
         background: transparent;
  }
  
  .header-logo {
    position: var(--header-logo-position);
  }
  
  .header-logo a {
    display: var(--header-logo-link-display);
    position: var(--header-logo-link-position);
    top: var(--header-logo-link-top);
    left: var(--header-logo-link-left);
  }
  
  /* Footer
      ============================= */
  
  .footer {
    --nav-item-font-weight: normal;
    --nav-item-font-size: var(--font-size-small);
    padding: var(--footer-padding);
  }
  
  .footer-copyright {
    margin: 0;
    font-size: var(--font-size-small);
    color: var(--text-color);
  }
  
  .footer ul {
    text-align: right;
  }
  
  .footer-address {
    color: var(--text-color);
  }
  
  .social-link {
    display: block;
  }
  
  .social-link > svg {
    fill: var(--text-color);
  }
  
  /*** 3. SECTION ***/
  
  /* Section (all styles)
      ============================= */
  
  .section {
    padding: var(--section-padding);
  }
  
  .section-header {
    text-align: var(--section-header-align);
    padding: var(--section-header-padding);
  }
  
  .section-title {
    font-size: var(--section-title-font-size);
    font-weight: var(--section-title-font-weight);
    line-height: var(--section-title-line-height);
    margin: var(--section-title-margin);
    color: var(--section-title-color);
  }
  
  .section-tagline {
    color: var(--section-tagline-color);
    font-family: var(--section-tagline-font-family);
    text-transform: var(--section-tagline-transform);
    font-weight: var(--section-tagline-font-weight);
    margin: var(--section-tagline-margin);
  }
  
  .section-body {
    padding: var(--section-body-padding);
  }
  
  .section-footer {
    padding: var(--section-footer-padding);
    text-align: var(--section-footer-align);
  }
  
  /* Section theming
      ============================= */
  
  [data-section-theme="dark"] {
    --button-color: var(--color-white);
    --text-color: var(--color-white);
    --section-title-color: var(--color-white);
    background-color: #010101;
  }
  
  /* Section HERO
      ============================= */
  
  .section-hero {
    background-position: 75% 0;
    background-repeat: no-repeat;
    background-size: 90rem auto;
    background-color: #010101;
  }
  
  .section-hero .section-title {
    margin-bottom: 5rem;
  }
  
  .section-hero .section-inner {
    padding: 10rem 40rem 2rem 0;
  }
  
  /*** 4. CARD ***/
  
  /* Card (all styles)
      ============================= */
  
  .card-category {
    color: var(--color-primary);
  }
  
  /* Card WORK
      ============================= */
  
  .card-work .card-outer {
    position: relative;
    overflow: hidden;
  }
  
  .card-work:hover .card-outer {
    transform: scale(0.95);
  }
  
  .card-work .card-image img {
    height: 30rem;
    width: 100%;
    object-fit: cover;
    vertical-align: bottom;
  }
  
  .card-work:hover .card-image {
    transform: scale(1.2);
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .card-work .card-inner {
    position: absolute;
    top: -0.1rem;
    left: -0.1rem;
    right: -0.1rem;
    bottom: -0.1rem;
    z-index: 1;
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .card-work:hover .card-inner {
    background-color: rgba(0, 0, 0, 0.7);
  }
  
  .card-work .card-title {
    text-align: center;
    margin: 0;
    opacity: 0;
    height: 100%;
    position: relative;
  }
  
  .card-work .card-title a {
    display: block;
    text-decoration: none;
    padding-top: 45%;
  }
  
  .card-work .card-title a::after {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    content: '';
  }
  
  .card-work:hover .card-title {
    opacity: 1;
  }
  
  /* Card SERVICES
      ============================= */
  
  .card-services .card-title {
    margin: 0;
  }
  
  .card-services a {
    display: block;
    padding: 2rem;
    background-color: var(--color-light-grey);
  }
  
  .card-services a:hover {
    color: var(--color-white);
    background: var(--color-primary);
    text-decoration: none;
    transition-duration: 0.3s;
    transition-property: color, background-color;
  }
  
  /* Card TESTIMONIAL
      ============================= */
  
  .card-testimonial {
    text-align: center;
  }
  
  .card-testimonial .card-avatar {
    border-radius: 50%;
    width: 10rem;
    height: 10rem;
  }
  
  .card-testimonial .card-quote cite {
    display: block;
    padding-top: 1rem;
    color: var(--color-primary);
  }
  
  .card-testimonial .card-quote {
    position: relative;
  }
  
  .card-testimonial .card-quote::before {
    content: '\201C';
    position: absolute;
    top: -4.5rem;
    left: -1rem;
    color: #efeded;
    font-size: 10rem;
    z-index: -1;
  }
```

### Files for tasks 10 and onward

#### `article.html`

```
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
    <title>Article - Techium</title>
    <meta name="description" content="Description of the page less than 150 characters">
    <link rel="icon" type="image/jpg" href="../images/favicon.jpg">
    <link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700|Raleway:700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="00-styles.css">
  </head>
  <body>
    <!– Header –>
    <header class="header" data-section-theme="dark">
      <div class="container">
        <div class="header-container">
          <div class="header-logo">
            <a href="/">
              <img src="images/logo-white.png" alt="Techium logo" width="160" height="40">
            </a>
          </div>
          <nav class="navbar-menu">
            <ul class="nav">
              <li class="nav-item">
                <a href="/" class="nav-link">Home</a>
              </li>
              <li class="nav-item">
                <a href="#services" class="nav-link">Services</a>
              </li>
              <li class="nav-item">
                <a href="#works" class="nav-link">Works</a>
              </li>
              <li class="nav-item">
                <a href="#about" class="nav-link">About</a>
              </li>
              <li class="nav-item">
                <a href="#latest_news" class="nav-link">Latest news</a>
              </li>
              <li class="nav-item">
                <a href="#testimonials" class="nav-link">Testimonials</a>
              </li>
              <li class="nav-item">
                <a href="#contact" class="nav-link">Contact</a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </header>
    <!– Main –>
    <main>
      <!– Hero section –>
      <header class="section-hero" data-section-theme="dark">
        <div class="container">
          <div class="section-body">
            <section class="section-inner">
            </section>
          </div>
        </div>
      </header>
    </main>
    <!– Footer –>
    <footer class="footer" data-section-theme="dark">
      <div  class="container">
        <div class="row">
          <div class="col-1-2">
            <img src="images/logo-white.png" alt="Techium logo" width="160" height="40">
            <address class="footer-address">
              234 Washington Street<br>
              Urbana, Illinois
            </address>
          </div>
          <div class="col-1-2">
            <ul class="social nav">
              <li class="social-item nav-item">
                <a href="https://www.facebook.com/HolbertonSchool/" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Facebook icon
                    </title>
                    <path d="M23.998 12c0-6.628-5.372-12-11.999-12C5.372 0 0 5.372 0 12c0 5.988 4.388 10.952 10.124 11.852v-8.384H7.078v-3.469h3.046V9.356c0-3.008 1.792-4.669 4.532-4.669 1.313 0 2.686.234 2.686.234v2.953H15.83c-1.49 0-1.955.925-1.955 1.874V12h3.328l-.532 3.469h-2.796v8.384c5.736-.9 10.124-5.864 10.124-11.853z"/>
                  </svg>
                </a>
              </li>
              <li class="social-item nav-item">
                <a href="https://twitter.com/holbertonschool" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Twitter icon
                    </title>
                    <path d="M23.954 4.569a10 10 0 0 1-2.825.775 4.958 4.958 0 0 0 2.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 0 0-8.384 4.482C7.691 8.094 4.066 6.13 1.64 3.161a4.822 4.822 0 0 0-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 0 1-2.228-.616v.061a4.923 4.923 0 0 0 3.946 4.827 4.996 4.996 0 0 1-2.212.085 4.937 4.937 0 0 0 4.604 3.417 9.868 9.868 0 0 1-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 0 0 7.557 2.209c9.054 0 13.999-7.496 13.999-13.986 0-.209 0-.42-.015-.63a9.936 9.936 0 0 0 2.46-2.548l-.047-.02z"/>
                  </svg>
                </a>
              </li>
              <li class="social-item nav-item">
                <a href="https://www.instagram.com/holbertonschool/" class="social-link">
                  <svg viewbox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" width="25" height="25">
                    <title>
                      Instagram icon
                    </title>
                    <path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913a5.885 5.885 0 0 0 1.384 2.126A5.868 5.868 0 0 0 4.14 23.37c.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558a5.898 5.898 0 0 0 2.126-1.384 5.86 5.86 0 0 0 1.384-2.126c.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913a5.89 5.89 0 0 0-1.384-2.126A5.847 5.847 0 0 0 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227a3.81 3.81 0 0 1-.899 1.382 3.744 3.744 0 0 1-1.38.896c-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421a3.716 3.716 0 0 1-1.379-.899 3.644 3.644 0 0 1-.9-1.38c-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 1 0 0-12.324zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405a1.441 1.441 0 0 1-2.88 0 1.44 1.44 0 0 1 2.88 0z"/>
                  </svg>
                </a>
              </li>
            </ul>
          </div>
        </div>
        <hr>
        <div class="row">
          <div class="col-1-2">
            <p class="footer-copyright">© 2020 Techium, made with ? by students at Holberton School.</p>
          </div>
          <div class="col-1-2">
            <ul class="footer-nav nav">
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Terms of use</a>
              </li>
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Privacy Policy</a>
              </li>
              <li class="footer-nav-item nav-item">
                <a href="#" class="footer-nav-link">Cookie Policy</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </body>
</html>
```

----
## Tasks
---
### 0. Add display flex

Use the starter HTML and CSS files from this task to task 10. Copy the contents of the starter files into the files that you need to produce and make the necessary changes according to the task description.<!--plain-NL-->

When using <!--plain-NL-->`display: flex;`<!--inline-NL--> on a container, all direct children become <!--plain-NL-->`flex-items`<!--inline-NL--> (and no more inline or block elements).<!--plain-NL-->

With display flex, margins are not collapsing as they would with block items. Also remember that flexbox is 1-dimensional system (vs CSS Grid which is a 2 dimensional system)<!--plain-NL-->

In the <!--plain-NL-->`/* Grid`<!--inline-NL--> section within your CSS<!--plain-NL-->

- Add a selector for the `row` class


Property: `display`, Value: `flex`
- Property: `display`, Value: `flex`

- Property: `display`, Value: `flex`

=> Now, all children from the <!--plain-NL-->`row`<!--inline-NL--> class are flex items<!--plain-NL-->

- Entirely remove the `row::after` declaration
- Remove the `float: left` inside `[class*='col-']`

=> All elements should appear same than before using the float<!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `0-index.html, 0-styles.css`


---
### 1. Add new classes on sections

Using the files from the previous task as the base for this task:<!--plain-NL-->

In the outermost section tag for <!--plain-NL-->`services`<!--inline-NL-->

- Add the class `section-services`

In the outermost section tag for <!--plain-NL-->`works`<!--inline-NL-->

- Add the class `section-works`

In the outermost section tag for <!--plain-NL-->`about`<!--inline-NL-->

- Add the class `section-about-us`

In the outermost section tag for <!--plain-NL-->`latest_news`<!--inline-NL-->

- Add the class `section-latest-news`

In the outermost section tag for <!--plain-NL-->`testimonial`<!--inline-NL-->

- Add the class `section-testimonial`

In the outermost section tag for <!--plain-NL-->`contact`<!--inline-NL-->

- Add the class `section-contact`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `1-index.html, 1-styles.css`


---
### 2. Reverse order Latest news cards

Using the files from the previous task for this task:<!--plain-NL-->

The <!--plain-NL-->`flex-direction`<!--inline-NL--> property says how flex items are placed on the main axis and their direction (normal or reversed).<!--plain-NL-->

`flex-direction`<!--inline-NL--> is sometimes used when doing responsive design. Some elements may appear better when they are in column mode on mobile and row when on desktop.<!--plain-NL-->

`row-reverse`<!--inline--> and <!--plain-->`column-reverse`<!--inline--> should be used in specific situation. The visual order of elements should be the same visually and in the HTML code. Refer to <!--plain-->[flex-direction - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction) <!--link--> for more information<!--plain-->

In your CSS file:<!--plain-NL-->

Before <!--plain-NL-->`/*** 4. CARD ***/`<!--inline-NL-->, add a new comment: <!--plain-NL-->`/* Section Latest news ============================= */`<!--inline-NL-->

Under that comment section, target the <!--plain-NL-->`row`<!--inline-NL--> class inside <!--plain-NL-->`section-latest-news`<!--inline-NL--> class<!--plain-NL-->

- Property: `flex-direction`, Value: `row-reverse`

The Latest news should appear in a reverse order. <!--plain-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `2-index.html, 2-styles.css`


---
### 3. Simplify services list

Using the files from the previous task for this task:<!--plain-NL-->

`flex-wrap`<!--inline--> is a property that can force the flex items to be in one or multiple lines. Learn more about it <!--plain-->[here](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap) <!--link-->.<!--plain-->

In the <!--plain-NL-->`Services section`<!--inline-NL--> of <!--plain-NL-->`3-index.html`<!--inline-NL-->, remove the second <!--plain-NL-->`ul`<!--inline-NL--> and put the 3 <!--plain-NL-->`li`<!--inline-NL-->elements under the first <!--plain-NL-->`ul`<!--inline-NL-->

Now, in your CSS file, before <!--plain-NL-->`/*** 4. CARD ***/`<!--inline-NL-->, add a new comment: <!--plain-NL-->`/* Section SERVICES ============================= */`<!--inline-NL-->

Under that comment section, add a new selector targeting the <!--plain-NL-->`row`<!--inline-NL--> class inside the <!--plain-NL-->`section-services`<!--inline-NL--> class<!--plain-NL-->

- Property: `flex-wrap`, Value: `wrap`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `3-index.html, 3-styles.css`


---
### 4. Playing around with the spacing between flex service items

Using the files from the previous task for this task:<!--plain-NL-->

In <!--plain-NL-->`4-styles.css`<!--inline-NL--> file, within the Grid section<!--plain-NL-->

- In `.col-1-3` selector

Replace the current width with `calc((100% / 3) - 2rem)`
- Replace the current width with `calc((100% / 3) - 2rem)`
- In `.col-1-2` selector

Replace the current width with `calc((100% / 2) - 2rem)`
- Replace the current width with `calc((100% / 2) - 2rem)`
- In `[class*='col-']`

Remove the padding declaration
Set Property: `margin` to `1rem`
- Remove the padding declaration
- Set Property: `margin` to `1rem`
- In `ul.row` declaration

Replace the current margin with `-1rem`
- Replace the current margin with `-1rem`

In <!--plain-NL-->`.col-1-3`<!--inline-NL--> selector<!--plain-NL-->

- Replace the current width with `calc((100% / 3) - 2rem)`

In <!--plain-NL-->`.col-1-2`<!--inline-NL--> selector<!--plain-NL-->

- Replace the current width with `calc((100% / 2) - 2rem)`

In <!--plain-NL-->`[class*='col-']`<!--inline-NL-->

- Remove the padding declaration
- Set Property: `margin` to `1rem`

In <!--plain-NL-->`ul.row`<!--inline-NL--> declaration<!--plain-NL-->

- Replace the current margin with `-1rem`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `4-index.html, 4-styles.css`


---
### 5. Flexify the header

Using the files from the previous task for this task:<!--plain-NL-->

In your <!--plain-NL-->`5-index.html`<!--inline-NL--> file, inside the Header section<!--plain-NL-->

- Wrap the div with class `header-logo` and the nav with class `navbar-menu` with a `div` that has `header-container` as a class

In your <!--plain-NL-->`5-styles.css`<!--inline-NL--> file, <!--plain-NL-->

- Inside the `/* Header` section
- Add a selector for the `header-container` class


Property: `display`, Value: `flex`
Property: `justify-content`, Value: `space-between`
- Property: `display`, Value: `flex`
- Property: `justify-content`, Value: `space-between`
- Remove `header-logo` and `header-logo a` rules
- Remove the `navbar-menu` rule
- In the variables section

Remove


`header-logo-position`
`header-logo-link-display`
`header-logo-link-position`
`header-logo-link-top`
`header-logo-link-left`
- Remove


`header-logo-position`
`header-logo-link-display`
`header-logo-link-position`
`header-logo-link-top`
`header-logo-link-left`
- `header-logo-position`
- `header-logo-link-display`
- `header-logo-link-position`
- `header-logo-link-top`
- `header-logo-link-left`

- Property: `display`, Value: `flex`
- Property: `justify-content`, Value: `space-between`

Remove the <!--plain-NL-->`navbar-menu`<!--inline-NL--> rule<!--plain-NL-->

In the variables section<!--plain-NL-->

- Remove


`header-logo-position`
`header-logo-link-display`
`header-logo-link-position`
`header-logo-link-top`
`header-logo-link-left`
- `header-logo-position`
- `header-logo-link-display`
- `header-logo-link-position`
- `header-logo-link-top`
- `header-logo-link-left`

- `header-logo-position`
- `header-logo-link-display`
- `header-logo-link-position`
- `header-logo-link-top`
- `header-logo-link-left`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `5-index.html, 5-styles.css`


---
### 6. Flexify the navbar

Using the files from the previous task for this task:<!--plain-NL-->

in <!--plain-NL-->`6-styles.css`<!--inline-NL-->, inside the <!--plain-NL-->`/* Navbar`<!--inline-NL-->section<!--plain-NL-->

- In the `nav` class selector


Property: `display`, Value: `flex`
- Property: `display`, Value: `flex`
- Inside the `.nav .nav-item` selector, remove the display declaration
- Target `.nav-item + .nav-item` inside `nav` class


Move the margin declaration from `.nav .nav-item` inside the new selector.
- Move the margin declaration from `.nav .nav-item` inside the new selector.
- In the variables section


Change the value of the variable `nav-item-margin` to be `0 0 0 2rem`
- Change the value of the variable `nav-item-margin` to be `0 0 0 2rem`

- Property: `display`, Value: `flex`

- Move the margin declaration from `.nav .nav-item` inside the new selector.

- Change the value of the variable `nav-item-margin` to be `0 0 0 2rem`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `6-index.html, 6-styles.css`


---
### 7. Align center logo and navbar

Using the files from the previous task for this task:<!--plain-NL-->

In <!--plain-NL-->`7-styles.css`<!--inline-NL-->, inside the <!--plain-NL-->`/* Header`<!--inline-NL--> section, in the <!--plain-NL-->`header-container`<!--inline-NL--> class selector,  set the property <!--plain-NL-->`align-items`<!--inline-NL--> to <!--plain-NL-->`center`<!--inline-NL-->

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `7-index.html, 7-styles.css`


---
### 8. Simplify the hero banner

Using the files from the previous task for this task:<!--plain-NL-->

In <!--plain-NL-->`8-styles.css`<!--inline-NL-->Inside the <!--plain-NL-->`/* Section HERO`<!--inline-NL--> section<!--plain-NL-->

- In the selector targeting `section-inner` class in `section-hero` class, remove the padding and replace with


Property: `display`, Value: `flex`
Property: `flex-direction`, Value: `column`
Property: `align-items`, Value: `flex-start`
Property: `justify-content`, Value: `center`
Property: `min-height`, Value: `50vh`
- Property: `display`, Value: `flex`
- Property: `flex-direction`, Value: `column`
- Property: `align-items`, Value: `flex-start`
- Property: `justify-content`, Value: `center`
- Property: `min-height`, Value: `50vh`

- Property: `display`, Value: `flex`
- Property: `flex-direction`, Value: `column`
- Property: `align-items`, Value: `flex-start`
- Property: `justify-content`, Value: `center`
- Property: `min-height`, Value: `50vh`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `8-index.html, 8-styles.css`


---
### 9. Better alignment about us

Using the files from the previous task for this task:<!--plain-NL-->

In <!--plain-NL-->`9-styles.css`<!--inline-NL-->, after the <!--plain-NL-->`/* Section SERVICES`<!--inline-NL--> section, create a <!--plain-NL-->`/* Section ABOUT US`<!--inline-NL--> section. Inside that new section, target all classes that begin with <!--plain-NL-->`col-`<!--inline-NL--> inside <!--plain-NL-->`section-about-us`<!--inline-NL--> class<!--plain-NL-->

- Property: `align-self`, Value: `center`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `9-index.html, 9-styles.css`


---
### 10.  Creating an article by fixing issues and updating hero styles

Using the CSS file from the previous task and  <!--plain-NL-->`article.html`<!--inline-NL--> (provided above in the project description) for this task:<!--plain-NL-->

In <!--plain-NL-->`10-styles.css`<!--inline-NL-->, inside the <!--plain-NL-->`/* Section HERO`<!--inline-NL--> section<!--plain-NL-->

After the <!--plain-NL-->`.section-hero`<!--inline-NL-->, add a new <!--plain-NL-->`hero-homepage`<!--inline-NL--> class selector (you will need to add that class later in your html files)<!--plain-NL-->

Move all declarations inside <!--plain-NL-->`section-hero`<!--inline-NL--> inside the new <!--plain-NL-->`hero-homepage`<!--inline-NL--> class selector<!--plain-NL-->

Inside <!--plain-NL-->`section-hero`<!--inline-NL--> class selector<!--plain-NL-->

- Property: `position`, Value: `relative`
- Property: `margin-top`, Value: `-8.5rem`

Below, target <!--plain-NL-->`.section-body`<!--inline-NL--> inside <!--plain-NL-->`section-hero`<!--inline-NL--> class<!--plain-NL-->

- Property: `padding`, Value: `10rem 4rem`

Below, target <!--plain-NL-->`.section-category`<!--inline-NL--> inside <!--plain-NL-->`section-hero`<!--inline-NL--> class<!--plain-NL-->

- Property: `color`, Value: point to the variable `color-white`
- Property: `text-transform`, Value: `uppercase`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `10-article.html, 10-styles.css`


---
### 11. Update the new hero banner

In <!--plain-NL-->`11-article.html`<!--inline-NL--> in the Hero section<!--plain-NL-->

- Add the `hero-article` class on the `&lt;header&gt;` which is in `&lt;main&gt;`
- Add this `background-image` (pic-article-02.jpg) as an inline style still on the `&lt;header&gt;`
- Inside the section with `section-inner` class


Add a `span` with the class `section-category` and the text `Digital Life`
Below, add an `h1` with the class `section-title` and the following text `Ut alios omittam, hunc appello, quem ille unum secutus est`
- Add a `span` with the class `section-category` and the text `Digital Life`
- Below, add an `h1` with the class `section-title` and the following text `Ut alios omittam, hunc appello, quem ille unum secutus est`

- Add a `span` with the class `section-category` and the text `Digital Life`
- Below, add an `h1` with the class `section-title` and the following text `Ut alios omittam, hunc appello, quem ille unum secutus est`

At the end of <!--plain-NL-->`11-styles.css`<!--inline-NL-->, create a new comment section<!--plain-NL-->

```
/*** ARTICLE PAGE ***/
/* Section HERO (article)
    ============================= */

```

Target the <!--plain-NL-->`hero-article`<!--inline-NL--> class<!--plain-NL-->

- Property: `background-size`, Value: `150rem 100rem`
- Property: `background-position`, Value: `50% 0`

Target the <!--plain-NL-->`before`<!--inline-NL--> pseudo element of <!--plain-NL-->`hero-article`<!--inline-NL--> class<!--plain-NL-->

- Property: `content`, Value: empty
- Property: `background`, Value: `rgba(0, 0, 0, 0.8)`
- Property: `position`, Value: `absolute`
- Property: `top`, Value: `0`
- Property: `right`, Value: `0`
- Property: `left`, Value: `0`
- Property: `bottom`, Value: `0`
- Property: `z-index`, Value: `0`

Target the <!--plain-NL-->`section-inner`<!--inline-NL--> class inside the <!--plain-NL-->`hero-article`<!--inline-NL--> class<!--plain-NL-->

- Property: `text-align`, Value: `center`
- Property: `align-items`, Value: `center`
- Property: `min-height`, Value: `40vh`

Target the <!--plain-NL-->`section-body`<!--inline-NL--> class inside the <!--plain-NL-->`hero-article`<!--inline-NL--> class<!--plain-NL-->

- Property: `position`, Value: `relative`
- Property: `padding`, Value: `7rem 0 0`
- Property: `z-index`, Value: `2`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `11-article.html, 11-styles.css`


---
### 12. The structure of the main article

In your <!--plain-NL-->`12-article.html`<!--inline-NL--> file, in the Hero section<!--plain-NL-->

- After the header, create a `&lt;div&gt;`and set its class to `main-article` (this div will be siblings with the Hero section header)
- Create a div inside the `main-article` div and set the class to `container`
- Create a `div` with the class `post` inside the `container` div
- Inside the `post` div:


Create a new `article` with the class `post-content`
Below the `post-content` article, add the comment `&lt;!-- Aside section --&gt;`
Sibling to the `post-content` article and after the comment, create an `aside` with the class `post-aside`
Inside `post-aside` aside, create 2 divs:


The first with the class `post-meta`
The second with the class `post-share`
- Create a new `article` with the class `post-content`
- Below the `post-content` article, add the comment `&lt;!-- Aside section --&gt;`
- Sibling to the `post-content` article and after the comment, create an `aside` with the class `post-aside`
- Inside `post-aside` aside, create 2 divs:


The first with the class `post-meta`
The second with the class `post-share`
- The first with the class `post-meta`
- The second with the class `post-share`

- Create a new `article` with the class `post-content`
- Below the `post-content` article, add the comment `&lt;!-- Aside section --&gt;`
- Sibling to the `post-content` article and after the comment, create an `aside` with the class `post-aside`
- Inside `post-aside` aside, create 2 divs:


The first with the class `post-meta`
The second with the class `post-share`
- The first with the class `post-meta`
- The second with the class `post-share`

- The first with the class `post-meta`
- The second with the class `post-share`

In your <!--plain-NL-->`12-styles.css`<!--inline-NL-->:<!--plain-NL-->

- Target the `main-article` class

Property: `padding`, Value: `5rem 0`
- Property: `padding`, Value: `5rem 0`
- Add the below separator comment

Target the <!--plain-NL-->`main-article`<!--inline-NL--> class<!--plain-NL-->

- Property: `padding`, Value: `5rem 0`

Add the below separator comment<!--plain-NL-->

```
/* Post
    ============================= */

```

- Target the `post` class


Property: `display`, Value: `flex`
- Property: `display`, Value: `flex`
- Target the `post-content` class


Property: `width`, Value: `100%`
- Property: `width`, Value: `100%`
- Target the `post-aside` class


Property: `order`, Value: `-1`
Property: `min-width`, Value: `20%`
- Property: `order`, Value: `-1`
- Property: `min-width`, Value: `20%`

- Property: `display`, Value: `flex`

- Property: `width`, Value: `100%`

- Property: `order`, Value: `-1`
- Property: `min-width`, Value: `20%`

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `12-article.html, 12-styles.css`


---
### 13. The meta list inside the aside section

In your <!--plain-NL-->`13-article.html`<!--inline-NL-->

- Create an unordered list inside the `post-meta` div with the classes `post-meta-list` and `row`

Create a first `&lt;li&gt;` with the class `post-meta-author`

Create the HTML tag that show a stronger importance


Text: `Written by:`

Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`


Create a second `&lt;li&gt;` with the class `post-meta-date`

Create the HTML tag that show a stronger importance


Text: `Posted on:`

Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`

Create a third `&lt;li&gt;` with the class `post-meta-tag`

Create the HTML tag that show a stronger importance


Text: `Tags:`

Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Create a first `&lt;li&gt;` with the class `post-meta-author`

Create the HTML tag that show a stronger importance


Text: `Written by:`

Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`
- Create the HTML tag that show a stronger importance


Text: `Written by:`
- Text: `Written by:`
- Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`
- Href: `#`
- Rel: `author`
- Text: `William Attaway`
- Create a second `&lt;li&gt;` with the class `post-meta-date`

Create the HTML tag that show a stronger importance


Text: `Posted on:`

Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`
- Create the HTML tag that show a stronger importance


Text: `Posted on:`
- Text: `Posted on:`
- Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`
- Create a third `&lt;li&gt;` with the class `post-meta-tag`

Create the HTML tag that show a stronger importance


Text: `Tags:`

Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Create the HTML tag that show a stronger importance


Text: `Tags:`
- Text: `Tags:`
- Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`
- Href: `#`
- Rel: `tag`
- Text: `Web Design`
- Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Href: `#`
- Rel: `tag`
- Text: `UX`

- Create a first `&lt;li&gt;` with the class `post-meta-author`

Create the HTML tag that show a stronger importance


Text: `Written by:`

Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`
- Create the HTML tag that show a stronger importance


Text: `Written by:`
- Text: `Written by:`
- Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`
- Href: `#`
- Rel: `author`
- Text: `William Attaway`
- Create a second `&lt;li&gt;` with the class `post-meta-date`

Create the HTML tag that show a stronger importance


Text: `Posted on:`

Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`
- Create the HTML tag that show a stronger importance


Text: `Posted on:`
- Text: `Posted on:`
- Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`
- Create a third `&lt;li&gt;` with the class `post-meta-tag`

Create the HTML tag that show a stronger importance


Text: `Tags:`

Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Create the HTML tag that show a stronger importance


Text: `Tags:`
- Text: `Tags:`
- Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`
- Href: `#`
- Rel: `tag`
- Text: `Web Design`
- Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Href: `#`
- Rel: `tag`
- Text: `UX`

- Create the HTML tag that show a stronger importance


Text: `Written by:`
- Text: `Written by:`
- Create a link


Href: `#`
Rel: `author`
Text: `William Attaway`
- Href: `#`
- Rel: `author`
- Text: `William Attaway`

- Text: `Written by:`

- Href: `#`
- Rel: `author`
- Text: `William Attaway`

- Create the HTML tag that show a stronger importance


Text: `Posted on:`
- Text: `Posted on:`
- Use the HTML tag for date / time
    - Datetime: `2019-10`
    - Text: `October 2019`

- Text: `Posted on:`

- Create the HTML tag that show a stronger importance


Text: `Tags:`
- Text: `Tags:`
- Create an unordered list with the class `tag-list`

First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`

Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`
- Href: `#`
- Rel: `tag`
- Text: `Web Design`
- Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Href: `#`
- Rel: `tag`
- Text: `UX`

- Text: `Tags:`

- First `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `Web Design`
- Href: `#`
- Rel: `tag`
- Text: `Web Design`
- Second `&lt;li&gt;` contain a link


Href: `#`
Rel: `tag`
Text: `UX`
- Href: `#`
- Rel: `tag`
- Text: `UX`

- Href: `#`
- Rel: `tag`
- Text: `Web Design`

- Href: `#`
- Rel: `tag`
- Text: `UX`

Update <!--plain-NL-->`13-styles.css`<!--inline-NL--> with this information<!--plain-NL-->

Add a separator comment <!--plain-NL-->

```
/* Post Meta
    ============================= */

```

Target the <!--plain-NL-->`post-meta-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `flex-direction`, Value: `column`

Target the <!--plain-NL-->`strong`<!--inline-NL--> tag inside <!--plain-NL-->`post-meta-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `color`, Value: point to the variable `color-primary`
- Property: `font-size`, Value: point to the variable `font-size-small`
- Property: `text-transform`, Value: `uppercase`
- Property: `display`, Value: `block`

Target all classes that start with <!--plain-NL-->`post-meta-`<!--inline-NL--> inside <!--plain-NL-->`post-meta-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `margin-bottom`, Value: `1rem`
- Property: `padding-bottom`, Value: `1rem`
- Property: `border-bottom`, Values: `0.2rem solid` and point to the `color-light-grey` variable

Target the last child of all classes that start with <!--plain-NL-->`post-meta`<!--inline-NL--> inside <!--plain-NL-->`post-meta-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `border`, Value: `none`
- Property: `margin-bottom`, Value: `3rem`

Add a separator comment<!--plain-NL-->

```
/* Tag list
    ============================= */

```

Target the <!--plain-NL-->`tag-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `padding`, Value: `0`
- Property: `list-style`, Value: `none`

Target all <!--plain-NL-->`li`<!--inline-NL--> inside the <!--plain-NL-->`tag-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `display`, Value: `inline`

Target the <!--plain-NL-->`after`<!--inline-NL--> pseudo element on the <!--plain-NL-->`li`<!--inline-NL--> inside <!--plain-NL-->`tag-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `content`, Value: `", "` (space after the comma)

Target the <!--plain-NL-->`after`<!--inline-NL--> pseudo element of the last-child on the <!--plain-NL-->`li`<!--inline-NL--> inside <!--plain-NL-->`tag-list`<!--inline-NL--> class<!--plain-NL-->

- Property: `content`, Value: empty

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `13-article.html, 13-styles.css`


---
### 14. Add the share social icons

In your <!--plain-NL-->`14-article.html`<!--inline-NL-->, inside the <!--plain-NL-->`post-share`<!--inline-NL--> div<!--plain-NL-->

- Copy paste the `social nav` list (already existing in the footer) inside
- Remove the `li` with Instagram (3rd one)
- Replace the `href` in the links with a default value ( `#`)

**Repo:**

- GitHub repository: `atlas-web_front_end`
- Directory: `flexbox`
- File: `14-article.html, 14-styles.css`