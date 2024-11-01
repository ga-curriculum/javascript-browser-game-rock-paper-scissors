<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Constants Variables and Cached Elements</span>
</h1>

**Learning objective:** By the end of this section, students will understand how to initialize constants and variables that represent game state, and how to create cached references to essential DOM elements.

The next few sections will consider the following user stories:

> As a user, I want to see the computer's choice displayed next to mine, so I can compare the two.
>
> As a user, I want to be presented with a clear message indicating the winner of the game, so that I can immediately understand the outcome.

## Constants

Initialize a globally available constant called `choices`. The `choices` constant will hold the three moves a player can make inside of an array. This constant, in contrast with our state variables, will *not* change or update.

```js
/*-------------------------------- Constants --------------------------------*/

const choices = ['rock', 'paper', 'scissors'];
```

## Variables (game state)

In our game, we'll manage three key pieces of information that will be our game's ***state***:

1. The player's selection, represented by the variable (`playerChoice`).
2. The computer's selection, which is randomly determined, stored in (`computerChoice`).
3. The outcome message (winner/loser/tie) of the game, held in the (`msg`) variable.

For now, we'll only initialize these variables and assign their values based on the game's progression later.

```js
/*-------------------------------- Variables --------------------------------*/

let playerChoice;
let computerChoice; 
let msg;
```

> 💡 State describes the *status* of an individual object or entire program. When determining what needs to be held in state, ask yourself “What changes do we need to keep track of to know the current state of the game?”

## Cached elements

In the Cached Element References section, define a cached element reference that will be used to display the game message. Simply put, we need to grab the element in the DOM that will be tasked with displaying our message and save it to a variable for ease of use later. We'll name this `resultDisplayEl`.

The `msg` variable we created above will store the interchangeable *message data*, while `resultDisplayEl` represents the *DOM element* that will display that message.

```js
/*------------------------ Cached Element References ------------------------*/

const resultDisplayEl = document.querySelector('#result-display');
```

> ❓ What element of HTML are we targeting with the above command?
