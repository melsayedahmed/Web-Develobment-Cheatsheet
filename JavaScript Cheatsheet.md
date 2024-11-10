 # ********************* JavaScript Cheatsheet *********************

## General

### 1. Comments

```js
// this is a comment 
/* or this is a comment */

// This code will be ignored. Comments are generally a bad idea, your code should be explicit enough as it is.
```

---
---
---


## Variables

### 1. Variable creation

```js
let school = "SheCodes";
let fullPackage = "SheCodes Pro";
let projects = 4;
let awesome = true;
```

### 2. Variable operations

```js
let x = 2;
let y = 3;
let z = x + y; // 5

let city = "Lisbon";
let country = "Portugal";
let place = city + " " + country; //Lisbon Portugal
```

### 3. Variable data Types

```js
let age = 23; // Number
let name = "Julie"; // String
let canCode = true; // Boolean, could also be false
```

### 4. Structure structure types

```js
let students = ["Kate", "Julie", "Mariana"]; // Array

let kate = {
  firstName: "Kate",
  lastName: "Johnson",
  age: 23,
  canCode: true,
}; // Object
```

---
---
---

## Alerts & Prompts

### 1. Alert

```js
alert("Olá");

let name = "Angela";
alert(name);
```

### 2. Prompt

```js
let firstName = prompt("What is your first name");
let lastName = prompt("What is your last name");
let fullName = firstName + " " + lastName;
alert(fullName);
```

---
---
---

## If else

### 1. if statement

```js
let country = prompt("What country are you from?");

if (country === "Portugal") {
  alert("You are cool");
}

if (country !== "Portugal") {
  alert("Too bad for you");
}
```

### 2. if else statement

```js
let age = prompt("How old are you?");

if (age < 18) {
  alert("You cannot apply");
} else {
  alert("You can apply");
}
```

### 3. Nested if else statements

```js
if (age < 18) {
  alert("you can't apply");
} else {
  if (age > 120) {
    alert("you can't apply");
  } else {
    alert("you can apply");
  }
}
```

### 4. Logical Or

```js
if (age < 18 || gender === "male") {
  alert("You can't join SheCodes 👩‍💻");
}
// The code will be executed if one statement is true.
```

### 5. Logical And

```js
if (continent === "Europe" && language === "Portuguese") {
  alert("You are from Portugal 🇵🇹");
} else {
  alert("You are not from Portugal");
}
// The code will be executed if both statements are true.
```

### 6. Comparison and Logical Operators

```js
2 > 3 // false 
2 < 3 // true 
2 <= 2 // true
3 >= 2 // true
2 === 5 // false 
2 !== 3 // true 
1 + 2 === 4 // false
```

---
---
---


## Strings

### 1. Creating a string

```js
let name = "SheCodes"; // "SheCodes"
```

### 2. String concatenation

```js
let firstName = "Julie";
let lastName = "Johnson";
let fullName = firstName + " " + lastName; // "Julie Johnson"

//or
let fullName = `${firstName} ${lastName}`;
```

### 3. Trim

```js
let city = " Montreal  ";
city = city.trim(); // "Montreal"
```

### 4. Replace

```js
let city = "Montreal";
city = city.replace("e", "é"); // "Montréal"
```

### 5. toLowerCase

```js
let city = "Montreal";
city = city.toLowerCase(); // "montreal"
```

### 6. toUpperCase

```js
let city = "Montreal";
city = city.toUpperCase(); // "MONTREAL"
```

### 7. Template literals

```js
let city = "Denver";
let sentence = `Kate is from ${city}`; // Kate is from Denver
```

---
---
---

## Arrays

### 1. Array declaration

```js
let myList = [];
let fruits = ["apples", "oranges", "bananas"];
myList = ['banana', 3, go, ['John', 'Doe'], {'firstName': 'John', 'lastName': 'Smith'}]
```

### 2. Access an Array

```js
fruits
fruits[0]
fruits[1]
fruits[2]
fruits[3]
```

### 3. Update an Array item

```js
fruits[1] = "Mango";
fruits[1] = 3;
```

### 4. while loop

```js
let times = 0;
while (times < 10) {
  console.log(times);
  times = times + 1;
}
```

### 5. forEach loop

```js
let fruits = ['apples', 'oranges', 'bananas'];
fruits.forEach(function(fruit) {
  alert("I have " + fruit + " in my shopping bag");
});
```

### 6. do while loop

```js
let times = 0;
do {
  console.log(times);
  times = times + 1;
} while(times < 10)
```

### 7. for loop

```js
for (let i = 0; i < 10; i++) {
  console.log("i is " + i);
}

for (let i = 0; i < myList.length; i++) {
  alert("I have " + myList[i] + " in my shopping bag");
}
```

### 8. Remove first item

```js
fruits.shift()
```

---
---
---


## Dates

### 1. Get current time

```js
let now = new Date();
```

### 2. Create a date

```js
let date = Date.parse("01 Jan 2025 00:00:00 GMT");
```

### 3. Get date data

```js
let now = new Date();
now.getMinutes(); // 0,1,2, 12
now.getHours(); //1, 2, 3, 4
now.getDate(); //1, 2, 3, 4
now.getDay(); // 0, 1, 2
now.getMonth(); // 0, 1, 2
now.getFullYear(); // 2021
```

---
---
---


## Numbers

### 1. Round

```js
Math.round(4.7) // 5
```

### 2. Floor

```js
Math.floor(4.7) // 4
```

### 3. Ceil

```js
Math.ceil(4.7) // 5
```

### 4. Min

```js
Math.min(2, 5, 1) // 1
```

### 5. Max

```js
Math.max(2, 5, 1); // 5
```

### 6. Random

```js
Math.random(); // 0.47231881595639025
```


---
---
---


## Objects

### 1. Creating a new object

```js
let fruit = new Object(); // "object constructor" syntax

let user = {}; // "object literal" syntax

let student = {
  firsName: "Julie",
  lastName: "Johnson",
};

let anotherStudent = {
  firstName: "Kate",
  lastName: "Robinson",
  female: true,
  greet: function () {
    alert("Hey");
  },
};
```

### 2. Reading an object properties

```js
let user = {
  firstName: "Lady",
  lastName: "Gaga",
  gender: "female",
};

alert(user.firstName); // Lady
alert(user.lastName); // Gaga

// or
alert(user["firstName"]); // Lady
alert(user["lastName"]); // Gaga
```

### 3. Adding object properties

```js
let user = {
  firstName: "Lady",
  lastName: "Gaga",
  gender: "female",
};

user.profession = "Singer";
```

### 4. Object Arrays

```js
let users = [
  {
    firstName: "Bradley",
    lastName: "Cooper",
  },
  {
    firstName: "Lady",
    lastName: "Gaga",
  },
];

users.forEach(function (user, index) {
  for (let prop in user) {
    alert(prop + " is " + user[prop]);
  }
});
```

### 5. Enumerating the properties of an object

```js
let user = {
  firstName: 'Lady',
  lastName: 'Gaga',
  gender: 'female'
}


for(let prop in user) {
  alert(prop); // firstName, lastName, gender
  alert(user[prop]); // 'Lady', 'Gaga', 'female'
}
```

---
---
---


## Functions

### 1. JS Functions

```js
function sayFact() {
  let name = prompt("What's your name?");

  if (name === "Sofia") {
    alert("Your name comes from the Greek -> Sophia");
  }
}

sayFact();

// Piece of code that does one or more actions
```

### 2. JS Functions Parameters

```js
function fullName(firstName, lastName) {
  alert(firstName + " " + lastName);
}

let firstName = prompt("What's your first name?");
let lastName = prompt("What's your last name?");
fullName(firstName, lastName);
fullName("Kate", "Robinson");
```

### 3. JS Functions Return

```js
function add(x, y) {
  return x + y;
}

let result = add(3, 4);
let result2 = add(result, 0);


function getFullName(firstName, lastName) {
  let fullName = firstName + " " + lastName;
  return fullName;
}

let userFullName = getFullName("Kate", "Robinson");
alert(userFullName); // Kate Robinson
alert(getFullName("Julie", "Smith")); // Julie Smith
```

### 4. Closures

```js
function hello() {
  function go(name) {
    alert(name);
  }

  let name = "SheCodes";
  go(name);
}

hello();
```

---
---
---


## Debugging

### 1. Console.log

```js
console.log(name);
console.log("Let's code!");

// Outputs a message to the web console.
```


---
---
---


## Selectors

### 1. QuerySelector

```js
let li = document.querySelector("li");
let day = document.querySelector(".day");
let paragraph = document.querySelector("ul#list p");
```

### 2. QuerySelectorAll

```js
let lis = document.querySelectorAll("li");
let paragraphs = document.querySelectorAll("li#special p");
```


---
---
---


## Events

### 1. Creating an event listener

```js
function sayHi() {
  alert("hi");
}

let element = document.querySelector("#city");
element.addEventListener("click", sayHi);
```

### 2. setTimeout

```js
function sayHello() {
  alert('Hello')
}
setTimeout(sayHello, 3000);
```

### 3. setInterval

```js
function sayHello() {
  alert('Hello')
}
setInterval(sayHello, 3000);
```


---
---
---


## AJAX

### 1. AJAX with Fetch

```js
let root = 'https://jsonplaceholder.typicode.com'
let path = 'users/1'

fetch(root + '/' + path)
  .then(response => (
    response.json()
  ))
  .then(json => (
    console.log(json)
  ));
```

### 2. AJAX with Axios

```js
<!DOCTYPE html>
<html>
  <head>
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  </head>
  <body>
    <script>
      function showUser(response) {
        alert(`The user name is ${response.data.name}`);
      }

      let url = "https://jsonplaceholder.typicode.com/users/1";
      axios.get(url).then(showUser);
    </script>
  </body>
</html>
```

---
---
---


## Element manipulation

### 1. HTML classes

```js
let li = document.querySelector("li#special");
li.classList.remove("liked");
li.classList.add("something");

// Update the element class names.
```

### 2. HTML content

```js
let li = document.querySelector("li");
li.innerHTML = "Hello World";

// Update the HTML content of the selected element.
```

### 3. Forms

```js
<form>
  <input type="text" id="email" />
</form>
<script>

function signUp(event) {
  event.preventDefault();
  let input = document.querySelector("#email");
  console.log(input.value);
}
let form = document.querySelector("form");
form.addEventListener("submit", signUp);
</script>

// Note: The event will be triggered by clicking the button or pressing enter.
```

### 4. HTML Attributes Manipulation

```js
let button = document.querySelector("input#button");
button.setAttribute("disabled", "disabled");

let email = document.querySelector("input#email");
email.removeAttribute("required");

// Update the element attributes
```

### 5. CSS Styles

```js
let boxElement = document.querySelector("#box");
boxElement.style.backgound = "red";
boxElement.style.padding = "10px 20px";
boxElement.style.marginRight = "10px";

// Changes the CSS style of an element.
// Note: We recommend using classList instead
```


---
---
---


## APIs

### 1. Geolocation API

```js
function handlePosition(position) {
  console.log(position.coords.latitude);
  console.log(position.coords.longitude);
}

navigator.geolocation.getCurrentPosition(handlePosition)

// The Geolocation API allows the user to provide their location to web applications if they so desire. For privacy reasons, the user is asked for permission to report location information.
```

---
---
---