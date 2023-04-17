# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)


**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./my-output/Screenshot%202023-04-17%20110639.png)

### Links

- Video URL: [Add live site URL here](https://nimb.ws/qD3Fik)

## My process
The purpose of creating this page is to enhance my skills in SASS. My approach to achieving this was to begin by obtaining resources from the frontend mentor website and opening the files in VSCode. Subsequently, I installed the required tools such as SASS, prettier, and stylelint to streamline the coding process. Initially, I started by developing the index.html page and subsequently implemented styling using SASS, following the ITCSS architecture and adhering to the BEM class naming convention. In order to ensure that the page is visually appealing and functional, I referenced prototype and design resources and made it responsive. Although the file structure wasn't ideal at first, I was able to optimize it as I learned best practices and improve it until it reached its current state.

### Built with

- CSS
- Flexbox
- ITCSS Architecture
- [SASS](https://sass-lang.com/) - Styling
- [BEM Methodology](https://en.bem.info/methodology/) - Naming convention
- [Stylelint](https://stylelint.io/) - For linting
- [Prettier](https://prettier.io/) - For code formatting


### What I learned

These are what I learned while making this page:
1. The importance of continually seeking opportunities to learn and enhance your skills.
2. The process of building a web page using SASS and various code formatting tools.
3. The significance of adhering to best practices such as using the ITCSS architecture and the BEM class naming convention.
4. The importance of designing based on prototype and design resources and making the page responsive.
5. The value of continuously optimizing the file structure and following good practices to improve the codebase over time.


```html
<div class="container__box container__box--orange">
  <img class="container__image" src="images/icon-sedans.svg" />
  <h1>SEDANS</h1>
  <p>
    Choose a sedan for its affordability and excellent fuel economy. Ideal
    for cruising in the city or on your next road trip.
  </p>
  <button class="container__button">Learn More</button>
</div>
```

```scss
@mixin box-color($primary-color, $secondary-color){
.container__box--#{$primary-color} {
  background-color: map-get(variables.$color, #{$primary-color});

  .container__button {
    color: map-get(variables.$color, #{$primary-color});

    &:hover {
     @include box-shadow(2px, map-get(variables.$color, #{$secondary-color}));

     color: map-get(variables.$color, #{$secondary-color}); 
     background-color: map-get(variables.$color, #{$primary-color});
    }
  }
}
}
```

```css
.container__box--orange .container__button:hover {
  box-shadow: inset 0 0 0 2px hsl(0deg 0% 100% / 75%);
  box-shadow: inset 0 0 0 2px hsl(0deg 0% 100% / 75%);
  color: hsl(0deg 0% 100% / 75%);
  background-color: hsl(31deg 77% 52%);
}
```

### Useful resources

- [Sass YouTube Tutorial By FreeCodeCamp](https://www.youtube.com/watch?v=_a5j7KoflTs&list=PLLah4xHYIASBG7GCKZa12md4exHNf2kQY&index=12&t=1414s) - This helped me learning the basics and features of SCSS. Really thankful for this!
- [Google Fonts](https://fonts.google.com/) - This helped me downloading my desired fonts.
- [Font Squirrel](https://www.fontsquirrel.com/) - This helped me converting font file format. Will definitely use this in the future.


