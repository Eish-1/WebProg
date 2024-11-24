# **Experiment No. 8**

**Problem Statement:**

**Source code :**

# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Squares</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Squares of Numbers</h1>
        <p>Click the button to display squares of numbers from 1 to 10:</p>
        <button id="generateBtn">Generate Squares</button>
        <ul id="numberList"></ul>
    </div>
    <script src="app.js"></script>
</body>
</html>

# css

body {
font-family: Arial, sans-serif;
background-color: #f0f8ff;
text-align: center;
margin: 0;
padding: 20px;
}

.container {
background-color: white;
border-radius: 10px;
box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.1);
max-width: 500px;
margin: 0 auto;
padding: 20px;
}

h1 {
color: #333;
}

button {
background-color: #000;
color: white;
border: none;
padding: 10px 20px;
font-size: 16px;
border-radius: 5px;
cursor: pointer;
}

button:hover {
background-color: #343434;
}

ul {
list-style-type: none;
padding: 0;
margin-top: 20px;
}

li {
background-color: ghostwhite;
padding: 10px;
margin-bottom: 5px;
border-radius: 5px;
border: 1px solid #ddd;
}

# javascript

function generateSquares() {
const numberList = document.getElementById('numberList');
numberList.innerHTML = ''; // clear the list before generating

    for (let i = 1; i <= 10; i++) {
        const listItem = document.createElement('li');
        listItem.textContent = `Number: ${i}, Square: ${i * i}`;
        numberList.appendChild(listItem);
    }

}

document.getElementById('generateBtn').addEventListener('click', generateSquares);
