<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Play Again?</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to enhance their Rock, Paper, Scissors game by implementing a reset functionality. They will learn to integrate a reset button into their game, write JavaScript functions to clear and reset the game state, and bind these functions to the button using event listeners. 

Enhance your Rock, Paper, Scissors game by adding a button that allows users to clear the game state and start anew, offering a streamlined experience without having to reload the page.

## Implementing a reset button

Currently there is no visual indication that the game can continue once a player has won or lost. Technically, you can just keep making selections to play future rounds, however, this isn't clearly communicated. It's also arguably not the most elegant user experience. Many games will feature a "reset" option to revert the game back to its original state without having to reload the page.

Let's implement this functionality.

### Design the button

In your HTML, add a button element below your game's display/message area.

```html
<button id="resetButton">Reset Game</button>
```

### Add reset functionality

Write a function in your JavaScript to reset the game's state.

```js
const resetGame = () => {
  playerChoice = null;
  computerChoice = null;
  msg = '';  // also clear any displayed messages or game outcomes on the page.
}
```

### Bind the function to the button

Use an event listener to call your reset function when the **Reset Game** button is clicked.

```js
document.querySelector('#resetButton').addEventListener('click', resetGame);
```

### Test your button

Play the game a few times, making different choices. Use the reset button to see if the game state is cleared and you can start over seamlessly.

### Style your button

Nobody likes a plain button.
