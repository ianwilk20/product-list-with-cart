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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

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

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

I learned the basics of tailwind CSS in this challenge. I never touched it in the past and thought it would be a perfect oppourtinity to learn the basics and see how my development process would benefit or be impaired by it.

I learned what flex-grow, flex-shrink, and flex-basis can do. I'm still not entirely satisfied with my understanding and will continue to look into this. 
  - ```flex-grow: 0``` means the element will not grow to fill available space. It will only take up the space it needs based on its content.
  - ```flex-grow: 1``` means the element can grow to fill available space. If there is extra space in the container, this element will expand to take it up.
  - ```flex-shrink: 0``` prevents a flex item from shrinking when there is not enough space in the flex container.
  - ```flex-shrink: 1``` means the element can shrink if necessary to avoid overflow. If the container is too small to fit all children, this element will shrink proportionally.
  - ```flex-basis: auto``` sets the initial size of the element based on its content or width/height properties.
Where this came up in the project was the Order Confirmed modal. I wanted the order items to take up any remaining space in the modal that wasn't already used by the checkmark, modal title and description, and Start over button. So I set those items to have a ```flex: 0 1 auto```, and the order items ```flex: 1 1 auto```. The challenge was that the Start over button would shrink and I wanted it to stay the height I defined for it of 3rem. The solution was to change the Start over button to have a ```flex-shrink: 0```. I think that means that it won't shrink.

I found a little issue with the increment and decrement pill. Each time I would increment or decrement the quantity of an item, the pill would resize slightly. My huntch was this was happening because the pill would resize to accomodate the changing quantity text. After some research, I learned how to prevent that. By adding a fixed, ex. 0.75rem, to the quantity text the pill no longer resizes when incrementing or decrementing the quantity.

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
