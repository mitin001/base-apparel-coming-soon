# Frontend Mentor - Base Apparel coming soon page solution

This is a solution to the [Base Apparel coming soon page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/base-apparel-coming-soon-page-5d46b47f8db8a7063f9331a0). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty
  - The email address is not formatted correctly

### Screenshot

![](./screenshot.jpg)

### Links

[Live Site URL](https://mitin001.github.io/base-apparel-coming-soon/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [Google Fonts](https://fonts.google.com/selection/embed)

### What I learned

Client-side form validation can be done without any JavaScript:

```html
<input placeholder="Email Address" pattern="^\S+@\S+\.\S+$"/>
```

Here, the browser uses the regex [pattern](https://stackoverflow.com/a/201447/7249166) on the input element here to check if the entered email address is valid.

When the input is invalid (does not match the pattern), the browser assigns the invalid pseudo-class to it, which can be used to notify the user of the input error:

```css
input:invalid { border: 2px solid red; }
```

If the user enters an invalid string into the input element, this CSS rule instructs the browser to draw a thick (2px) red border around it. The `:invalid` [pseudo-class](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation) assigned by the browser is used to target the element in the CSS selector.

Flexibility of CSS selectors allows us to avoid much scripting. For example, the heading "We're coming soon" in the [screenshot](#screenshot) is a single HTML element. The striking difference in the first line of this heading was accomplished by targeting the `::first-line` pseudo-element:

```css
h1::first-line { font-weight: 300; color: red; }
```

Different lines within the same element can have different styles thanks to pseudo-elements.

### Continued development

There is no dynamic content on this page, so no JavaScript was required. However, JavaScript will be useful once the form starts sending data to an external API.

### Useful resources

- [Mozilla Developer Network](https://developer.mozilla.org/) - Guidance on HTML elements and attributes, CSS selectors, etc. Especially useful for explaining [client-side form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation).
- [W3Schools](https://www.w3schools.com/) - Alternative resource for guidance on HTML and CSS. Especially useful for explaining [CSS variables](https://www.w3schools.com/css/css3_variables.asp).

## Author

- Frontend Mentor - [@mitin001](https://www.frontendmentor.io/profile/mitin001)
- LinkedIn - [Andrey Mitin](https://www.linkedin.com/in/andrey-mitin-13824a8a)

## Acknowledgments

This challenge was assigned to me as part of the Discussion Assignment for Unit 5 in [MSIT 5250-01 Foundations of Software Engineering](https://catalog.uopeople.edu/graduate-catalog-t1/graduate-program-of-study/the-curriculum-3) (AY2024-T4) at the University of the People.
