# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Code snippets and acknowledgments](#code-snippets-and-acknowledgments)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the section depending on their device's screen size

### Screenshot

![](./images/social-proof-desktop.png)

### Links

- [Solution URL](https://github.com/codercreative/social-proof-section)
- [Live site URL](https://codercreative.github.io/social-proof-section/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### Code snippets and acknowledgments

I coded most of this project myself, but I was very happy to learn some new tricks via [Kevin Powell's youtube recording](https://youtu.be/K27WULzr2P8) of how he solved this frontendmentor challenge.

In the mobile version, the star rating icons posed a challenge, but Kevin had a cool solution. With below code, I only had to insert the star icon once --- instead of 15 times.

```css
.stars p::before {
  content: "";
  width: 6rem;
  height: 1rem;
  margin: 0 auto;
  display: block;
  background-image: url("../images/icon-star.svg");
  margin-bottom: 0.5rem;
  background-repeat: space;
  margin-bottom: 0.8em;
}
```

Whew, I had a hard time figuring out why I could not place the stars and the rating text next to each other and center align them. Kevin Powell came to the rescue with this line of code:

```css
.stars p::before {
  margin: -0.2rem 0.5rem 0 0;
}
```

Below, Kevin Powell's cool solution for shifting the alignment of the star rating elements as well as the quote elements:

One option for star ratings:

```css
.stars:first-of-type {
  margin-left: 0;
}

.stars:last-of-type {
  margin-right: 0;
}
```

...However, I chose this option for star ratings:

```css
.stars:first-of-type {
  transform: translateX(-2em);
  margin-top: 2em;
}

.stars:last-of-type {
  transform: translateX(2em);
  margin-bottom: 2em;
}
```

Simple and elegant solution to shift the alignment of the quote elements --- once you know how 😁:

```css
.card:nth-child(2) {
  transform: translateY(3em);
}

.card:nth-child(3) {
  transform: translateY(6em);
}
```

One thing I have to ensure in future is that all images show on the live version of the project. I was thrown for a loop with Visual Studio Code as the images showed locally, but not when I uploaded the project to Github. It turned out I had to add ../ to my url. (Thanks to @hyrongennike at Frontendmentor.io for pointing this out)

```css
body {
  background-image: url("../images/icon-star.svg");
}
```

I added the two wave svg images to the background thanks to great help from @correlucas at Frontendmentor.io.

```css
body {
  background-image: url("../images/bg-pattern-top-desktop.svg"),
    url("../images/bg-pattern-bottom-desktop.svg");
  background-position: left -200px top -80px, right -100px bottom -100px;
  background-repeat: no-repeat, no-repeat;
}
```

## Author

- Frontend Mentor - [@codercreative](https://www.frontendmentor.io/profile/codercreative)
