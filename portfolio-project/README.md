cYour Portfolio Page
===

Show off your peacock feathers as you begin to spread your wings and take flight into the world software development. Okay, peacocks can't fly, but you get the point - your portfolio will give you a place to work and show off your coding projects!

**Table of Contents** 

- [Your Portfolio Page](#your-portfolio-page)
  - [Overview](#overview)
    - [Specs](#specs)
    - [Take Away](#take-away)
    - [Work Flow](#work-flow)
    - [Type of App](#type-of-app)
  - [Intro to CSS](#intro-to-css)
    - [Padding](#padding)
    - [Margins](#margins)
    - [Classes and IDs](#classes-and-ids)
  - [Lesson Steps](#lesson-steps)
    - [TODO 1 : Create Portfolio Page](#todo-1--create-portfolio-page)
    - [TODO 2 : Add a Title](#todo-2--add-a-title)
    - [TODO 3 : Add CSS](#todo-3--add-css)
    - [TODO 4 : Add Navigation](#todo-4--add-navigation)
      - [The Skinny on Anchor Tags](#the-skinny-on-anchor-tags)
      - [Relative vs Absolute File Paths](#relative-vs-absolute-file-paths)
    - [TODO 5 : Create the Main Content](#todo-5--create-the-main-content)
    - [Checking Your Work](#checking-your-work)
    - [Extra Credit](#extra-credit)

## Overview

### Specs

* At the end of the lesson, will have a portfolio page added to their website.  The portfolio page will list all of the projects we'll complete in our studies, and help begin a decent resume of your coding skills! In this lesson, we also delve a bit deeper into Cascading Style Sheets (CSS) and hyperlinks.

### Take Away

* Building a web page from scratch
* Basics of Cascading Style Sheets (CSS)
* Basic web page navigation through hyperlinks, aka anchor tags
* Relative vs absolute file paths
* Using git and GitHub

### Work Flow

We're going to continue building out your website by adding a portfolio page where you can show off your work. We'll also spruce up the site by further developing the design with CSS.

To complete the assignment, below you'll find numbered **TODO** lesson steps. While reading this lesson, whenever you come across a TODO step, you are expected to implement this step, which may require you to create a file, or insert some HTML, CSS or JavaScript in the appropriate place. Please follow the instructions closely. Sometimes, however, we may be showing you code examples to make a point, so you only need to add code if we're explicitly telling you to do a lesson step, so please be aware of the actual lesson steps.

### Type of App

We are building a website, to be viewed live on the web at your GitHub page, and it will be viewed in a web browser, like Chrome.

## Intro to CSS

Cascading Style Sheets, or CSS, is what give websites style. Without CSS, the internet would be a very bland place.

Facebook with CSS:

<img src="https://github.com/OperationSpark/teacher-training-curriculum/raw/master/img/facebook-with-css.png">

Facebook without CSS:

<img src="https://github.com/OperationSpark/teacher-training-curriculum/raw/master/img/facebook-without-css.png">

Here are just a few things you can do with CSS:

* Choose colors of everything on the page like the background, font, or main menu.
* Set the size of any element such as font size, width of the entire site, or an image
* Create borders or drop shadows around whole sites, images, and menus
* Change the state of items when hovering over them

To make CSS work you select an HTML element and assign various properties to it.

One of the first things you might want to do on any site, if you're not satisfied with white, is to change the background color.

```css
body {
  background-color: blue;
}
```

Here, we're selecting the body element, which encompasses the entire page, and setting the background color to blue. The word, `body` is a **selector** and the `background-color` is a style **property**. Look over the formatting in the above CSS.

We have:

* The selector
* A curly bracket
* The property
* A colon
* The value of the property
* A semicolon
* A curly bracket

The spacing and indenting matter a lot for legibility! You and your fellow developers will appreciate well formatted HTML, CSS, and JavaScript because it will make it extremely easy to understand your intentions.  Pay close attention to indentation when coding!

Let's talk about a few more common CSS properties, that is, ways in which we can alter an element's appearance.

### Padding

**Padding** is the amount space around content that is inside of an element. You can set padding on all four sides of an element.

Here's an example of padding around a div:

```css
div {
  padding-top: 20px;
  padding-right: 10px;
  padding-bottom: 5px;
  padding-left: 0;
}
```

Remember that the `div` is the **selector** and there are four **properties** which apply to padding.

### Margins

A **margin** is the amount of space outside of an element. You can set it on all four side like padding.

### Classes and IDs

By more concretely describing HTML elements by assigning an id or class, we can select those elements uniquely by their id or grouped by their class. You will often want to apply styling to only certain HTML elements rather than all of them. In the above code examples we're selecting the `<div>` elements. The CSS styling you applied will change the look of all of the `<div>` elements across the site. To give an element a class or id we can add an attribute to their HTML tag:

```html
<div class="myClass">
  <!-- div content goes here -->
</div>

<div id="myId">
  <!-- div content goes here -->
</div>
```

class selectors in CSS are created with a period and the class name:

```css
.myClass {
  background-color: blue;
}
```

id selectors in CSS are created with a hashtag and the id name:

```css
#myId {
  background-color: red;
}
```

Now, only the first `<div>` with `class="myClass"` will have a blue background. Meanwhile only the `<div>` with `id="myId"` will hvae a red background. Ok, let's move on to create our portfolio!

## Lesson Steps

### TODO 1 : Create Portfolio Page

We're going to build the page from scratch:

1. On the left side of your workspace, locate the `portfolio-project` folder. 

2. Inside of this folder, you should see a file called `portfolio.html`. Within this `portfolio.html` file, let's create the scaffolding HTML tags we need for any web page by adding the following HTML tags:

```html
<!DOCTYPE HTML>
<html>
  <head>
  </head>

  <body>
    <div id="all-contents">
		
    </div>
  </body>
</html>
```

### TODO 2 : Add a Title

Add a title tag within the `<head>` tag of the portfolio.html page.  Use the same title you used on your `index.html` page:

```html
<head>
  <title>Sheba's Amazing Website</title>
</head>
```

### TODO 3 : Add CSS

Let's add some style! Within the `<head>` tag, but under the `<title>` tag you just created in the last step, copy and paste in the following CSS, include the `<style></style>` tags:

```html
<style type="text/css">
  body {
    background: rgb(125, 198, 205);
    color: rgb(45, 45, 45);
    padding: 10px;
    font-family: arial;
  }
  header {
    font-size: 1.5em;
    font-weight: bold;
  }
  h1 {
    margin: 10px;
  }
  #all-contents {
    max-width: 800px;
    margin: auto;
  }

  /* navigation menu */
  nav {
    background: rgb(239, 80, 41);
    margin: 0 auto;
    display: flex;
    padding: 10px;
  }
  nav header {
    display: flex;
    align-items: center;
    color: rgb(255, 255, 255);
    flex: 1;
  }
  nav ul {
    list-style-image: none;
  }
  nav li {
    display: inline-block;
    padding: 0 10px;
  }
  nav a {
    text-decoration: none;
    color: #fff;
  }

  /* main container area beneath menu */
  main {
    background: rgb(245, 238, 219);
    display: flex;
  }
  .content {
    flex: 1;
    padding: 15px;
  }
</style>
```

We want our portfolio page to fit with our Home page so copy over any changes you made to the CSS in `index.html`! 

### TODO 3: Part 2, Style the portfolio

Now add some styling that is unique to portfolio. Paste this within your `style` tags below the `.content` block:

```css
/* portfolio styles */
#portfolio {
  list-style-type: none;
  padding-left: 0;
}

#portfolio li {
  background: #fff;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 10px;
}

#portfolio li:hover {
  background: #eee;
} 

#portfolio a {
  text-decoration: none;
  color: #454545;
}
```

### TODO 4 : Add Navigation

Within the `<div id="all-contents">` tag, insert the following structure to create our navigation:

```html
<div id="all-contents">
  <nav>
    <header>Sheba's Glorious Website</header>
    <ul>
      <li>
        <a href="index.html">Home</a>
      </li>
      <li>
        <a href="portfolio.html">Portfolio</a>
      </li>
    </ul>
  </nav>
</div>
```

Here, we've added the same navigation on our home page, `index.html`.  It's common to have the same navigation options across an entire website, so the user can get to wherever from wherever!  Inside our `<nav>`, we have an unordered list, (`<ul>`), with 2 list items (`<li>`).  This list items contain anchor tags (`<a>`).

#### The Skinny on Anchor Tags

Anchor tags are the original hypertext - they allow us to link one web page to another web page, and also making things on a web page, _clickable_.

The text between the start and end of the tag, like the HERE in `<a>HERE</a>`, represents what the user will see on the web page as _clickable_.  In our nav, our anchor links use the text `Home` and `Portfolio`, so that's what will be displayed to the user in the nav bar. But links can wrap images or `<div>` tags or other HTML elements, making them _clickable_.

The first part of the `<a>` tag requires the `href` attribute.  `href` stands for hypertext reference, and this value is the URL or file path to the page or file we want the browser to load when a user _clicks_ on our link.  The file paths `index.html` and `portfolio.html` are _relative_ paths, that is, they are relative in location to the file in which they occur, in this case, the `portfolio.html` file.  Paths that include the full hard-drive location or an Internet domain are considered _absolute_ paths, as in, the fully qualified address of the file.

Here's an example of an absolute URL:

    https://github.com/OperationSpark/portfolio/blob/master/README.md

Or, on your computer, an absolute file path from the root directory of the file system:

    /home/ubuntu/workspace/README.md

#### Relative vs Absolute File Paths

One way to think of relative vs absolute paths is to describe _where_ the person sitting next to you is _located_.

* Relative: "She's right next to me"
* Absolute: "She's in the Universe, in the Milky Way galaxy, on planet Earth, in the north west hemisphere, in North America, in the United States, in Louisiana, in New Orleans, in the CBD, in some office building, on the 17th floor, in room 1701, sitting at the desk number 1".

Because we are able to relatively describe the location of the files to which we're linking in our website, we don't have to spell out their absolute path, and this is better for portability.  If we were to use absolute paths, but then move our website to another part of the file system or to another computer, the absolute paths would change, and our links would break.

In the example of describing _where_ the person sitting next to you is _located_, if you both move to another room, the relative description stays the same (right next to me), but the absolute description does not (we have to account for the fact that we're in a different room, at different desks, etc)!

### TODO 5 : Create the Main Content

Now we want to create a place where our work throughout the course will be displayed. 
* Beneath the entire `<nav></nav>` section create a pair of `<main>` tags. 
* Nested within the `<main>` tags create a `<div>` with `class="content"`
* Add an `<h1>` header and title this section `Portfolio`
* Lastly, add an unordered lists `<ul>` with `id="portfolio"`

Your code will look like this...
```html
<nav>
  <!-- Nav stuff here...-->
</nav> 

<main>
  <div class="content">
    <h1>Portfolio</h1>
    <ul id="portfolio">
      <!-- List items here -->
    </ul>
  </div>
</main>
```

So, we created an unordered list with an `id` of `portfolio`.  This will allow us to access the portfolio `<ul>` to style it, which we are doing with a CSS selector, _and_, to use JavaScript to _dynamically_ add list items to our portfolio list. Right now, there's no items in the list, but later, when we install projects, we'll see our projects begin to list themselves, to appear dynamically in our portfolio page. The term dynamic means _constant change, activity, or progress_, which describes the state of our web page in that we can change it on the fly and thus its not _static_, which is the opposite of dynamic.

### Checking Your Work

To check the status of your portfolio.html, follow these steps:
* Find the `index.html` file.
* Right click `index.html` and select "Open with Live Server".
* This will open a webpage where you can click on a link to view your First Webiste Page and Portfolio Page.
