# JS: Rock, Paper, Scissors Browser Game - Solution

![Hero image](./assets/hero.png)


You did it! 🎉 

If you need to check your work, the full JavaScript solution code can be found here. 

```js


/*-------------------------------- Constants --------------------------------*/

const choices = ["rock", "paper", "scissors"]

/*-------------------------------- Variables --------------------------------*/

let playerChoice, computerChoice, msg

/*------------------------ Cached Element References ------------------------*/

const resultDisplayEl = document.getElementById("result-display")

/*----------------------------- Event Listeners -----------------------------*/

document.getElementById("rock").addEventListener("click", play)
document.getElementById("paper").addEventListener("click", play)
document.getElementById("scissors").addEventListener("click", play)

/*-------------------------------- Functions --------------------------------*/

function getPlayerChoice(event) {
  playerChoice = event.target.id
}

function getComputerChoice() {
  const randomIndex = Math.floor(Math.random() * choices.length)
  computerChoice = choices[randomIndex]
}

function compare() {
  if (playerChoice === computerChoice) {
    msg = 'You tied!'
  } else if (playerChoice === choices[0] && computerChoice === choices[2]) {
    msg = "Congrats! You win!"
  } else if (playerChoice === choices[1] && computerChoice === choices[0]) {
    msg = "Congrats! You win!"
  } else if (playerChoice === choices[2] && computerChoice === choices[1]) {
    msg = "Congrats! You win!"
  } else {
    msg = "You lose! Try again?"
  }
}

function render() {
  resultDisplayEl.textContent = `You chose ${playerChoice} and the computer chose ${computerChoice}. ${msg}`
}

function play(event) {
  getPlayerChoice(event)
  getComputerChoice()
  compare()
  render()
}
```