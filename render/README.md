# ![JavaScript Browser Game - Rock, Paper, Scissors - Render](./assets/hero.png)

**Learning objective:** By the end of this section, students will understand how to dynamically update the DOM to reflect changes in game state, specifically by utilizing a render function to showcase the results to the player.

## `render`

> 🥅 Goal: update the text of `resultDisplayEl` to reflect the changes in game state.


Now that the result of our compare function has updated `msg` state, we need to show the player the result! 

It’s best practice to do this within a `render` function, whose job it is to re-render elements of the DOM when the state changes. 

In this case, our `playerChoice`, `computerChoice`, and `msg` state have all changed since the page first loaded. We’ll update the `textContent` of `resultDisplayEl` to reflect those changes. 

```js
const render = () => {
  resultDisplayEl.textContent = `You chose ${playerChoice} and the computer chose ${computerChoice}. ${msg}`;
}
```

If you test this function, the final readout on screen should look something like this:

```
You chose rock and the computer chose scissors. You Win!
```

This fulfills the requirements of our second to last user story:

> As a user, I want to be presented with a clear message indicating the winner of the game, so that I can immediately understand the outcome.