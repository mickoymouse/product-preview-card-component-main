# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./design/desktop-preview.jpg)

### Links

- Solution URL: [FEM Solution - Product Overview](https://www.frontendmentor.io/solutions/product-preview-card-w-pseudo-elements-data-attributes-and-more-ffn9TTxcoh)
- Live Site URL: [FEM - Product Overview](https://product-preview-card-component-main-kappa-smoky.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- Data Attributes
- Pseudo Elements
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

I was able to apply what I learn about picture.

```html
<picture>
	<source
		media="(min-width: 768px)"
		srcset="/images/image-product-desktop.jpg"
	/>
	<img
		src="/images/image-product-mobile.jpg"
		alt="Chanel perfume laid out in a table with leaves besides it."
	/>
</picture>
```

I also learned how to use data attributes to add an icon to a button. This approach is also useful as you can dynamically change the icon by changing the data attribute. As long as you support it on the css of couse.

```html
<button class="button" data-icon="cart">Add to Cart</button>
```

```css
.button[data-icon="cart"]::before {
	content: "";
	background-image: url("/images/icon-cart.svg");
	width: 15px;
	height: 16px;
}
```

Additionally I applied something I came across while searching css tricks and what not which is related to screen readers. With the following code any element will be not visible on the screen but will be read by screen readers.

```css
.sr-only:not(:focus):not(:active) {
	clip: rect(0 0 0 0);
	clip-path: inset(50%);
	height: 1px;
	overflow: hidden;
	position: absolute;
	white-space: nowrap;
	width: 1px;
}
```

I was also able to explore how I can dynamically change some sizes you media queries and some css variables.

```css
@media screen and (min-width: 768px) {
	.card {
		--_padding: 2rem;
		grid-template-columns: 1fr 1fr;
	}
}
```

### Useful resources

- [Picture element](https://web.dev/learn/design/picture-element) - This is an article linked by Frontend Mentor which helped me understand how to use picture and data attributes. I'd recommend it to anyone still learning this concept.
- [For SR contents](https://css-tricks.com/inclusively-hidden/) - This is a csss trick article that helped me understand how to hide elements from the screen but still have them read by screen readers.

## Author

- Frontend Mentor - [@mickoymouse](https://www.frontendmentor.io/profile/mickoymouse)
