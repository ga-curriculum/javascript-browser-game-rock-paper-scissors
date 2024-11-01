<h1>
  <span class="headline">Rock, Paper, Scissors</span>
  <span class="subhead">Pseudocode</span>
</h1>

**Learning objective:** By the end of this section, students will be able to write the pseudocode that guides the implementation of key features in their game.

## Learning to plan like a programmer

After crafting our user stories, we'll now outline pseudocode to guide the implementation of these features in our application. To start, let's focus on the logic that powers a typical game of rock, paper, scissors.

Learning to think programmatically might be challenging initially. It requires a different approach to problem-solving than you might be accustomed to. With practice, you'll learn to ask the right questions when planning an application.

- Take note of the types of information you need to keep track of while you play. (hello state!)
- Consider how to adapt the traditional game for a browser environment.
- Think about what and how choices are made during typical game play.
- Reflect on how users' choices, or *input*, can be captured in a browser setting. (DOM interactions and events)

If we consult our user stories, we know that the players selection of "hand" should be made by the user clicking an icon.

> As a user, I want to be able to easily click on one of the "Rock," "Paper," or "Scissors" buttons, so I can make my weapon choice for the game.
>
> As a user, I want visual feedback after making my selection, so I know my choice has been registered.

## Pseudocode

Now let's incorporate this and the rest of our brainstorming into some actionable ***pseudocode***:

```javascript
// 1) Define any variables used to track the state of the game:
//    The players choice
//    The computers choice
//    The match result - win/lose/tie
//    A result message - display who won that round

// 2) Define the required constants:
//    There are only 3 choices a user can make ("rock", "paper", "scissors")
//    We'll need a reference to a DOM element to display messages

// 3) Handle a player clicking a button

// 4) Handle generating random selections for the computer player

```

Next, we'll need to consider the following user stories as we outline the main game logic:

> As a user, I want to see the computer's choice displayed next to mine, so I can compare the two.
>
> As a user, I want to be presented with a clear message indicating the winner of the game, so that I can immediately understand the outcome.

```javascript
// 5) Compare the player choice to the computer choice, and check for a winner

// 6) Render a win/lose/tie message to the player 
//    Include both player and computer selections in the message
//    Clearly indicate who won
```

Now that we know what we want the game to do, we need to start considering the physical structure of our application.

What are the moving parts?
