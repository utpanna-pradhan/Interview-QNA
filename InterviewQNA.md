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