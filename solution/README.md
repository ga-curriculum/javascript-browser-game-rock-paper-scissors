<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Solution</span>
</h1>

You did it! 🎉

If you need to check your work, the full JavaScript solution code can be found here.

```js

/*-------------------------------- Constants --------------------------------*/

const choices = ['rock', 'paper', 'scissors'];

/*-------------------------------- Variables --------------------------------*/

let playerChoice;
let computerChoice;
let msg;

/*------------------------ Cached Element References ------------------------*/

const resultDisplayEl = document.querySelector('#result-display');

/*-------------------------------- Functions --------------------------------*/

const getPlayerChoice = (event) => {
  playerChoice = event.target.id;
};

const getComputerChoice = () => {
  const randomIndex = Math.floor(Math.random() * choices.length);
  computerChoice = choices[randomIndex];
};

const compare = () => {
  if (playerChoice === computerChoice) {
    msg = 'You tied!';
  } else if (playerChoice === choices[0] && computerChoice === choices[2]) {
    msg = 'Congrats! You win!';
  } else if (playerChoice === choices[1] && computerChoice === choices[0]) {
    msg = 'Congrats! You win!';
  } else if (playerChoice === choices[2] && computerChoice === choices[1]) {
    msg = 'Congrats! You win!';
  } else {
    msg = 'You lose! Try again?';
  }
};

const render = () => {
  resultDisplayEl.textContent = `You chose ${playerChoice} and the computer chose ${computerChoice}. ${msg}`
}

const play = (event) => {
  getPlayerChoice(event);
  getComputerChoice();
  compare();
  render();
}

/*----------------------------- Event Listeners -----------------------------*/

document.querySelector('#rock').addEventListener('click', play);
document.querySelector('#paper').addEventListener('click', play);
document.querySelector('#scissors').addEventListener('click', play);

```
