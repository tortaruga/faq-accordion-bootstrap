# Frontend Mentor - FAQ accordion solution

This is a solution to the [FAQ accordion challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-wyfFdeBwBz). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)


## Overview

the point of this project was to try and create the accordion with bootstrap this time instead of using js like my previous solution.

I thought it would be fast since most of the work is already taken care of by bootstrap, i forgot to consider that this is my first time using bootstrap, so it ended up being not as fast as anticipated.

if anything i was almost faster last time handling the js myself...

the accordion component wasn't too hard to get working, but it took a while to get the styling to do what i wanted, but i am pleased with the result. 

### The challenge

Users should be able to:

- Hide/Show the answer to a question when the question is clicked
- Navigate the questions and hide/show answers using keyboard navigation alone
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/faq-accordion-with-bootstrap-uYl0h6BO5R](https://www.frontendmentor.io/solutions/faq-accordion-with-bootstrap-uYl0h6BO5R)
- Live Site URL: [https://tortaruga.github.io/faq-accordion-bootstrap/](https://tortaruga.github.io/faq-accordion-bootstrap/)

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Bootstrap

### What I learned

to create an accordion with bootstrap you should have a container with the class of .accordion, and as many .accordion-item as needed.

each .accordion-item should have an .accordion-header with an id, and an .accordion-button which should also have a class of .collapsed if it should be closed by default.

the .accordion-button should have a data-bs-target of the id of the corresponding collapsible content, data-bs-toggle of collapse, and aria-expanded of false if it's collapsed by default, true otherwise.

it should also have aria-controls equal to the element it controls, which is the collapsible content.

to create this collapsible content, you use the classes .accordion-collapse and .collapse, a unique id, and aria-labelledby equal to the id of the .accordion-header.

to make it so that expanding one item closes all the others all the .accordion-collapse should have the same data-bs-parent, which is equal to the id of the whole accordion container.

to change the default arrows: 

```
.accordion-button::after {   
    display: none;      
}

.accordion-button { 
    background-image: url('./assets/images/icon-plus.svg'); 
    background-repeat: no-repeat; 
    background-position: 100%;  
    background-size: 1em; 
}

.accordion-button:not(.collapsed) { 
    background-image: url('./assets/images/icon-minus.svg'); 
    background-color: transparent;  //to remove the blue color 
}  

```

and then i spent fifteen hours trying to remove the border separating the button from the content when you open the answer, and it turns out it was a shadow instead.

```
.accordion-button:not(.collapsed) {
    border: none; 
    outline: none;
    box-shadow: none; 
}  
```

### Continued development

i'll continue to practice bootstrap

### Useful resources

- [Bootstrap docs](https://getbootstrap.com/docs/5.0/components/accordion/) - This helped with the accordion

## Author

- Frontend Mentor - [@tortaruga](https://www.frontendmentor.io/profile/tortaruga)

