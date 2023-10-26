# ![JS: Rock, Paper, Scissors Browser Game - 🎮 Game Logic](./assets/hero.png)

**Learning objective:** By the end of this section, students will be able to utilize JavaScript functions to manage game state, understand event handling from user interactions, and implement game logic to determine the outcome of one round of play. 

## Setup `play`

> 🥅 Goal: contain and organize our game logic

In a round of Rock, Paper, Scissors a player can click on one of three buttons to select the "hand" or weapon they wish to play. Clicking one of these buttons will call upon the `play` function, due to the event listeners we set up in the previous step. 

Within our `play` function, we will eventually call upon any other functions that need to be executed to complete a round of the game. We’ll build out the remaining functions next, but for now let’s stub up the `play` function and verify that our event listeners are working properly with a `console.log`.

```js
const play = (ev) => {
  console.log(ev.target);
}
```

Now try clicking on a button! Take a few minutes to inspect `event.target` in the browser console.


## `getPlayerChoice`


> 🥅 Goal: set `playerChoice` to the `id` of the button the player clicked.


Next you’ll need to create a function to handle setting game state. The `getPlayerChoice` function will be responsible for updating the `playerChoice` state variable with a player’s selection. 

Stub up the `getPlayerChoice` function you see below. Then refactor your code to call it within `play`.

```js
const getPlayerChoice = (ev) => {
  console.log('getPlayerChoice:', ev);
};

const play = (ev) => {
  getPlayerChoice(ev);
};
```

> 🗒️ Note: Our `getPlayerChoice` function relies on the `event` object to set `playerChoice` state. In the `play` function, we have to pass the `event` down to getPlayerChoice so that it has access to `event` as well!


Earlier we saw how `event.target` contains data related to the clicked element. For our purposes, the most important piece of information inside `event.target` is the element’s `id`, a unique identifier for each button which corresponds to the `id` attribute assigned to the button in our html file.

By accessing the `id` of the button a player clicked on, we can update the `playerChoice` variable accordingly. When a player clicks on the button with the `id` “scissors”, our function should set `playerChoice` to the string “scissors”. 

```js
const getPlayerChoice = (ev) => {
  playerChoice = ev.target.id;
};

const play = (ev) => {
  getPlayerChoice(ev);
  console.log(playerChoice); // <= verify that everything is working!
};
```

```html
<main>
  <button id="rock">🪨</button>
  <button id="paper">📄</button>
  <button id="scissors">✂️</button>
  // Note: the ids match the strings we will use to compare choices later
</main>
```

## `getComputerChoice`


> 🥅 Goal: set `computerChoice` to a random element from the `choices` array


Now that the `playerChoice` state is set, we also need a function that can capture and update `computerChoice` state. We can do this by generating a random number between 0 - 2, and using the resulting number as an index. 

We’ll use square bracket notation to access our `choices` array at that random index.

Every time this function runs, it will select a new element from the choices array randomly and assign it to our `computerChoice` state variable, like so:

```js
const getComputerChoice = () => {
  const randomIndex = Math.floor(Math.random() * choices.length);
  computerChoice = choices[randomIndex];
};
```

## `compare`

> 🥅 Goal: set `msg` text based on a comparison of `playerChoice` and `computerChoice` state

Next, we’ll build the main game logic- a function to compare the choices stored in state and determine the result! This function will also set `msg` state based on that result.

- If the player and computer have chosen the same "hand" or weapon, we'll set `msg` to "You tied!."
- Otherwise, we’ll need to determine all of the possible outcomes in which the player would have the winning hand. If none of those scenarios are true, our else statement will assume that the player lost.


```js
const compare = () => {
  if (playerChoice === computerChoice) {
    msg = 'You tied!';
  } else if (playerChoice === choices[0] && computerChoice === choices[2]) { // "rock" vs. "scissors"
    msg = 'Congrats! You win!';
  } else if (playerChoice === choices[1] && computerChoice === choices[0]) { // "paper" vs. "rock"
    msg = 'Congrats! You win!';
  } else if (playerChoice === choices[2] && computerChoice === choices[1]) { // "scissors" vs. "paper"
    msg = 'Congrats! You win!';
  } else {
    msg = 'You lose! Try again?';
  }
};
```

> 🧠 For more information on how this solution works, check out the [**Logical AND && Operator**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND) on MDN.
