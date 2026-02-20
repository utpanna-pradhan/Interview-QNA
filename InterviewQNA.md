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
# Q28. Largest Number
function maxnum(arr){
    let max = arr[0];
    for(let i=0;i<=arr.length;i++){
        if(arr[i]>max){
            max = arr[i]
        }
    }
    return max;
}
console.log(maxnum([3,7,2,9,5]));

# Q29. Remove duplicate
```javascript
function removedub(arr){
const result = [];
for(let i=0;i<=arr.length;i++){
    if(!result.includes(arr[i]))
    {
        result.push(arr[i])
    }
}
return result;
}
console.log(removedub([1,2,2,3,4,4,5]))
```

# 30. Add item to list in react
```javascript
import {useState} from "react";
function ItemList(){
    const [ txt,setTxt ] = useState(" ");
    const [items,setItems] = useState([]);
    const handleAdd = () =>{
        if(items.trim=="")return;
        setItems([...items,txt])
        setTxt("")
    }
    return(<>
    <input type ="text" onChange={(e)=>setTxt(e.target.value)}/>
    <button onClick = {handleAdd}> Add </button>
    <ul>
    {items.map((index,item)=>(
        <li key = {index}>{item}</li>
    ))}
    </ul> 
        </>
    )
}
```

# 31. What happen after rerender?
- State update.
- component function runs again.
- new virtual dom created.
- diffing algorithmn compares old vs new dom.
- real dom updates minimal changes

# 32. post method /add
```javascript
const express = require("express");
const app = express();
app.use(express.json());
app.post("/add",(req,res)=>{
    const {a,b} = req.body;
    res.json ({result : a+b})
});
const PORT = process.env.PORT || 8000;
app.listen(PORT,()=>{
    console.log(`server is running on PORT ${PORT}`)
})
```

# 33.Middleware
It is a function that runs before route handle
- req = incoming request
- res = response
- next = passes control to next middle ware

# 34.sync vs async
sync = Blocks execution
async = non blocking ,handle via callback,promises,event loop

# 35. Double everynumber
```javascript
const numbers = [1,2,3,4];
const dblnum = numbers.map((num)=>{
    return num * 2
})
console.log(dblnum)
```

# 36.Square of each number
```javascript
const numbers = [1,2,3];
const sqrnum = numbers.map((num)=>{
    return num*num;
})
console.log(sqrnum)
```