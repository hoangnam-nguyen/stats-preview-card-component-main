# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62).

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./images/screenshot_desktop.png)
![](./images/screenshot_mobile1.png)
![](./images/screenshot_mobile2.png)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow


### What I learned

- Use rem units instead of px in most cases to facilitate responsive design
- Get used to mobile-first workflow
- Add an image to html as a background-image of a div, then create a pseudo-element to add an additional layer to the image

```css
.image {
    position: relative;
    height: 18.75rem;
    background-size: cover;
    background-image: url('images/image-header-mobile.jpg');
    background-repeat: no-repeat;
    background-position: center;
}

.image::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background: var(--clr-primary-violet);
    mix-blend-mode: soft-light;
}
```

- A simple way to center (horizontally and vertically) a div inside `body` using flexbox:

```css
body {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
}
```

- If there is an image inside a div, setting `overflow: hidden;` makes sure the image will not spill out of the div's area. This is useful for instance when setting `border-radius` for div.

```css
div {
    border-radius: 1rem;
    overflow: hidden;
}
```


### Useful resources

- [CSS Units Best Practice](https://gist.github.com/basham/2175a16ab7c60ce8e001)
- [A Complete Guide of responsive web design using CSS rem and em Units](https://dev.to/romankhan/a-complete-guide-of-responsive-web-design-using-css-rem-and-em-units-4j6k) - These sources helped me realize the need to use rem/em units more than absolute units (like px), as a good practice for professional responsive web design. I really liked this method and will use it going forward.


## Author

- GitHub - [Nguyen Hoang Nam](https://github.com/hoangnam-nguyen)
- Frontend Mentor - [@hoangnam-nguyen](https://www.frontendmentor.io/profile/hoangnam-nguyen)
- CodePen - [@hoangnam-nguyen](https://codepen.io/hoangnam-nguyen)


## Acknowledgments

Many thanks to [@darryncodes](https://www.frontendmentor.io/profile/darryncodes) for his constructive comment in my previous challenge's [solution](https://github.com/hoangnam-nguyen/order-summary-component-main), which has been applied in this very project.


