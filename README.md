# mini-ludo-game
Mini ludo Dice Game using HTML,CSS and javascript
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mini Ludo Game</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h1>Mini Ludo Dice</h1>
    <div class="dice" id="dice">🎲</div>
    <button onclick="rollDice()">Roll Dice</button>
    <p id="output"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>
body {
    background: #f0f0f0;
    font-family: 'Segoe UI', sans-serif;
    text-align: center;
    padding: 50px;
  }
  
  .container {
    background: white;
    padding: 30px;
    border-radius: 10px;
    width: 300px;
    margin: auto;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
  }
  
  h1 {
    color: #444;
  }
  
  .dice {
    font-size: 100px;
    margin: 20px 0;
  }
  
  button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #2980b9;
  }
  
  #output {
    font-size: 18px;
    margin-top: 20px;
    color: #333;
  }
  function rollDice() {
    const diceValue = Math.floor(Math.random() * 6) + 1;
    const dice = document.getElementById("dice");
    const output = document.getElementById("output");
  
    const diceFaces = ["⚀", "⚁", "⚂", "⚃", "⚄", "⚅"];
    dice.textContent = diceFaces[diceValue - 1];
    output.textContent = "You rolled a " + diceValue;
  }
