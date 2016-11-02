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
#### Your answer: [2p]
Foo box is nested into body with position absolute,
so this is 20px down and 20px to the right of the t-l. corner of the body.
Bar is nested into foo with an absolute position too,
so it is 20px down and 20px to the right of the t-l. corner of foo.
This adds up to 40px down and 40px to the right of the t-l. corner of the body
for the yellow box with the class "bar". Not taken into account that
the "div" element might have a default browser-style.


## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: [2p]
"Display: block" sets the type of the element as block-level element,
which is occupying the space given by its parent
(e.g. width fills the space to the right padding of the parent).
They start in new lines. They contain other elements of almost any type.

"Display: inline" sets an element as if it would be an inline element,
which only occupy space their content needs.
They do not open a new line and might overlap.
They do not have top and bottom margin or paddings.
They contain only data or other inline elements.

Inline-block setting adds the advantages of both above: the container-property of the block element (can expand to the childrens' extent and do not overlap with another block) and the inline element (only occupies the space its content needs and flows within its parent)

### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: [2p]
Sections are collection of elements thematically belonging together with heading
inlcuding part of the entire content of e.g. a homepage.
So homepages for one specific subject can be splitted to more sections.

Articles are like articles in magazines or blog posts independent from each other, with separate topics.
They could be taken out and put into another html document, they would still make sense alone.
