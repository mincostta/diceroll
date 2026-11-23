# 🎲 Dice Roll

A website where two players can enter their names and roll a pair of dice. The player who gets the highest number wins. The dice roll is powered by JavaScript code that generates a random number between 1 and 6. [Access here](https://mincostta.github.io/rolagem-dados/).

## ⚙️ Technologies Used
- **Languages**: HTML, CSS, JavaScript
- **Tools**: Git

## 🔧 How It Works
Once the calculate button is clicked, the JavaScript code generates a random number between 1 and 100. The button can only be clicked after the user has entered two names, which must be different from each other. The resulting percentage is displayed instantly, accompanied by a heart emoji representing how good the result is.

## ⚙️ Button Click Event

```javascript
    rolar.addEventListener('click', function() {
    var rolagem1 = Math.random();
    rolagem1 = rolagem1 * 6 + 1;
    rolagem1 = Math.floor(rolagem1);

    var rolagem2 = Math.random();
    rolagem2 = rolagem2 * 6 + 1;
    rolagem2 = Math.floor(rolagem2);

    dado1.setAttribute("src", "./imgs/dado" + rolagem1 + ".png");
    dado2.setAttribute("src", "./imgs/dado" + rolagem2 + ".png");

    if (rolagem1 == rolagem2) {
        texto.textContent = "É um empate!";
    }

    else if (rolagem1 > rolagem2) {
        texto.textContent = player1.textContent + " venceu!"
    }

    else if (rolagem2 > rolagem1) {
        texto.textContent = player2.textContent + " venceu!"
    }
});
```
