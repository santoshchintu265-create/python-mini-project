<!DOCTYPE html>
<html>
<head>
<title>Employee Payroll System</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<h1>Employee Payroll System</h1>

<div class="container">

<label>Employee Name</label>
<input type="text" id="name">

<label>Hours Worked</label>
<input type="number" id="hours">

<label>Pay per Hour</label>
<input type="number" id="rate">

<button onclick="calculateSalary()">Calculate Salary</button>

<h2 id="result"></h2>

</div>

<script src="script.js"></script>

</body>
</html>

body{
    font-family: Arial;
    background-color:#f2f2f2;
    text-align:center;
}

h1{
    color:darkblue;
}

.container{
    width:300px;
    margin:auto;
    background:white;
    padding:20px;
    border-radius:10px;
}

input{
    width:90%;
    padding:8px;
    margin:10px;
}

button{
    padding:10px;
    background:blue;
    color:white;
    border:none;
    cursor:pointer;
}

button:hover{
    background:darkblue;
}

function calculateSalary(){

let name = document.getElementById("name").value
let hours = document.getElementById("hours").value
let rate = document.getElementById("rate").value

let salary = hours * rate

document.getElementById("result").innerHTML =
"Employee: " + name + "<br>Total Salary: ₹" + salary
}
