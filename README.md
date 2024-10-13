# Frontend Mentor - Product list with cart solution

This is a solution to the [Product list with cart challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-list-with-cart-5MmqLVAp_d). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- Add items to the cart and remove them
- Increase/decrease the number of items in the cart
- See an order confirmation modal when they click "Confirm Order"
- Reset their selections when they click "Start New Order"
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

Desktop:

![Desktop initial state](/design/solution-screenshots/sol-desktop-init.png)

![Desktop items in cart state](/design/solution-screenshots/sol-desktop-cart.png)

![Desktop confirmed order state](/design/solution-screenshots/sol-desktop-confirmed.png)

Tablet:

![Desktop initial state](/design/solution-screenshots/sol-tablet-init.png)

Mobile: 

![Mobile initial state](/design/solution-screenshots/sol-mobile-init.png)

![Mobile items in cart state](/design/solution-screenshots/sol-mobile-cart.png)

![Mobile confirmed order state](/design/solution-screenshots/sol-mobile-init.png)


### Links

- [Solution URL](https://github.com/ianwilk20/product-list-with-cart)
- [Live Site URL](https://product-list-and-cart-ianwilk20.netlify.app/design/)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- CSS Grid
- Mobile-first workflow
- [Tailwind](https://tailwindcss.com/docs) - For styles

### What I learned

I learned the basics of tailwind CSS in this challenge. I never touched it in the past and thought it would be a perfect oppourtinity to learn the basics and see how my development process would benefit or be impaired by it. I found that it saved me lots of time and later maintenance (adjusting existing styles for tablet and desktop) when writing css. On the other hand, there was a learning curve to know the basic utility classes and I found that the time I saved from writing and maintaining css was spend looking up classes in the Tailwind documentation. Likely, the benefit from using Tailwind will appear the more projects I do, but also in the maintainability of the css.

I learned what flex-grow, flex-shrink, and flex-basis can do. I'm still not entirely satisfied with my understanding and will continue to look into this. 
  - ```flex-grow: 0``` means the element will not grow to fill available space. It will only take up the space it needs based on its content.
  - ```flex-grow: 1``` means the element can grow to fill available space. If there is extra space in the container, this element will expand to take it up.
  - ```flex-shrink: 0``` prevents a flex item from shrinking when there is not enough space in the flex container.
  - ```flex-shrink: 1``` means the element can shrink if necessary to avoid overflow. If the container is too small to fit all children, this element will shrink proportionally.
  - ```flex-basis: auto``` sets the initial size of the element based on its content or width/height properties.
Where this came up in the project was the Order Confirmed modal. I wanted the order items to take up any remaining space in the modal that wasn't already used by the checkmark, modal title and description, and Start over button. So I set those items to have a ```flex: 0 1 auto```, and the order items ```flex: 1 1 auto```. The challenge was that the Start over button would shrink and I wanted it to stay the height I defined for it of 3rem. The solution was to change the Start over button to have a ```flex-shrink: 0```. I think that means that it won't shrink.

I found a little issue with the increment and decrement pill. Each time I would increment or decrement the quantity of an item, the pill would resize slightly. My hunch was this was happening because the pill would resize to accomodate the changing quantity text. After some research, I learned how to prevent that. By adding a fixed, ex. 0.75rem, to the quantity text the pill no longer resizes when incrementing or decrementing the quantity.

I learned that if you have images that you want to use for different screen sizes, you can create a ```<picture>``` element and have various ```<source>``` elements with the images that should be shown given certain screen sizes. Example: 

```html
<picture id="item-7-image" class="rounded-lg">
  <!-- Image to display on screens up to 640px wide -->
  <source srcset="./assets/images/image-cake-mobile.jpg" media="(max-width: 640px)">
  
  <!-- Image to display on screens between 641px to 1024px wide  -->
  <source srcset="./assets/images/image-cake-tablet.jpg" media="(max-width: 1024px)">

  <!-- Image to display on screens larger than 1025px  -->
  <source srcset="./assets/images/image-cake-desktop.jpg" media="(min-width: 1025px)">

  <!-- Fallback image  -->
  <img src="./assets/images/image-cake-mobile.jpg" alt="Image of Red Velvet Cake" class="w-full rounded-[inherit]">
</picture>
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

I will continue to learn Tailwind as my first impressions with it were good and I can see the utility that it brings.

I'd be interested in adding TypeScript into my next challenge because I found that I wrote many JavaScript functions that delt with objects in this challenge. If a project grows beyond the scope of this one, I can see type safety being important, especially for preventing bugs.


### Useful resources

- [Understanding flex-grow, flex-shrink, and flex-basis ](https://css-tricks.com/understanding-flex-grow-flex-shrink-and-flex-basis/) - This helped me start to understand flex-grow, flex-shrink, and flex-basis.
- [Tailwind Docs](https://tailwindcss.com/docs) - This is the documentation I used to help kickstart using Tailwind in my challenge.

## Author

- GitHub - [ianwilk20](https://github.com/ianwilk20)