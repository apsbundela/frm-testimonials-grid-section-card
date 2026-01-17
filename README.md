# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![Desktop](./design/Final-Desktop-Design.png)
![Mobile](./design/mobile-design.jpg)

### Links

- Solution URL: (https://github.com/apsbundela/frm-testimonials-grid-section-card)
- Live Site URL: (https://apsbundela.github.io/frm-testimonials-grid-section-card/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

#### Centering the grid container

- Initially, the testimonial grid was taking the full screen width on desktop.
- I learned that to center a grid layout properly, it is important to give the grid container a `max-width` so it knows when to stop growing.
- Without a `max-width`, the container naturally expands to fill the entire viewport.
- I learned that using `margin-left: auto` and `margin-right: auto` centers a block-level element horizontally.
- I also learned that `margin-inline: auto` is a cleaner and more modern alternative for horizontal centering.

#### Understanding vertical scrolling and card height

- At first, I assumed the cards were growing vertically due to a grid or layout issue.
- I learned that the real cause was typography, not CSS Grid.
- Larger `font-size`, improper `line-height`, and excessive `padding` were increasing the card height.
- After adjusting these typography values, the cards matched the design proportions more closely.
- I also learned that vertical scrolling is content-driven and is completely normal, especially on smaller viewport heights.




#### How to make background image below content (::before Pesudo class)
- Using :: before element created background Image
- Faced challenge how to make image down and card content above - Then selected all card direct child using > * selector and set zindex more than Quattion image

#### :: Before Peudo element 
- ::before creates a pseudo-element that is the first child of the selected element. 
- It is often used to add cosmetic content to an element with the content property. 
- It is inline by default.
- They have no default size, you will have to provide height - width to see on screen.


#### CSS Selector: `.daniel-card > *`

```css
.daniel-card > * {
  position: relative;
  z-index: 1;
}

- **`.daniel-card`** → targets the parent element with this class.  
- **`>`** → selects **only direct children** of `.daniel-card`.  
- **`*`** → selects **all elements** (any tag).  

**Effect:** All direct children of `.daniel-card` get `position: relative;` and `z-index: 1`.  
