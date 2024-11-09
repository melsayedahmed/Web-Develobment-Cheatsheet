# ********************* React Cheatsheet *********************

## JSX


### 1. JSX Element

Define simple JSX elements with HTML-like syntax.

```jsx
let element = <h1>Hello, world!</h1>;
let emptyHeading = <h1 />;
```


### 2. JSX Expressions

Embed JavaScript expressions in JSX using curly braces `{}`.

```jsx
let name = 'Josh Perez';
let element = <h1>Hello, {name}</h1>;

function fullName(firstName, lastName) {
  return firstName + ' ' + lastName;
}
let element = <h1>Hello, {fullName('Julie', 'Johnson')}</h1>;
```


### 3. JSX Attributes

JSX attributes use camelCase, and `class` becomes `className`.

```jsx
const element = <img src={user.avatarUrl} />;
const element = <button className="btn">Click me</button>;

/* Note: Use "className" instead of "class" */
```


### 4. JSX Functions

Functions can be used directly in JSX for dynamic rendering.

```jsx
function name() {
  return "Julie";
}

return (
  <h1>
    Hi {name()}!
  </h1>
);
```

### 5. JSX Conditional Rendering

Use conditional logic to render different elements based on props.

```jsx
import React from "react";

export default function Weather(props) {
  if (props.temperature >= 20) {
    return (
      <p>
        It is {props.temperature}°C (Warm) in {props.city}
      </p>
    );
  } else {
    return (
      <p>
        It is {props.temperature}°C in {props.city}
      </p>
    );
  }
}
```

---
---
---

## Components


### 1. Functional component

```jsx
import React from 'react';

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <div>Hello</div>  
        <div>World</div>
      </div>
  );
}
/* Note: Every component needs one root element */
```

### 2. Embed an internal component

```jsx
import React from 'react';
import UserAvatar from "./UserAvatar";

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <UserAvatar />
        <UserAvatar />
      </div>
  );
}
/* Note: Assuming UserAvatar is declared in UserAvatar.js */
```

### 3. Embed an external component

```jsx
import React from 'react';
import ComponentName from 'component-name';

export default function UserProfile() {
  return (
      <div className="UserProfile">
        <ComponentName />
      </div>
  );
}
/* Note: External components are found on npmjs.com and need to be imported first. */
```

### 4. Advanced functional component

```jsx
import React from "react";

export default function Hello(props) {
  function fullName() {
    return `${props.firstName} ${props.lastName}`;
  }
  return (
    <p>
      {fullName()}
    </p>
  );
}


<Hello firstName="Matt" lastName="Delac" />
```

---
---
---

## Properties


### 1. Passing properties to a component

```jsx
<Student firstName="Julie" lastName="Johnson" age={23} pro={true} />
```

### 2. Accessing the properties from a component

```jsx
import React from "react";

export default function Student(props) {
  return (
    <h1>
      {props.firstName} {props.lastName} is {props.age}.
    </h1>
  )
}
```

---
---
---

## CSS


### 1. CSS in a React Component

```jsx
import React from "react";
import "./Student.css";

export default function Student() {
  return (
    <div className="Student">
      Julie Johnson
    </div>
  )
}

/* Note: You'll then have to crate a css file called Student.css */
```

---
---
---

## Events


### 1. Event listener

```jsx
import React from "react";

export default function Hello() {
  function handleClick(event) {
    event.preventDefault();
    alert("Hello World");
  }

  return (
    <a href="/" onClick={handleClick}>
      Say Hi
    </a>
  );
}

/* Note: The most common event listeners are onClick for links/buttons and onSubmit for forms */
```

---
---
---

## States


### 1. React state

```jsx
import React, { useState } from "react";

export default function Hello(props) {
  let [name, setName] = useState("Julie");
  function updateName() {
    let newName = prompt("What is your name?");
    setName(newName);
  }

  return (
    <div>
      <h1>
        {name}
      </h1>
      <button onClick={updateName}>
        Update name
      </button>
    </div>
  );
}
```

---
---
---


## Forms


### 1. React forms

```jsx
import React, { useState } from "react";

export default function LoginForm() {
  let [username, setUsername] = useState("");
  let [password, setPassword] = useState("");

  function handleSubmit(event) {
    event.preventDefault();
    alert(`Loging in with ${username} and ${password}`);
  }

  function updateUsername(event) {
    setUsername(event.target.value);
  }

  function updatePassword(event) {
    setPassword(event.target.value);
  }

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" placeholder="Username" onChange={updateUsername} />
      <input type="password" placeholder="Password" onChange={updatePassword} />
      <input type="submit" value="Login" />
    </form>
  );
}
```

---
---
---

## Loops


### 1. Looping through an array

```jsx
let elements = ['one', 'two', 'three'];

return (
  <ul>
    {elements.map(function(value, index) {
      return <li key={index}>{value}</li>
    })}
  </ul>
);
/* Note: Each list item inside a map loop needs a key attribute with a unique value which is generally the index. */
```


### 2. Looping through an array of objects

```jsx
let elements = [
  {
    name: "one",
    value: 1,
  },
  {
    name: "two",
    value: 2,
  },
  {
    name: "three",
    value: 3,
  },
];
return (
  <ul>
    {elements.map(function (element, index) {
      return (
        <li key={index}>
          The value for {element.name} is {element.value}
        </li>
      );
    })}
  </ul>
);
/* Note: Each list item inside a map loop needs a key attribute with a unique value which is generally the index. */
```

---
---
---

## AJAX


### 1. AJAX Request with Axios

```jsx
import React from "react";
import axios from "axios";

export default function Weather(props) {
  function handleResponse(response) {
    console.log(response);
  }
  
  if (notifications) {
    return (
      <p>
        notifications
      </p>
    );
  } else {
    let url = `https://notifications.com`;
    axios.get(url).then(handleResponse);
    return <p>Loading notifications..</p>;
  }
}
/* Note: Make sure to import Axios first to your project. */
```
---
---
---