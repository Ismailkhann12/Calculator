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
<br>
Css file
<br>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f9;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.calculator {
  background-color: #fff;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  padding: 20px;
  border-radius: 10px;
  width: 260px;
}

.display {
  width: 100%;
  height: 50px;
  text-align: right;
  font-size: 24px;
  padding: 10px;
  margin-bottom: 20px;
  border: 2px solid #ccc;
  border-radius: 5px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.btn {
  font-size: 20px;
  padding: 20px;
  background-color: #f0f0f0;
  border: 2px solid #ccc;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn:hover {
  background-color: #ddd;
}

.operator {
  background-color: #fe9241;
  color: white;
}

.operator:hover {
  background-color: #f77b26;
}

.equal {
  grid-column: span 2;
  background-color: #41fe6d;
  color: white;
}

.equal:hover {
  background-color: #39d563;
}
<br>
JavaScrift
<br>
let display = document.getElementById('display');

function appendToDisplay(value) {
  display.value += value;
}

function clearDisplay() {
  display.value = '';
}

function calculate() {
  try {
    display.value = eval(display.value);
  } catch (e) {
    display.value = 'Error';
  }
}
