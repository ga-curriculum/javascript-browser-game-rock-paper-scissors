# ![JS: Rock, Paper, Scissors Browser Game - Level Up - Play Again?](./assets/tktk)

Enhance your Rock, Paper, Scissors game by adding a button that allows users to clear the game state and start anew, offering a streamlined experience without having to reload the page.

## 🚀 **Stretch Goal**: Implementing a "Reset" Button


**Objective:**

Currently there is no visual indication that the game can continue once a player has won or lost. Technically, you can just keep making selections to play future rounds, however, this isn't clearly communicated. It's also arguably not the most elegant user experience. Many games will feature a "reset" option to revert the game back to its original state without having to reload the page. 


Let's implement this functionality. 


1) **Design the Button:**

In your HTML, add a button element below your game's display/message area.

```html
<button id="resetButton">Reset Game</button>
```

2) **Add Reset Functionality:**

Write a function in your JavaScript to reset the game's state.

```js
const resetGame = () => {
  playerChoice = null;
  computerChoice = null;
  msg = '';  // also clear any displayed messages or game outcomes on the page.
}
```

3) **Bind the Function to the Button:**

Use an event listener to call your reset function when the "Reset Game" button is clicked.

```js
document.querySelector('#resetButton').addEventListener('click', resetGame);
```

4) **Test Your Button:**

Play the game a few times, making different choices. Use the reset button to see if the game state is cleared and you can start over seamlessly.

5) **Style your button**

Nobody likes a plain button. 