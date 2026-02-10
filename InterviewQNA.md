# Q1
Task:
Create a React component that:
Shows text: "Hello MERN"
Has a button
On button click, text should toggle (show / hide)
Rules:
Use useState
Keep code simple
No styling needed

ans: 
```javascript
import {useState} from "react"

function ToggleText(){
    const[show , setShow] = useState(true)
    return(
        <div>
        <button onClick = {()=>setShow(!show)}>
        Toggle</button>
        {show && <h1>Hello MERN</h1>}
        </div>
    )
}
```

# Q2. 
Task:Create an Express GET API /status that returns this JSON:{ "server": "running" }

ans:
```javascript
const express = require("express")
const app = express();

app.get("/status",(req,res)=>{
    res.json({server:"running"})
})
const PORT = process.env.PORT || 8000
app.listen(PORT,()=>{
    console.log(`Server is running on port ${PORT})
})
```

# Q3. What is the difference between frontend and backend?
ans:

Frontend handles the user interface and user interactions in the browser. Backend handles server-side logic, data storage, and APIs which are not directly visible to users.


# Q4.Even Numbers (Without .filter())
ans:
 ```javaScript
 const numbers = [1,2,3,4,5,6];

function getEvenNumbers(arr){
    const result = [];
    for(let i = 0; i < arr.length; i++){
        if(arr[i] % 2 === 0){
            result.push(arr[i]);
        }
    }
    return result;
}

console.log(getEvenNumbers(numbers));
```

# Q5. React Counter
ans :
 
 ```javascript
 import React, { useState } from "react";

function Counter() {
    const [count, setCount] = useState(0);

    return (
        <>
            <button onClick={() => setCount(count + 1)}>
                Increase
            </button>
            <p>Counter: {count}</p>
        </>
    );
}

export default Counter;
```

# Q6. State Update Explanation
ans:
- State updates using setState / setCount
- React schedules a re-render
- Component function runs again
- New Virtual DOM is created
- React compares old and new Virtual DOM (diffing)
- Only changed parts are updated in real DOM
- UI updates efficiently

# Q7.app.use vs app.get
ans:

app.get()
- Used to handle GET requests
- Specific route
- Example: app.get("/users", handler)

app.use()
- Used for middleware
- Runs before routes
- Can apply globally or for specific path
- Example: app.use(express.json())

Important:
app.use() works for ALL HTTP methods.

# Q8.Closure
Closure is when an inner function remembers and accesses variables from its outer function scope even after the outer function has executed.

# Q9.Middleware
Middleware is a function that has access to req, res, next and runs before the request reaches the route handler.

# Q10.
