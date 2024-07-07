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
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![screenshot](./screenshot.jpeg)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/product-preview-card-component-using-media-and-flexbox-i_RY_6UdEr](https://www.frontendmentor.io/solutions/product-preview-card-component-using-media-and-flexbox-i_RY_6UdEr)
- Live Site URL: [https://ryan-ohanlon.github.io/product-preview-card-component-main/](https://ryan-ohanlon.github.io/product-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

This challenge taught me how CSS determines priority and how important developing CSS rules are when having to create a view for desktop and mobile devices.

The primary challenge I had with this challenge was that I had to create two sets of CSS rules where the product page displayed a look for desktop viewers and a different layout for mobile devices. The first hurdle was coming up with a solution for each product image to only be visible for their respective resolution.

The solution I settled on took multiple CSS rules. I had to assign both images a CSS class and set the display to none. Then, using the @media CSS rule to set each image to be visible using the display attribute and the block property if it was for desktop or mobile view. Using min-width and max-width at 376px set the breaking point for desktop or mobile view.

The amount of rules needed for this challenge due to how each product page looked between mobile and desktop and understanding CSS inheritance made this a good starting point for understanding responsive web design where a single CSS file can make a single webpage look completely different based on the device.

```css
/*Disables desktop and mobile image for @media CSS rule*/
.desktop, .mobile {
    display: none;
    max-width: 100%;
}
/*Mobile layout*/
@media (max-width: 376px){
    main{
        display: flex;
        flex-direction: column;
    }
    .mobile{
        display: block;
        border-radius: 1em 1em 0em 0em;
    }
    .desktop {
        display: none;
    }
}
@media (min-width: 376px){
    body{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }
    main{
        display: flex;
        flex-direction: row;
        justify-content: center;
        width: 600px;
        height: 450px;
    }
    .desktop{
        display: block;
        border-radius: 1em 0em 0em 1em;
        width: 50%;
        height: auto;
    }
    .mobile{
        display: none;
    }
}
```

### Continued development

If there still is something I need to continue developing is understanding how to make the elements of a webpage responsive.

While I have developed a better understading the basics of flexbox, I still wasn't able to make every HTML element responsive on the desktop when the device resolution scales up and down trying to exactly match the design-preview specs.

I also still need to learn more about the priority of CSS rules and what the best practices when you need to make multiple CSS files as I originally intended to use a framework but the project design did not offer the solution in the class rules set in the framework. I still needed to create a CSS file of my own so I abandoned the framework for custom CSS rules.

### Useful resources

- [Web.dev](https://web.dev/learn/css/) - Webdev helped me understand the CSS layouts of flexbox.
- [W3Schools](https://www.w3schools.com/css/default.asp) - W3Schools was my resource on how to use the @media CSS rule and how to have image elements appear and not appear based on the resolution of the device.

## Author

- Website - [Ryan O'Hanlon](https://ryan-ohanlon.github.io/)
- Frontend Mentor - [@Ryan-OHanlon](https://www.frontendmentor.io/profile/Ryan-OHanlon)
- Twitter - [@RyanROHanlon](https://x.com/RyanROHanlon)
