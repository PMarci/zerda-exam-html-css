# Exam: HTML & CSS

### Getting Started
 - Fork this repository under your own account
 - Commit your progress frequently and with descriptive commit messages
 - All your answers and solutions should go in this repository

### What can I use?
 - You can use any resource online, but **please work individually**
 - Instead of copy-pasting your answers and solutions, write them in your own words.


# Tasks

## 1. Build a design (~90 minutes) [10 points]
Build the following profile cards according to the design provided.   
Follow the design as closely as possible.   
Commit an HTML and a CSS file to this repository.
![design](exercise-1.png)

### Assets
John Duck | Jane Duck | Pencil icon
--------- | --------- | -----------
![duck](duck.jpg) | ![duck](duck2.jpg) | ![pencil-icon](edit-icon.png)   

### Other data
  - Name font size: 28 pixels
  - Text size: 14 pixels
  - Font family: Arial, sans-serif

### Acceptance criteria
The task is accepted if:
  - The result follows design [2p]
  - The code follows style guide [1p]
  - The CSS & HTML are valid [1p]
  - The HTML considers semantic responsibilities [2p]
  - The code avoids code duplication [2p]
  - The CSS has meaningful and short selectors [2p]

Extra points for if:
  - the result is centered on the page [2p]


## 2. Understand code (~15 minutes) [2 points]
Read the following code snippet:   
What is the distance between the top-left corner of the document body and the yellow box?   
Give a detailed explanation below!   
Add your answer to this readme file, commit your changes to this repository.
```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        padding: 0px;
        margin: 0px;
      }
      .foo {
        top: 20px;
        left: 20px;
        width: 100px;
        height: 100px;
        position: absolute;
        background: blue;
      }
      .bar {
        top: 20px;
        left: 20px;
        width: 30px;
        height: 30px;
        position: absolute;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <div class="foo">
      <div class="bar"></div>
    </div>
  </body>
</html>
```
#### Your answer: 
The yellow box (top left corner) is located 40px to the right and 40px to the bottom of the top left corner of the `<body>` element. This is because
both descendants of the `<body>` element ("foo"and "bar") have their positioning set to absolute, that is absolute to their respective parent element.
Furthermore, none of them have a margin, or a padding set, so this positioning using top, left becomes the cumulative distance of said corners.
Considering the html document represents an two-dimensional Euclidian space, which has a norm associated to it, and because the inner product of x with itself (sqrt(x*x))is always non-negative,
we can define a distance function based on that norm (the Euclidian norm). This makes the distance of the two corners sqrt(40^2+40^2)=56.56px
[2p]


## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: 
Inline elements won't break the flow of text or other elements, they will appear inline, e. g. not forcing succeeding elements into a new line. They will accept margins and paddings, 
however they ignore height and width properties. Block elements will appear, if not set otherwise, in a new row, breaking past the previous element, 
and taking up as much space as allowed by the parent element.
Inline-block elements behave as inline elements, however they will accept height and width settings.
[2p]


### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: 
`<section>` denotes a generic section in a document, which could be a chapter, a heading, a footer, a block of text. MDN recommends sections be identified with a nested `<h>` element.
In comparison, the `<article>` tag should be used for self-contained composition, which should not be depended on it's context. It could be used for example as a forum, or blog post
or similar text. This too, should be identified by a heading. MDN mentions extra tags to be used in conjunction, such as `<adress>` and `<time>`, to identify the euthor, date and time of a
composition.
[2p]
