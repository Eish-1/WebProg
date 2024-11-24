# **Experiment No. 6**

**Problem Statement:**

Create a JavaScript application with window object and document object

**Theory:**

# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <button onclick="showAlert()">Show Alert</button>
    <button onclick="changeBg()">Change background color</button>
    <div id="colorHexaCode">
        #ffffff
    </div>

<script src="app.js"></script>
</body>
</html>

# css

body{
font-family: 'Franklin Gothic Medium',
'Arial Narrow', Arial, sans-serif;
text-align: center;
margin: 1rem;
}

h1{
color: brown;
}

button{
padding: 0.5rem;
font-size: 15px;
margin: 10px;
}

#colorHexaCode{
display: inline-block;
background-color: #D3D3D3;
padding: 15px;
border-radius: 4px;
margin-top: 20px;
height: 37;
width: 191.8;
}

# javascript

function showAlert()
{
window.alert("Hello, this is a window alert!");
}

function changeBg(){
document.body.style.backgroundColor = getRandomColor();
document.getElementById('colorHexaCode').innerHTML = getRandomColor();
}

function getRandomColor(){
poss = "0123456789ABCDEF";
col = "#";
for (let i = 0; i<6; i++ ){
col += poss[Math.floor(Math.random()*16)];
}
return col; }
