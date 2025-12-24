<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Calculator</title>

    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }

        .calculator {
            width: 260px;
            margin: 100px auto;
            padding: 15px;
            background-color: #222;
            border-radius: 10px;
        }

        #display {
            width: 100%;
            height: 45px;
            font-size: 22px;
            margin-bottom: 10px;
            text-align: right;
            padding-right: 10px;
            border-radius: 5px;
            border: none;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
        }

        button {
            height: 45px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            background-color: #444;
            color: white;
        }

        button:hover {
            background-color: #666;
        }

        .zero {
            grid-column: span 2;
        }
    </style>
</head>
<body>

<div class="calculator">
    <input type="text" id="display" disabled>

    <div class="buttons">
        <button onclick="clearDisplay()">C</button>
        <button onclick="append('/')">/</button>
        <button onclick="append('*')">*</button>
        <button onclick="append('-')">-</button>

        <button onclick="append('7')">7</button>
        <button onclick="append('8')">8</button>
        <button onclick="append('9')">9</button>
        <button onclick="append('+')">+</button>

        <button onclick="append('4')">4</button>
        <button onclick="append('5')">5</button>
        <button onclick="append('6')">6</button>
        <button onclick="calculate()">=</button>

        <button onclick="append('1')">1</button>
        <button onclick="append('2')">2</button>
        <button onclick="append('3')">3</button>
        <button onclick="append('0')" class="zero">0</button>
    </div>
</div>

<script>
    let display = document.getElementById("display");

    function append(value) {
        display.value += value;
    }

    function clearDisplay() {
        display.value = "";
    }

    function calculate() {
        try {
            display.value = eval(display.value);
        } catch {
            display.value = "Error";
        }
    }
</script>

</body>
</html>
# basic-calculator
A SIMPLE CALCULATOR USING HTML CSS AND JAVA SCRIPT FOR BASIC ARETHEMATIC OPERATIONS
