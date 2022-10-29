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
<!-- Created: 2022/10/29 11:53:10 by aperez-b                       +@@@%@   -->
<!-- Updated: 2022/10/29 17:36:31 by aperez-b                                -->
<!--                                                                         -->
<!-- *********************************************************************** -->

# Part 1. Exercises

### Table of Contents

- [Exercise 1](#exercise-1)
- [Exercise 2](#exercise-2)
- [Exercise 3](#exercise-3)
- [Exercise 4](#exercise-4)
- [Exercise 5](#exercise-5)

## Exercise 1

**Statement**

Give the necessary code to include the following image [https://www.publicdomainpictures.net/pictures/120000/velka/musiker-am-strand-von-havanna.jpg](https://www.publicdomainpictures.net/pictures/120000/velka/musiker-am-strand-von-havanna.jpg) with all necessary attributes. The image will be displayed with a width of ``400px`` and the proportional height. These measurements must be indicated in a CSS file. The title of the image and the caption is ``Musicians Caribbean Beach``. In addition, the image must be linked in such a way that the original image is opened when clicking on it. You can use codepen or another editor indicating the link where you have solved the question. It is not necessary to include the HTML headers.

**Answer** \*


```HTML
<!-- HTML Code -->

<!-- Link css file -->
<link rel="stylesheet" href="./style.css"/>

<!-- Insert image -->
<figure>
    <a target="_blank"
    href="https://www.publicdomainpictures.net/pictures/120000/velka/musiker-am-strand-von-havanna.jpg">
    <img class="music"
    alt="Musiker am Strand von Havanna"
    title="Musicians Caribbean Beach"
    src="https://www.publicdomainpictures.net/pictures/120000/velka/musiker-am-strand-von-havanna.jpg">
    </a>
    <figcaption>Musicians Caribbean Beach</figcaption>
</figure>
```
```CSS

/* CSS Code */
html
{
    background-color: black;
}

.music
{
    width: 400px;
    display: block;
    margin: auto;
}
```
\* Coded and tested locally (using vim and a web browser), without any websites.

## Exercise 2

### Statement

Explain, in your own words, the difference between the em, pixel, and rem units applied to text with the CSS font-size property.

### Answer

When setting the font size, we can use many numbering formats. The simplest one is specifying the size of a text element in **pixels** (e.g. 12px). This applies the specific size to font sizes inside the css ruleset, ignoring parent font sizes. The **em** unit specifies the font size in relation to the parent font size. This is useful to inherit the previous font size thanks to CSS' cascading property. Lastly, the **rem** unit is very similar to the **em** one, but the font size is related to the root font size, i.e., the font size defined by default or manually for the general document. For example, if our base size is ``12px`` and we set a specific header to use ``2rem``, then our header will be of size ``24px``.


## Exercise 3

### Statement

Generate the necessary HTML and CSS code to create the lists that are shown below:

![Sample List - Exercise 3](https://user-images.githubusercontent.com/40824677/198830060-5ad11e8d-c311-4f35-9a59-b0c1b2e4bb80.jpeg)

### Answer \*


```HTML
<!-- HTML Code -->

<!-- Link css file -->
<link rel="stylesheet" href="./style.css"/>

<!-- Add nested lists -->
<ul>
    <li>list a1</li>
    <li>list a2</li>
    <ol>
        <li>list b1</li>
        <ul>
            <li>list c1</li>
            <li>list c2</li>
            <li>list c3</li>
            <li>list c4</li>
        </ul>
        <li>list b2</li>
        <li>list b3</li>
        <li>list b4</li>
    </ol>
    <li>list a3</li>
    <li>list a4</li>
</ul>
```

```CSS
/* CSS Code */
ul + ol + ul
{
    list-style-type: square;
}
```
\* Coded and tested locally (using vim and a web browser), without any websites.

## Exercise 4

### Statement

Explain the difference between block elements and inline elements. Describe the following HTML elements and specify whether they are block or inline: ``footer``, ``time``, ``figure``, ``img``, ``a``, ``nav`` and ``address``.

### Answer

**Block vs inline elements**: as the name suggests, ``block-level`` elements form a distinct block on the page, separating itself from other elements on the page with a gap. These block elements can be used to organize the layout of the page, through paragraphs, menus, or media insertation. On the contrary, ``inline-level`` elements are ususally used to add a certain value inside a block-level element. For example, writing a part of a paragraph in bold, or adding a link to a word to act as a clickable link.

- **footer**: ``(block)`` Adds footer information for a page, typically includes the author details and contact, related reources, or copyright information, among other things.
- **time**: ``(inline)`` Used to define timestamps and dates, though modern browsers do not show any visual queues when used. More for indexing purposes than anything.
- **figure**: ``(block)`` Separates content to show a graphic (image, diagram, etc), with the possibility to add captions. As the *W3* notes on their documentation, this element stores self-contained content in it.
- **img**: ``(inline)`` Embeds an image to the document.
- **a**: ``(inline)`` Defines a link to some other resource local or online from other content (text, images, etc).
- **nav**: ``(block)`` Creates links used mainly for navigation. Used to link the various menus on a site.
- **address**: ``(block)`` Adds information about a person including contact information (email, personal URL, phone number, social media, and even the actual address).

## Exercise 5

### Statement

Explain, in your own words, what abbreviated properties in CSS are, what properties allow that, and give an example with each of those properties of how it would be abbreviated and unabbreviated.

### Answer

In CSS there are some rules that refer to the same property, but various specific aspects about it. Let us consider the example of the abbreviation/shorthand property of ``background``. There are several properties to set regarding the background, namely the background ``color``, background ``image``, background ``repeat`` and the background ``position``. Here is what each of these represent about the background:

- **color**: Specify a color code or name to use as background.
- **image**: Use a link to an image as the background.
- **repeat**: Boolean to check if the background image should be 'repeated' (added multiple times until the whole background is full).
- **position**: Location on the screen where the background should be located.

The idea behind these ``shorthand properties`` is to shorten the way to specify all the attributes related to the same property (in our example, the ``background``). Thus, there are two ways to specify the smae background and properties, either by writing all of them in one line or by specifying the different properties individually, as follows:

```css

/* Example of background property in individual properties */
html
{
    background-image: url(./background.jpg);
    background-repeat: repeat-x;
    background-position: center;
}

/* Example of background property in a single line */
html
{
    background: url(./background.jpg) repeat-x center;
}
```
