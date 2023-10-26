# ![JS: Rock, Paper, Scissors Browser Game - Event Listeners](./assets/hero.png)

**Learning objective:** By the end of this section, students will understand how to implement event listeners in JavaScript for specific DOM elements, allowing for user interaction.

Our game will need three event listeners, one for each of our button options. Our event listeners will listen for a click, and call a function that starts the game. 

We'll call this function `play`. What is `play`? Don’t worry, we’ll stub that up in the next section! For now, just add these event listeners to your code in `**app.js**`.

```js
/*----------------------------- Event Listeners -----------------------------*/

document.querySelector('#rock').addEventListener('click', play);
document.querySelector('#paper').addEventListener('click', play);
document.querySelector('#scissors').addEventListener('click', play);
```

> 🧠 `[addEventListener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)` passes the`event` object to its listener function implicitly (tacitly). This means that the callback function that’s called when the event is triggered automatically receives the event object as an argument.

> 🚀 How could we refactor the code above to better adhere to the ***DRY principle**?*

- Possible Solution:

```js
document.querySelectorAll('button').forEach(function (button) {
  button.addEventListener('click', play);
});
```