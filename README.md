# Blog preview card

## Table of contents

- [Overview](#overview)
  - [Screenshot and live site URL](#screenshot-and-live-site-url)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Inspired by](#acknowledgments)

## Overview

### Screenshot and live site URL

| Desktop                                      | Mobile                                      |
| -------------------------------------------- | ------------------------------------------- |
| ![Alt Text](/assets/desktop-screenshot.jpeg) | ![Alt Text](/assets/mobile-screenshot.jpeg) |

[Live Site URL](https://noonpanirsabzi.github.io/blog-preview-card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

The challenge states, "The font sizes in this project are slightly smaller in the mobile layout. Find a way to reduce font size for smaller screens without using media queries." I addressed this issue using the CSS `min()` function. Initially, I had some difficulties understanding the `min()`, `max()`, and `clamp()` functions in CSS and their applications, but I eventually figured it out.

To solve the problem, the key is to establish a relationship between the user's screen size and CSS measurements. For example, consider the following code:

```css
.blog-card {
  width: min(87.2vw, 24rem);
}
```

In this case, the relative unit **vw** (viewport width) increases as the screen size gets larger. However, it reaches a maximum value of 24rem (24 \* 16px = 384px). Beyond this point, the `min()` function selects 24rem, ensuring the element does not exceed this fixed width.

With this approach, we achieved a reponsive mobile-first design. Our _.blog-card_ element maintains an appropriate size on smaller screens. As the screen size increases, it remains at a fixed width that doesn’t need to grow further, preventing unnecessary scaling.

I applied the same technique to font sizes as well. Here's an example:

```css
.figtree-label {
  font-size: clamp(0.75rem, 3.2vw, 0.875rem);
}
```

The `clamp()` function works similarly—allowing the font size to scale with the viewport while keeping it within a reasonable range.

### Useful resources

- [CSS min(), max(), and clamp()](https://web.dev/articles/min-max-clamp)
- [Pseudo classes in CSS like Hover](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
- [Transition attribute](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) - to combine with Hover effect and make it more visually appealing.

## Author

- Github - [@AminForouzan](https://github.com/AminForouzan)
- Frontend Mentor - [@AminForouzan](https://www.frontendmentor.io/profile/AminForouzan)

## Inspired by

- [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS).
