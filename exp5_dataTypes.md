# **Experiment No. 5**

**Source code :**

# html file:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Data Types and Operators</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>JavaScript Data Types, Statements, Keywords & Operators: </h1>
    <script src="app.js"></script>
</body>
</html>

# css file:

body {
font-family: Arial, sans-serif;
background-color: #f0f8ff;
text-align: center;
margin-top: 50px;
color: #333;
}
button {
background-color: #007bff;
color: white;
padding: 15px 32px;
font-size: 16px;
border: none;
cursor: pointer;
margin-top: 20px;
}

# javascript

// Data Types Example
let numberType = 25; // Number
let stringType = "Hello"; // String
let booleanType = true; // Boolean
let undefinedType; // Undefined
let objectType = { name: "John", age: 30 }; // Object
let array = [20,30,40]; // array

const body = document.querySelector("body");

window.document.body.innerHTML += `<h2>Data Types Example</h2>`;

window.document.body.innerHTML += `<p>Number: ${numberType}</p>`;
window.document.body.innerHTML += `<p>String: ${stringType}</p>`;
window.document.body.innerHTML += `<p>Boolean: ${booleanType}</p>`;
window.document.body.innerHTML += `<p>Undefined: ${undefinedType}</p>`;
window.document.body.innerHTML += `<p>Array: [${array}]</p>`;
window.document.body.innerHTML += `<p>Object: ${JSON.stringify(objectType)}</p>`;

let a = 100;
let b = 20;
let sum = a + b;  
 let product = a \* b;  
 let divison = a / b;
let modulus = a % b;

window.document.body.innerHTML += `<h2>Operators and Operations</h2>`;
window.document.body.innerHTML += `<p>a = ${a}, b = ${b}</p>`
window.document.body.innerHTML += `<p>Additon: a + b = ${sum}</p>`
window.document.body.innerHTML += `<p>Multiplication: a * b = ${product}</p>`
window.document.body.innerHTML += `<p>Division: a / b = ${divison}</p>`
window.document.body.innerHTML += `<p>Modulus: a % b = ${modulus}</p>`

window.document.body.innerHTML += `<h2>Conditional Statement</h2>`;
let button = document.createElement('button');
button.innerText = "clickMe";
document.body.appendChild(button);

button.addEventListener("click",()=>{
let user = prompt("enter your age: ");
let para = document.createElement('p');
if(user > 20){
para.innerText = `Oh you are above 20!`

    }else if(user == 20){
        para.innerText = `Oh you are JUST 20!`

    }
    else{
        para.innerText = `Oh you are below 20 huh`

    }
    button.insertAdjacentElement("afterend", para);

})
