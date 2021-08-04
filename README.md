# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
- [Author](#Author)

## Overview

This was a basic card that was put forward by the frontend mentor as a challenge and the experience of making it was very thrilling and enjoyable as I learned a whole lot using this project.

### The challenge

The challenge required me to produce the card in the preview with the following requirements. i.e.

Users should be able to:

- View the optimal layout depending on their device's screen size
- Adjust the items and also manage not to break any of them.

## Screenshots of my implementaion

### Desktop-Screenshot

![desktop-screenshot](/images/desktop-screenshot.png)

### Mobile-Screenshot

![mobile-screenshot](/images/mobile-screenshot.png)

### Links

- Solution URL: [My-solution](https://www.frontendmentor.io/solutions/statpreview-card-using-htmlcss-only-vu1DsgHf_)
- Live Site URL: [Solution-site](https://stat-preview-card-prakhar-dev.netlify.app/)

## My process

I started by laying out the structure of the challenge for the desktop interface then I followed step-by-step CSS by previewing the designs by opening them in my preview of the browser or you can paste them in figma to watch all of them at the same moment this makes the working easy , while coding. After wards I wrote some media queries which were quite repetitive to the code written for the desktop just written explicitly for different class otherwise inside code was pretty much the same.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Media-queries
- Mobile-first workflow

### What I learned

- How the flex-box works

The following is the stat-bar i built using flexbox which contained ul elements which in-turn contain two elements stat-bar-stat (example:10k+) and stat-bar-heading(example:companies). Using flex-box i was at ease arranging them in rows and column using just CSS for both desktop and mobile environment using properties shown below in CSS code.

```html
<div class="stat-bar">
 <ul>
  <li class="stat-bar-stat">10k+</li>
  <li class="stat-bar-heading">Companies</li>
 </ul>
 <ul>
<li class="stat-bar-stat">314</li>
<li class="stat-bar-heading">Templates</li>
</ul>
<ul>
<li class="stat-bar-stat">12M+</li>
<li class="stat-bar-heading">queries</li>
</ul>
</div>
```

```CSS
/* For desktop CSS of flex box: */
.stat-bar {
display: flex;
flex-direction: row;
}
.stat-bar ul {
list-style: none;
margin-right: 30px;
}

.stat-bar .stat-bar-stat {
color: hsl(0, 0%, 100%);
font-weight: 700;
font-size: large;
margin-bottom: 2px;
}
.stat-bar .stat-bar-heading {
color: hsla(0, 0%, 100%, 0.75);
text-transform: uppercase;
font-size: smaller;
}

/* For mobile the following media query was written */
@media(max-width:480px)
{
.stat-bar {
display: flex;
flex-direction: column;
margin-left: 10px;
}
.stat-bar .stat-bar-heading {
margin-bottom: 12px;
}
}
```

- The overlay over the image.
 I took the inspiration from the stackoverflow post that i would link in the resources.
 Also I used the filter property of the CSS to increase the contrast as due to overlay the image was a little bit dull.
 You can refer to my code below.

 ```Html
 <!-- For mobile -->
 <div class="card-image-mobile">
<div class="overlay-mobile"></div>
</div>

<!-- For desktop -->
<div class="card-image">
<div class="overlay"></div>
</div>
```

```CSS
/* For the desktop interface */
.card-image {
background: url(/images/image-header-desktop.jpg);
background-position: center center;
background-size: cover;
width: 100%;
position: relative;
border-radius: inherit;
border-top-left-radius: 0;
border-bottom-left-radius: 0;
filter: contrast(150%);
}

.overlay {
position: absolute;
top: 0;
bottom: 0;
right: 0;
left: 0;
border-radius: inherit;
border-top-left-radius: 0;
border-bottom-left-radius: 0;
background-color: hsl(277, 64%, 61%);
opacity: 0.5;
}
/* For mobile interface */
.card-image-mobile {
  background: url(/images/image-header-mobile.jpg);
  background-position: center center;
  background-size: cover;
  padding: 120px;
  position: relative;
  border-radius: inherit;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  filter: contrast(150%);
}
.card-image-mobile .overlay-mobile {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  border-radius: inherit;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
  background-color: hsl(277, 64%, 61%);
  opacity: 0.5;
}
```

### Continued development

I am still not comfortable with:

- The accessibility issues of the site.
- Centring the content appropriately with different sizes of screen.

- Also the background images should be set properly and the images should not overflow.

### Useful resources

- [Flexbox-guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - This helped me for the flex-box implementation.
 I really liked how they have explained everything so beautifully and appropriately.

-[Overlay-method](https://stackoverflow.com/questions/9182978/semi-transparent-color-layer-over-background-image)-This helped me to lay an overlay over the image.

-[Idea-for-filter](https://www.tutorialspoint.com/adjusting-the-image-contrast-using-css3) -This helped me to adjust the contrast of the image.

## Author

- Website - [Prakhar Garg](https://github.com/Prakhargarg-2010196)
- Frontend Mentor - [@Prakhargarg-2010196](https://www.frontendmentor.io/profile/Prakhargarg-2010196)
