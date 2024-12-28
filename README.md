# Calculator
Its my first project in github
<br>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <div class="calculator">
    <input type="text" id="display" class="display" disabled />
    <div class="buttons">
      <button class="btn" onclick="appendToDisplay('7')">7</button>
      <button class="btn" onclick="appendToDisplay('8')">8</button>
      <button class="btn" onclick="appendToDisplay('9')">9</button>
      <button class="btn operator" onclick="appendToDisplay('/')">/</button>
      
      <button class="btn" onclick="appendToDisplay('4')">4</button>
      <button class="btn" onclick="appendToDisplay('5')">5</button>
      <button class="btn" onclick="appendToDisplay('6')">6</button>
      <button class="btn operator" onclick="appendToDisplay('*')">*</button>
      
      <button class="btn" onclick="appendToDisplay('1')">1</button>
      <button class="btn" onclick="appendToDisplay('2')">2</button>
      <button class="btn" onclick="appendToDisplay('3')">3</button>
      <button class="btn operator" onclick="appendToDisplay('-')">-</button>
      
      <button class="btn" onclick="appendToDisplay('0')">0</button>
      <button class="btn" onclick="appendToDisplay('.')">.</button>
      <button class="btn" onclick="clearDisplay()">C</button>
      <button class="btn operator" onclick="appendToDisplay('+')">+</button>
      
      <button class="btn equal" onclick="calculate()">=</button>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
