# **Experiment No. 4**

**Problem Statement:**

**Source code :**

# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="app">
        <h1>To-Do List</h1>
        <div id="inputContainer">
            <input type="text" id="newTask" placeholder="Enter a new task">
            <button id="addTaskButton">Add Task</button>
        </div>
        <ul id="taskList"></ul>
    </div>
    <script src="app.js"></script>
</body>
</html>

# css

body {
margin: 0;
padding: 0;
font-family: Arial, sans-serif;
background-color: #f4f4f9;
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
}

    #app {
    background: #ffffff;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    padding: 20px;
    width: 300px;
    text-align: center;
    }

    h1 {
    margin-bottom: 20px;
    color: #333;
    }

    #inputContainer {
    display: flex;
    gap: 10px;
    margin-bottom: 20px;
    }

    #newTask {
    flex: 1;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 14px;
    }

    #addTaskButton {
    padding: 10px 15px;
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 14px;
    }

    #addTaskButton:hover {
    background-color: #218838;
    }


    #taskList {
    list-style: none;
    padding: 0;
    margin: 0;
    }

    #taskList li {
    background: #f9f9f9;
    padding: 10px;
    margin: 5px 0;
    border-radius: 5px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 1px solid #ddd;
    }

    .editButton, .deleteButton {
    border: none;
    cursor: pointer;
    padding: 5px 8px;
    border-radius: 5px;
    font-size: 12px;
    }

    .editButton {
    background-color: #007bff;
    color: white;
    }

    .editButton:hover {
    background-color: #0056b3;
    }

    .deleteButton {
    background-color: #dc3545;
    color: white;
    }

    .deleteButton:hover {
    background-color: #c82333;
    }

# javascript

// app.js

// Selectors
const newTaskInput = document.getElementById("newTask");
const addTaskButton = document.getElementById("addTaskButton");
const taskList = document.getElementById("taskList");

// Event Listeners
addTaskButton.addEventListener("click", addTask);

// Functions

// Add Task
function addTask() {
const taskText = newTaskInput.value.trim();

    if (taskText === "") {
        alert("Please enter a task!");
        return;
    }

    const listItem = document.createElement("li");

    const taskSpan = document.createElement("span");
    taskSpan.textContent = taskText;

    const editButton = document.createElement("button");
    editButton.textContent = "Edit";
    editButton.classList.add("editButton");
    editButton.addEventListener("click", () => editTask(listItem, taskSpan));

    const deleteButton = document.createElement("button");
    deleteButton.textContent = "Delete";
    deleteButton.classList.add("deleteButton");
    deleteButton.addEventListener("click", () => deleteTask(listItem));

    listItem.appendChild(taskSpan);
    listItem.appendChild(editButton);
    listItem.appendChild(deleteButton);

    taskList.appendChild(listItem);

    newTaskInput.value = "";

}

// Edit Task
function editTask(listItem, taskSpan) {
const newTaskText = prompt("Edit your task:", taskSpan.textContent);

    if (newTaskText !== null && newTaskText.trim() !== "") {
        taskSpan.textContent = newTaskText.trim();
    }

}

// Delete Task
function deleteTask(listItem) {
taskList.removeChild(listItem);
}
