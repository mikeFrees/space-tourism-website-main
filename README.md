# Frontend Mentor - Space tourism website solution

This is a solution to the [Space tourism website challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/space-tourism-multipage-website-gRWj1URZ3). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout for each of the website's pages depending on their device's screen size
- See hover states for all interactive elements on the page
- View each page and be able to toggle between the tabs to see new information

### Screenshot

![](./screenshot.png)

### Links

- [solution repository](https://github.com/mikeFrees/space-tourism-website-main)
- [live site](https://mikes-space-travel.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- scss
- 7 - 1 file structure scss
- CSS Grid
- postcss

### What I learned

I learned how to use mixins in scss and tried to use it to make my backgrounds change according to the page it is on.
```scss
// Media queries
$desktop: 800px;
$tablet: 600px;
$mobile: 599px;

@media only screen and (max-width: $mobile) {
    @include screenType("mobile");
}

@media only screen and (min-width: $tablet) {
    @include screenType("tablet")
}

@media only screen and (min-width: $desktop) {
    @include screenType("desktop");
}

@mixin screenType($type) {
    body {
        height: 100vh;
        @include mediaBackground("../images/home/background-home-" + $type +".jpg");
        &.Destination {
            @include mediaBackground("../images/destination/background-destination-" + $type + ".jpg");
        }
    
        &.Technology {
            @include mediaBackground("../images/technology/background-technology-" + $type + ".jpg");
        }
    
        &.Crew {
            @include mediaBackground("../images/crew/background-crew-" + $type + ".jpg");
        }
    }
}

@mixin mediaBackground($url) {
    background: center / cover no-repeat url($url);
  }
```

### Continued development

I feel the need to structure my code better. At the beginning everything is clear but as i continue to work on a project my view of the whole gets fuzzy and i sometimes get lost in the whole. I will try to find a workflow to follow and a clear structure for my css in the future(Learn about the BEM architecture for CSS).

I ended this challenge with only the desktop version finished because i spent too long on this project and started to feel like i was stuck in place. I will come back to it later to continue the tablet and phone versions.

I need to try and comment my code more and commit earlier with small adjustments each time.

### Useful resources

- [7-1 pattern for a manageable codebase](https://openclassrooms.com/en/courses/5625786-produce-maintainable-css-with-sass/5723581-use-the-7-1-pattern-for-a-manageable-codebase) - This helped me organize my scss files and improve my file structure. I really liked this organization and will implement it in my starting template for future projects.

## Author

- LinkedIn - [Frees Mike](https://www.linkedin.com/in/mike-frees/)
- Frontend Mentor Profile - [Mike Frees](https://www.frontendmentor.io/profile/mikeFrees)

