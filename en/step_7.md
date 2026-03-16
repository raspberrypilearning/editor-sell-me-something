<h2 class="c-project-heading--task">Style the final layout</h2>

--- task ---
Update the page styles so the background and flip cards match the finished YouTube channel design and still fit neatly inside the project embed.
--- /task ---

Edit the highlighted parts of `style.css`.

<div class="c-project-code">

--- code ---
---
language: css
filename: style.css
line_numbers: true
line_number_start: 46
line_highlights: 47-56,73-75,170-172,177-180,185-189,205-210,238-277
---
/* The main content of the page between the header and footer */
main {
  background: var(--primary); /* Colour the background */
  color: var(--onprimary); /* Colour the text */
  margin: 0 auto; /* Center if the browser is really wide */
  width: 100%; /* Let the content fill the available space */
  min-width: 0; /* Allow the layout to shrink inside embeds */
  max-width: 70rem; /*  Don't let the content get too wide */
  padding: 0;
  padding-top: 0.5rem; /* Padding at the top */
  margin-bottom: 1em; /* Gap before the footer */
}

/* Section styles */

section {
  padding: 1rem; /* Keep enough space without forcing overflow */
  margin: 1rem auto;
}

/* Styles for the div tags that are inside a .wrap class */

.wrap > div {
  width: min(14rem, 100%); /* Keep wrapped blocks inside narrow embeds */
  padding: 0rem;
}

/* Styles for the img tags that are inside a .wrap class */

.wrap > img {
  width: min(14rem, 100%); /* Let wrapped images shrink on smaller screens */
  display: block;
  padding: 0rem;
}

/* Styles for the p tags that are inside a .wrap class */

.wrap > p,
.wrap > span {
  width: min(14rem, 100%); /* Let text blocks shrink instead of overflowing */
  display: block;
  padding: 0rem;
}

/* Specific styles for this project */

.bigfont {
  font-size: 3rem;
}

.hugefont {
  /* Used to make a large emoji */
  font-size: 8rem;
  text-align: center;
  padding: 1rem;
}

.wrap .narrow {
  width: min(10rem, 100%); /* Keep narrow blocks responsive */
}

.wrap .wide {
  width: min(20rem, 100%); /* Stop the quote block overflowing in embeds */
}

blockquote {
  font: var(--quote-font);
  color: var(--ontertiary);
  text-align: center;
  padding: 0.2rem;
  max-width: 25rem;
}

cite {
  color: var(--onprimary);
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
  width: min(15rem, 100%); /* Keep cards responsive in narrow embeds */
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
**Test:** The page background should look more like a video channel banner, the layout should fit neatly inside the project embed, and the flip cards should still work.
--- /task ---
