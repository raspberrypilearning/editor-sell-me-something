<h2 class="c-project-heading--task">Style the final layout</h2>

--- task ---
Update the page styles so the background and flip cards match the finished YouTube channel design.
--- /task ---

Edit the highlighted parts of `style.css`.

<div class="c-project-code">

--- code ---
---
language: css
filename: style.css
line_numbers: true
line_number_start: 114
line_highlights: 116-119,169-171,176-179,184-188,197-201,212-224,237-283
---
/* Style for ordered and unordered lists */

ol,
ul {
  text-align: left; /* Keep the list aligned neatly inside the wrapper */
  padding-left: 2rem;
}

/* Padding around paragraphs */

p {
  padding: 0.25rem 0.5rem;
}

/* Style for links */

a:link,
a:visited {
  font-weight: bold;
  color: inherit; /* Use the colour of the parent element */
}

.xcenter {
  text-align: center;
}

.ycenter {
  display: flex;
  justify-content: center;
  flex-flow: column;
}

/* Styles just for the .wrap class */

.wrap {
  /* Make content wrap over mutiple rows */
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
}

/* For creating fancy boxes */

.dashed-border {
  border: 0.25rem dashed var(--detail2);
}

.solid-border {
  border: 0.25rem solid var(--detail2);
}

/* Styles for the div tags that are inside a .wrap class */

.wrap > div {
  width: 14rem;
  padding: 0rem; /* Remove extra padding so the cards line up cleanly */
}

/* Styles for the img tags that are inside a .wrap class */

.wrap > img {
  width: 14rem;
  display: block;
  padding: 0rem; /* Keep wrapped images flush with the layout */
}

/* Styles for the p tags that are inside a .wrap class */

.wrap > p,
.wrap > span {
  width: 14rem;
  display: block;
  padding: 0rem; /* Keep text blocks aligned with the cards */
}

/* Specific styles for this project */

.bigfont {
  font-size: 3rem;
}

.hugefont {
  /* Used to make a large emoji */
  font-size: 8rem; /* Make the main emoji extra large */
  text-align: center;
  padding: 1rem;
}

.wrap .narrow {
  width: 10rem;
}

.wrap .wide {
  width: 20rem;
}

blockquote {
  font: var(--quote-font);
  color: var(--ontertiary); /* Use light text on the quote background */
  text-align: center;
  padding: 0.2rem;
  max-width: 25rem;
}

cite {
  color: var(--onprimary); /* Make the quote credit readable */
  background-color: var(--primary);
  font-size: normal;
  padding: 0.2rem;
}

/* Specific styles for this project */

.tile {
  height: 9.4rem;
}

.rounded {
  border-radius: 1rem;
}

.gradient1 {
  background-image: linear-gradient(
    to bottom right,
    #111111,
    #ff0033
  ); /* Create a dark-to-red gradient for the header and cards */
  color: #ffffff;
}

.gradient2 {
  background-image: linear-gradient(
    to bottom right,
    #ff3d00,
    #ffcc00
  ); /* Create a warm orange-to-yellow gradient for the quote and card backs */
  color: #111111;
}

.gradientCP {
  background-image: linear-gradient(
    to bottom right,
    #0a0a0a,
    #1f1f1f,
    #ff0033,
    #0a0a0a,
    #ff3d00,
    #ffffff
  ); /* Add a bold background that suits a video channel */
  color: #ffffff;
}

.shadow {
   box-shadow: 5px 5px 3px 0px #888888; /* right and bottom shadow size, blur, spread and colour */
   /*box-shadow: 5px 5px 4px 2px var(--detail);*/
}

.wrap .card {
  width: 15rem; /* Give each card a fixed size */
  height: 10rem;
  border: 0.1rem solid transparent;
}

.card-content {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 1s; /* Animate the flip effect */
  transform-style: preserve-3d;
  perspective: 60rem;
}

.card:hover .card-content {
  transform: rotateY(180deg); /* Flip the card on hover */
}

.card-face {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden; /* Hide the back until the card flips */
}

.card p {
  padding: 0.5rem;
}
--- /code ---

</div>

--- task ---
**Test:** The page background should look more like a video channel banner, and the flip cards should still work.
--- /task ---
