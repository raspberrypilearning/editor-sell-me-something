<h2 class="c-project-heading--task">Refine the animation</h2>

--- task ---
Adjust the animation settings so the channel emoji and link keep moving gently while the cards flip smoothly.
--- /task ---

Edit the animation classes in `animation.css`.

<div class="c-project-code">

--- code ---
---
language: css
filename: animation.css
line_numbers: true
line_number_start: 1
line_highlights: 1-3,17-19,31,38-39,49,52,55,70-76,88-94
---
 .spinme {
  animation: rotate-center linear 8s infinite; /* Keep the channel emoji spinning all the time */
  display: inline-block; /* Important to allow rotation */
}

@keyframes rotate-center {
  /* The spin me animation code */
  0% {
    /* Rotate from 0 to 360 degrees */
    transform: rotate(0);
  }
  100% {
    transform: rotate(360deg);
  }
}

.bounceme {
  animation: bounce ease 2s infinite; /* Keep the channel link bouncing so it stands out */
  display: inline-block;
}

@keyframes bounce {
  /* The bounce animation code */
  0% {
    transform: scale(1, 1) translateY(0); /* Starting position and actual size */
  }
  10% {
    transform: scale(1.1, 0.9) translateY(0); /* Grow width and shrink height for pre bounce squash effect */
  }
  30% {
    transform: scale(1, 1) translateY(-1rem); /* Use a small bounce so the text stays readable */
  }
  50% {
    transform: scale(1, 1) translateY(0); /* Move emoji back to starting position */
  }
}

.scaleme {
  animation: scale ease 2s infinite; /* Keep scaling effects looping smoothly */
  display: inline-block;
}

@keyframes scale {
  /* The twinkle animation code */
  0% {
    transform: scale(1, 1);
  }
  20% {
    transform: scale(1.05, 1.05); /* Make the scale effect more subtle */
  }
  40% {
    transform: scale(1.1, 1.1); /* Peak size for the animation */
  }
  60% {
    transform: scale(1.05, 1.05); /* Shrink back down smoothly */
  }
  80% {
    transform: scale(1, 1);
  }
}

.rollmeleft {
  animation: rollleft ease 8s 1;
  display: inline-block;
}

@keyframes rollleft {
  /* The roll animation code */
  from {
    transform: translate(-60vw) rotate(0deg);
    transform-origin: center; /* Rotate around the middle of the element */
  }

  to {
    transform: translate(0vw) rotate(360deg);
    transform-origin: center;
  }
}

.rollmeright {
  animation: rollright ease 8s 1;
  display: inline-block;
}

@keyframes rollright {
  /* The roll animation code */
  from {
    transform: translate(60vw) rotate(360deg);
    transform-origin: center; /* Rotate around the middle of the element */
  }

  to {
    transform: translate(0vw) rotate(00deg);
    transform-origin: center;
  }
}

.flipme {
  transform: rotateY(180deg);
}
--- /code ---

</div>

--- task ---
**Test:** The emoji should spin continuously, the `Visit the channel` link should keep bouncing, and the flip cards should still work.
--- /task ---
