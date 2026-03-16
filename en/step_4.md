<h2 class="c-project-heading--task">Add a customer quote</h2>

--- task ---
Add a quote section that gives visitors social proof that the channel is worth subscribing to.
--- /task ---

Place the new section after your list in `index.html`.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 52
line_highlights: 54-60
---
      <!-- Add a quote to make the channel feel more convincing -->
      <section class="wrap gradient2">
        <div class="wide">
          <blockquote>The videos are short, clear, and full of ideas I can try straight away on my own channel.</blockquote> <!-- Share feedback from a subscriber -->
          <cite>Mia, Pixel Pulse subscriber</cite> <!-- Credit the quote -->
        </div>
      </section>
--- /code ---

</div>

--- task ---
**Test:** A quote should appear underneath the list section with the subscriber's name shown below it.
--- /task ---
