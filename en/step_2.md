<h2 class="c-project-heading--task">Add the page title</h2>

--- task ---
Update the placeholder text so visitors immediately know that your page is promoting a YouTube channel.
--- /task ---

Edit the title, heading, and footer area in `index.html`.

<div class="c-project-code">

--- code ---
---
language: html
filename: index.html
line_numbers: true
line_number_start: 1
line_highlights: 9,26,28-29,40-41
---
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />

    <!-- Title shown in web browsers-->
    <title>Pixel Pulse Channel</title> <!-- Show the channel name in the browser tab -->

    <!-- Import fonts from Google -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Bungee+Shade&family=Codystar:wght@300&family=Creepster&family=Eater&family=Faster+One&family=Finger+Paint&family=Flavors&family=Freckle+Face&family=Fredericka+the+Great&family=Gorditas&family=Hanalei+Fill&family=Lobster&family=Luckiest+Guy&family=Miltonian&family=Monoton&family=Ranchers&family=Rubik+Moonrocks&family=Shrikhand&family=Spirax&family=Titan+One&Bebas+Neue&Cairo&display=swap"
      rel="stylesheet"
    />

    <!-- Include CSS style file -->

     <link href="style.css" rel="stylesheet" type="text/css" />
     <link href="animation.css" rel="stylesheet" type="text/css" />
     <link href="default.css" rel="stylesheet" type="text/css" />
  </head>

  <body class="gradientCP"> <!-- Add a class so you can style the whole page background later -->
    <!-- The page header code goes here -->
    <header class="gradient1 border-bottom"> <!-- Use a stronger header style -->
      <h1>Subscribe to Pixel Pulse</h1> <!-- Tell visitors what action you want them to take -->
    </header>

    <!-- The main content for the web page goes between the main tags -->
    <main>
      <section>
      <p>Lorem ipsum dolor sit amet.</p>
      </section>
    </main>

    <!-- Footer code goes here -->
    <footer class="secondary border-top">

    </footer> <!-- Remove the placeholder footer text -->

  </body>
</html>
--- /code ---

</div>

--- task ---
**Test:** The browser tab should say `Pixel Pulse Channel`, the page heading should say `Subscribe to Pixel Pulse`, and the old footer text should be gone.
--- /task ---
