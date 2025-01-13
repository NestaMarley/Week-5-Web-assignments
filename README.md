# Week-5-Web-assignments
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Assignment</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>JavaScript Assignment</h1>
    <p>Learning JavaScript is fun!</p>
    <div id="dynamic-content"></div>

    <script src="script.js"></script>
</body>
</html>


// Part 1: JavaScript Basics

// Variables and Data Types
let name = "John Manu"; // string
let age = 25; // number
let isStudent = true; // boolean
let hobbies = ["reading", "gaming", "coding"]; // array
let user = {name: "John", age: 25}; // object

console.log(`Name: ${name} (Type: ${typeof name})`);
console.log(`Age: ${age} (Type: ${typeof age})`);
console.log(`Is student: ${isStudent} (Type: ${typeof isStudent})`);

// Operators
function calculator() {
    let num1 = parseFloat(prompt("Enter the first number:"));
    let num2 = parseFloat(prompt("Enter the second number:"));
    let operation = prompt("Choose an operation (+, -, *, /):");

    let result;
    if (isNaN(num1) || isNaN(num2)) {
        alert("Please enter valid numbers.");
        return;
    }

    switch (operation) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 === 0) {
                alert("Cannot divide by zero.");
                return;
            }
            result = num1 / num2;
            break;
        default:
            alert("Invalid operation.");
            return;
    }
    alert(`Result: ${result}`);
}

// Functions
function greetUser(name) {
    return `Hello, ${name}! Welcome to the JavaScript Assignment.`;
}

// Part 2: JavaScript Control Structures

// If Statements
let userAge = parseInt(prompt("What is your age?"));
let eligibilityMessage = userAge >= 18 ? "You are eligible to vote." : "You are not eligible to vote.";
document.body.innerHTML += `<p>${eligibilityMessage}</p>`;

// Loops
let ol = '<ol>';
for (let i = 1; i <= 10; i++) {
    ol += `<li>${i}</li>`;
}
ol += '</ol>';
document.body.innerHTML += ol;

// Part 3: Introduction to the DOM

// Selecting and Modifying HTML Elements
document.querySelector('h1').textContent = "JavaScript in Action!";
const dynamicDiv = document.getElementById('dynamic-content');
dynamicDiv.innerHTML += "<p>This content was added dynamically using JavaScript.</p>";

// Initialize calculator
calculator();
