# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

![Screenshot of completed design at a screen width of 1440px](./design/Screenshot%20Completed%20Frontend%20Mentor%20Bento%20grid.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- SASS styling and variables

### What I learned

I learned how to set up a bento grid using CSS Grid with grid-template-areas to define the layout of the divs as desired. I initially set up the grid to be 12x10 grids with each grid being 1fr wide and 1fr high. This, however, caused me problems when changing the size of the browser off of the desired 1440px and 375px. Instead, I used SASS variables to size the grid widths and heights according to the width of the grid, which in turn was also set to be reactive.

```css
$page-width: min(97vw, 100vh);
$grid-gap: 1.2vw;
$grid-padding: 1vw;
$grid-size-w : calc(($page-width - $grid-gap*11 - $grid-padding*2) / 12);
$grid-size-h : calc(($page-width - $grid-gap*12 - $grid-padding*2) / 10);
```
I initially had the grid-size-h variable to subtract only $grid-gap*9 instead of $grid-gap*12, since there are only 10 rows and thus 9 gaps between them, but the divs ended up being too long for the design, so I changed it to make the divs a bit shorter. 

I also initially used px to define the padding and margins within the divs, but later changed it to % to make it more reactive. Alongside this, I changed the measurements of the font sizes and the letter-spacing to use rem. I then added a few more media queries at 650px, 600px, 500px, and 250px where I just changed the font-size in html to be smaller, which caused the text in all the divs to scale to a better size. Even though the project was designed only for the two screen widths, I found it to be good practice to make sure that other sizes still looked presentable, even if not exactly like the desired design.

### Continued development

I want to continue to learn ways to make projects more reactive without over-defining the variables in css or setting up too many media queries.

I also want to learn more about accessibility. I didn't focus on how accessible a project like this would be for screen readers, so I would like to come back to it at some point and see what needs to be changed to make it more accessible.

### Useful resources

- [How to Use Bento Grids Design in Your Web Projects](https://www.freecodecamp.org/news/bento-grids-in-web-design/) - This helped me understand how to use CSS Grid to set up a bento grid design.

## Author

- Frontend Mentor - [@Ankia-Fuls](https://www.frontendmentor.io/profile/Ankia-Fuls)
- GitHub - [@Ankia-Fuls](https://github.com/Ankia-Fuls)

