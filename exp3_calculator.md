# **Experiment No. 3**

**Source code :**

# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Practicing Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="calc">
        <div id="content">
            <form>
                <h2 ><center> <font color="white">Calculator</font> </center></h2>
                <div id="output">
                    <input type="text" id='res'>
                </div>
                <div class="btn">
                    <input type="button" value='C' onclick="Clear()" id="clear">
                    <input type="button" value='CE' onclick="Back()" id="backspace">
                    <input type="button" value='%' onclick="Solve('%')">
                    <input type="button" value='/' onclick="Solve('/')">
                    <br>
                    <input type="button" value='7' onclick="Solve('7')">
                    <input type="button" value='8' onclick="Solve('8')">
                    <input type="button" value='9' onclick="Solve('9')">
                    <input type="button" value='x' onclick="Solve('*')">
                    <br>
                    <input type="button" value='4' onclick="Solve('4')">
                    <input type="button" value='5' onclick="Solve('5')">
                    <input type="button" value='6' onclick="Solve('6')">
                    <input type="button" value='-' onclick="Solve('-')">
                    <br>
                    <input type="button" value='1' onclick="Solve('1')">
                    <input type="button" value='2' onclick="Solve('2')">
                    <input type="button" value='3' onclick="Solve('3')">
                    <input type="button" value='+' onclick="Solve('+')">
                    <br>
                    <input type="button" value='00' onclick="Solve('00')">
                    <input type="button" value='0' onclick="Solve('0')">
                    <input type="button" value='.' onclick="Solve('.')">
                    <input type="button" value='=' onclick="Result()">
                </div>
            </form>
        </div>
    </div>
 </div>

    <script src="index.js"></script>

</body>
</html>

# css

body{
background-color: #2c3e50;
}

- {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }
  #calc {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  }
  #content {
  background: black;
  padding: 20px;
  border-radius: 10px;
  }

#content form input {
border: 2;
outline: 2;
width: 50px;
height: 50px;
border-radius: 8px;
font-size: 20px;
margin: 10px;
cursor: pointer;
background: grey;
}

#backspace {
background-color: #e74c3c;
color: #fff;
}

#res {
padding: 10px;
background-color: #2c3e50;
color: #fff;
border-radius: 5px;
}

#clear {
background-color: #e74c3c;
color: #fff;
}

form #output {
display: flex;
justify-content: flex-end;
margin: 15px 0;
}

form #output input {
text-align: right;
flex: 1;
font-size: 25px;
}

# javascript

function Solve(val) {
var v = document.getElementById('res');
v.value += val;
}

function Result() {
var num1 = document.getElementById('res').value;
try {
var num2 = eval(num1.replace('x', '\*'));
document.getElementById('res').value = num2;
} catch {
document.getElementById('res').value = 'Error';
}
}

function Clear() {
var inp = document.getElementById('res');
inp.value = '';
}

function Back() {
var ev = document.getElementById('res');
ev.value = ev.value.slice(0, -1);
}

document.addEventListener('keydown', function (event) {
const key = event.key;
const validKeys = '0123456789+-_/.%';
if (validKeys.includes(key)) {
Solve(key === '_' ? 'x' : key);
} else if (key === 'Enter') {
Result();
} else if (key === 'Backspace') {
Back();
} else if (key.toLowerCase() === 'c') {
Clear();
}
});
