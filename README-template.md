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
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://bento-grid-mu-taupe.vercel.app/](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow
- [Google Fonts](https://fonts.google.com/specimen/DM+Sans) - DM Sans

### What I learned

This challenge was a great opportunity to practice `grid-template-areas` for a non-uniform bento-style layout. Instead of adding extra wrapper `<div>`s, I mapped each card to a named grid area using `nth-child` selectors on the existing `<article>` elements, which kept the HTML clean while giving full control over placement on desktop:

```css
.bento-grid {
  grid-template-columns: repeat(4, 1fr);
  grid-template-areas:
    "create social  social  schedule"
    "create manage  maintain schedule"
    "write  percent grow    grow";
}

.bento-grid > article:nth-child(1) { grid-area: create; }
```

On mobile, the grid collapses back to a single column, and the two components that sit in the left column on desktop move to the bottom of the page — a good reminder that grid placement is independent from source order.

### Continued development

- Fine-tune spacing and font sizes to match the design more precisely at in-between breakpoints (e.g. tablet).
- Add the illustrations/icons and star-rating graphic that appear in the full design.
- Practice building the same layout with CSS Grid subgrid once browser support is more consistent.

## Author

- Frontend Mentor - [@wambuimuriu](https://www.frontendmentor.io/profile/wambuimuriu)
- GitHub - [Hannah Wambui](https://github.com/wambuimuriu)