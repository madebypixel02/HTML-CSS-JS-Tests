<!-- *********************************************************************** -->
<!--                                                                         -->
<!--                                         =@@*   +@@+                     -->
<!--                                         =@@*   +@@+ :*%@@@%*:           -->
<!--                                         =@@*   =@@+.@@@=--%@@-          -->
<!--                                         :@@%. .#@@--@@*   +@@* .+%@@@   -->
<!-- README.md                                =%@@@@@@+ =@@*   =@@+.@@@+-=   -->
<!--                                            .---:   -@@#.  *@@--@@*      -->
<!-- By: aperez-b <aperez-b@uoc.edu>                     +@@@@@@@* +@@+      -->
<!--                                                       :-==:.  -@@#      -->
<!-- Created: 2022/12/05 16:57:45 by aperez-b                       +@@@%@   -->
<!-- Updated: 2022/12/06 13:01:35 by aperez-b                                -->
<!--                                                                         -->
<!-- *********************************************************************** -->

# Part 1. Questions

## Table of Contents

- [Question 1 Positioning](#question-1-positioning)
- [Question 2 Page Layout](#question-2-page-layout)
- [Question 3 Responsive Design](#question-3-responsive-design)
- [Explanation of the HTML and CSS Entities Used](#explanation-of-the-html-and-css-entities-used)

## Question 1 Positioning

Indicate which are the four main types of positioning in *CSS* and describe,
in your own words, their main characteristics.

### Answer 1

The four main types of positioning and their main characteristics are the following:

- **Static Positioning**: this is the standard way in which elements are laid out.
It simply positions the elements following the flow of the document. Elements go
right where we expect them to go if we did not set this property.
- **Relative Positioning**: this positioning type allows us to move the position
of an element relative to its position in the normal flow. For example, if we set
the property `top: 30px`, the element will be `30` pixels below its "normal" position.
- **Absolute Positioning**: used to position element relative to other (parent)
positioned elements. It is quite neat in cases where we might want to position some
content on a box (`<div>`). When no parent element is postioned, the base `html`
element will be used to position the element.
- **Fixed Positioning**: allows for positioning elements relative to the viewport
of the page, so it is in some sense detached from the other content on the screen.
This is useful to keep some parts of the webpage (navigation bar, "move to top"
button, etc) visible at all times.

There is also a fifth positioning type, **Sticky Positioning**, which is a mix
of **relative** and **fixed** positioning, allowing for convent to be positioned
on some part of the document until a threshold is reached, which makes the element
display in a fixed position on the viewport.

## Question 2 Page Layout

We need to develop a structure with a parent element (`.row`) that will act as
a row and twelve child elements (`.col`) that act as columns. Characteristics:

- Four columns per row.
- Even columns must be twice as wide as the odd ones.
- The space between columns has to be `25px`.
- The space between rows has to be `15px`.
- The rows have to have a minimum height of `150px` and an automatic maximum
(this height will vary depending on its content).

Write the necessary *CSS* rules for the parent and the child elements.

### Answer 2

Here is the *CSS* code to implement the table structure, inside *HTML* code
for reference:

```html
<!DOCTYPE html>
<html>
<body style="margin: 0;">
<style>
.col
{
    border: 1px solid blue;
    background-color: lightblue;
    border-radius: 5px;
    text-align: center;
}
.row
{
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 2fr;
    grid-auto-rows: minmax(150px, auto);
    row-gap: 15px;
    column-gap: 25px;
        
}
</style>
<div class="row">
    <div class="col">col1</div>
    <div class="col">col2</div>
    <div class="col">col3</div>
    <div class="col">col4</div>
    <div class="col">col5</div>
    <div class="col">col6</div>
    <div class="col">col7</div>
    <div class="col">col8</div>
    <div class="col">col9</div>
    <div class="col">col10</div>
    <div class="col">col11</div>
    <div class="col">col12</div>
    <div class="col">col13</div>
</div>
</body>
</html>
```

## Question 3 Responsive Design

### Question 3.1

Explain, in your own words, the advantages that we can get by developing
a site using the principles of responsive design, compared to one developed
with a fixed width.

#### Answer 3.1

Modern devices come in all shapes and sizes. From ultra-wide monitors to
the smallest smartwatches, all tech that can browse the web should be able
to enjoy a coherent experience. Responsive design is not only crucial to
make content easily enjoyable on every type of screen, but also allows for
making the whole experience much more coherent. A small device visiting a site
may need a more vertical interface with some parts of the site squeezed inside
a hamburger menu. Similarly, devices with wider screens should have things
laid out differently. Namely, paragraphs need not stretch the whole width,
but should rather split into different columns. Lastly, responsive design
helps adapt the web interface depending on the size of the browser window,
changing how content is displayed and resizing elements when necessary.

Fixed width sites are harder to view on certain displays, as content will
often overflow into vertical and horizontal scrollbars, as well as content
will bunch up in a rather meaningless way, making navigation on the site
a real hustle.

### Question 3.2

Write the necessary style rules so that they are applied correctly in the
following cases:

- On screens with at least `660` pixels of width, all document headings must
have a font size of `110%` with respect to the value specified in their parent,
be centered and have `10%` padding to the left and right.
- On screens with a width of at least `769` pixels and a maximum of `1023` pixels,
class `2` headers must have a font size `130%` of the value specified in their parent,
and class `3` through `6` headers must have a font size `120%` of the value specified
in their parent.
- On screens with at least `1024` pixels of width, all document headings must be
aligned to their default value and have no left and right padding.

#### Answer 3.2

- Case 1 Code

```css
@media screen and (min-width: 660px)
{
    h1, h2, h3, h4, h5, h6
    {
        font-size: 110%;
        text-align: center;
        padding: auto 10% auto 10%;
    }
}
```

- Case 2 Code

```css
@media screen and (min-width: 769px) and (max-width: 1023px)
{
    h2
    {
        font-size: 130%;
    }
    h3, h4, h5, h6
    {
        font-size: 120%;
    }
}
```

- Case 3 Code

```css
@media screen and (min-width: 1024px)
{
    h1, h2, h3, h4, h5, h6
    {
        text-align: initial;
        padding: auto 0 auto 0;
    }
}
```

## Explanation of the HTML and CSS Entities Used

This last part corresponds to the code part of this practical (2. Exercise).

### HTML entities: why have you chosen to use those specific tags?


### The CSS used must be explained. Why have you chosen those selectors and properties?

December 6th, 2022
