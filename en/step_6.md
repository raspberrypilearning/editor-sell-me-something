<h2 class="c-project-heading--task">Add YouTube flip cards</h2>

--- task ---
Add two flip cards that reveal highlights from your YouTube channel when the visitor hovers over them.
--- /task ---

Place this section after the quote section in `index.html`.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 63
line_highlights: 65-91
---
      <!-- Add two cards that will flip when the user hovers over them -->
      <section class="wrap">
        <div class="card">
          <div class="card-content">
            <div class="card-face ycenter rounded gradient1 shadow">
              <h2>Fresh videos every week</h2>
              <p class="bigfont">▶️</p> <!-- Front of the first card -->
            </div>
            <div class="card-face ycenter rounded flipme gradient2 shadow">
              <p class="bigfont">📅</p>
              <p>NEW UPLOADS EVERY FRIDAY</p> <!-- Back of the first card -->
            </div>
          </div>
        </div>

        <div class="card">
          <div class="card-content">
            <div class="card-face ycenter rounded gradient2 shadow">
              <h2>More than just tutorials</h2>
              <p class="bigfont">🔔</p> <!-- Front of the second card -->
            </div>
            <div class="card-face ycenter rounded flipme gradient1 shadow">
              <p class="bigfont">🎥</p>
              <p>SHORTS, LIVESTREAMS, AND CHALLENGES</p> <!-- Back of the second card -->
            </div>
          </div>
        </div>
      </section>
--- /code ---

</div>

--- task ---
**Test:** Two new cards should appear under the quote, and each one should show a different channel message when you hover over it.
--- /task ---
