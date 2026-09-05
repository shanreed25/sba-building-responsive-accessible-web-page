# Building a Responsive and Accessible Web Page
> Demonstrate the ability to create a well-structured, responsive, and accessible web page using the HTML and CSS techniques. Assessed on the use of semantic HTML, CSS layout techniques (including Flexbox and Grid), and the implementation of accessibility features.


**Design and develop a responsive, multi-section webpage for a fictitious company called Accessible Design Co..**

## Features
- Semantic HTML Structure
- Responsive Design Using Flexbox and Grid
    - mobile first starting at 375px
    - header uses flexbox
    - skip link first in the page
- Accessibility Features
    - skip link first in the page
    - `tabindex="-1"` used to make`<main>` is foucusable, but not in the tab order
    - `aria-expanded, aria-label, aria-controls` for hambuger menu 
    - using `role="list"` because I am using `list-style: none` which make some browsers strip list semantic
- Color Contrast and Visual Design

## Reflection Questions

### What accessibility challenges did you face, and how did you address them?
> When trying to implement to skip link feature, I tried to use `display: none` and `visibility: hidden` but they both removed the element from the tab order, so I used `translateY(-100%)` instead

### How did you ensure that your design was responsive and accessible to all users?
- Used mobile-first and let the content decide most breakpoints and added complexity as the viewport grew. 
- The base styles are a single column
- About section rearranges through named grid areas so the image moves beside the text
- The Services grid uses `repeat(auto-fit, minmax(240px, 1fr))` so the cards reflow on their own
- Used semantic landmarks `header, nav, main, footer` 
- Gave each section an `aria-labelledby` and pointed it at the heading, this way the landmarks are announced with meaningful names
- Added a skip link that stays hidden until it receives focus, for keyboard users
- The contact form was were most of the accessibility work happen


### What tools or resources did you find most helpful during this project?
- [CSS Grid Template Areas & grid-area Property explained!](https://www.youtube.com/watch?v=u052g8Yt2l0&t=9s)


## How to view
> Clone the repository and open `index.html` in any browser. 