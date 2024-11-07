<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Scaffolding the Application</span>
</h1>

**Learning objective:** Students will prepare the structure of their webpage using the provided starter code.

## Creating our main page

We know from our user stories that we need an attention grabbing landing page, with game play choices prominently displayed.

> As a user, I want to see a landing page when I arrive at the website, so I know I'm in the right place.
>
> As a user, I want to see clearly labeled buttons for "Rock," "Paper," and "Scissors," on the landing page, so I instantly know my options for game play.
>
> As a user, I want to be able to click on one of the "Rock," "Paper," or "Scissors" buttons, making it easy to select my game move.

Based on these stories we are able to make some assumptions about what our HTML structure should be:

1) Our game will need a landing page with a clear title so that users know they have reached the correct page.
2) We need Rock, Paper, and Scissors buttons displayed prominently so a user can quickly choose one
3) We should have a text element for communicating messages to the user- such as *what the computer chose*, and *who won the round*

To allow you to concentrate on the core objectives of this lesson—JavaScript and DOM manipulation—we've taken these assumptions and provided pre-written HTML and CSS code. This allows you to focus on developing the game logic in JavaScript.

Let's review our starter code!

## HTML

Add the following to your `index.html` file.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rock Paper Scissors</title>
  <link rel="stylesheet" href="./css/style.css" />
  <script defer src="./js/app.js"></script>
</head>

<body>
  <header>
    <h1>Rock Paper Scissors</h1>
    <p id="result-display"></p>
  </header>
  <main>
    <button id="rock">🪨</button>
    <button id="paper">📄</button>
    <button id="scissors">✂️</button>
  </main>
</body>

</html>
```

## CSS

Add the following code to your CSS stylesheet:

```css
html, body {
  margin: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

header {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#result-display {
  min-height: 20px;
}

button {
  margin: 10px;
  font-size: 40px;
  background-color: transparent;
  border: 1px solid rgba(0,0,0,.1);
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

button:hover {
  border: 1px solid rgba(0,0,0,0.5);
  cursor: pointer;
}
```

## JavaScript

In `app.js`, add the following sections using commented-out lines. This will help us organize our code a bit.

```javascript
/*-------------------------------- Constants --------------------------------*/

/*-------------------------------- Variables --------------------------------*/

/*------------------------ Cached Element References ------------------------*/

/*-------------------------------- Functions --------------------------------*/

/*----------------------------- Event Listeners -----------------------------*/
```

> 💡 Pro Tip: Use the headings above when building simple browser games! Having a plan-of-attack and basic scaffolding is one of the best ways to prevent getting ‘stuck’ and not knowing where to start coding.
