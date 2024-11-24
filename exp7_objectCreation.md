# **Experiment No. 7**

**Problem Statement:**

create objects and method of objects

**Source code :**

# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple JavaScript Object Example</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Object Creation and Methods</h1>
        <button id="createPersonBtn">Create Person</button>
        <div id="personInfo"></div>
    </div>
    <script src="app.js"></script>
</body>
</html>

# css

body {
font-family: Arial, sans-serif;
background-color: #f4f4f9;
color: #333;
text-align: center;
margin-top: 50px;
}

.container {
width: 50%;
margin: 0 auto;
}

button {
background-color: grey;
color: white;
padding: 15px 32px;
font-size: 16px;
border: none;
cursor: pointer;
margin-top: 20px;
}

#personInfo {
margin-top: 20px;
font-size: 18px;
}

# javascript

// Object constructor for Person

//it generally refers to creating objects using constructors or
// object literals, and defining methods (functions) that belong to those objects.
function Person(name, age) {
this.name = name;
this.age = age;

    // Method to return a greeting
    this.greet = function() {
        return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
    };

    // Method to increment age
    this.haveBirthday = function() {
        this.age += 1;
        return `Happy Birthday! I am now ${this.age} years old.`;
    };

}

// Event listener for button click
document.getElementById('createPersonBtn').addEventListener('click', function() {
let name = prompt("Enter name of the person:");
let age = prompt("Enter age:");
age = parseInt(age);
const person = new Person(name, age);

    // Display person info and call methods
    document.getElementById('personInfo').innerHTML = `
        <p>${person.greet()}</p>
        <p>${person.haveBirthday()}</p>
    `;

});
