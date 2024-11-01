<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Play</span>
</h1>

**Learning objective:** By the end of this section, students will understand how to effectively organize and sequence game logic within a central function. They will learn to integrate individual functions to create a sequential gameplay progression triggered by a user's action, specifically by executing multiple functions in response to a single event.

## `play`

> 🥅 Goal: contain and organize our game logic

Finally, we have all of the functions necessary to make our game work! Let’s make sure they are all being used, and called upon in the correct order in our `play` function. Reminder- `play` is the function called when the user initiates game play by clicking Paper, Rock, or Scissors.

```js
const play = (event) => {
  getPlayerChoice(event);  // captures player choice, updates state
  getComputerChoice();  // randomly selects computers choice, updates state
  compare();            // determines winning result
  render();             // renders result message back to the user 
};
```

Let's review! It might be useful to take another look at our event listeners. We pass our `play` function to the event listeners on our rock paper scissors buttons, so that whenever a player clicks one, each of the functions invoked in `play` will run sequentially, updating state variables and rendering the changes back for the player to see.

Now that the `play` function is fully built out, its easier to see how this long chain of functionality is triggered by a single click!

```js
/*----------------------------- Event Listeners -----------------------------*/

document.querySelector('#rock').addEventListener('click', play);
document.querySelector('#paper').addEventListener('click', play);
document.querySelector('#scissors').addEventListener('click', play);
```
