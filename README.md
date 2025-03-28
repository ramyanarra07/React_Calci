# Ex04 Simple Calculator - React Project
## Date:28-03-2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
DEVELOPED BY : NARRA RAMYA
REG NO: 212223040128

##APP.JS
```
import React, { useState } from "react";
import "./App.css";

const App = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const deleteLast = () => {
    setInput((prev) => prev.slice(0, -1));
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
        <button className="operator" onClick={() => handleClick("%")}>%</button>
        <button className="operator" onClick={() => handleClick("/")}>÷</button>
        <button className="operator" onClick={deleteLast}>⌫</button>
        <button className="operator" onClick={clearInput}>AC</button>
        <button onClick={() => handleClick("7")}>1</button>
        <button onClick={() => handleClick("8")}>2</button>
        <button onClick={() => handleClick("9")}>3</button>
        <button className="operator" onClick={() => handleClick("*")}>×</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button className="operator" onClick={() => handleClick("-")}>−</button>

        <button onClick={() => handleClick("1")}>7</button>
        <button onClick={() => handleClick("2")}>8</button>
        <button onClick={() => handleClick("3")}>9</button>
        <button className="operator" onClick={() => handleClick("+")}>+</button>

        <button className="zero" onClick={() => handleClick("0")}>  0  </button>
        <button onClick={() => handleClick(".")}>.</button>
        <button className="equal" onClick={calculateResult}>=</button>
      </div>
    </div>
  );
};

export default App;
```

##APP.CSS
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-image: url('ramya.jpg'); 
  background-size: cover; 
  background-position: center; 
  font-family: Arial, sans-serif;
}


.calculator {
  width: 320px;
  background: gray;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.display {
  width: 100%;
  height: 80px;
  background: rgb(42, 41, 41);
  color: white;
  font-size: 2.5em;
  text-align: right;
  padding: 15px;
  border-radius: 10px;
  margin-bottom: 10px;
  font-weight: bold;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  width: 100%;
  height: 60px;
  font-size: 1.8em;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  transition: 0.2s;
  background: ivory;
  color: black;
}

button:hover {
  background: #555;
}

.operator {
  background: rgb(239, 201, 125);
}

.operator:hover {
  background: lightcyan;
}

.equal {
  background: rgb(182, 221, 235);
  border-radius: 50%;
}

.equal:hover {
  background: ivory;
}

.zero {
  grid-column: span 2;
  border-radius: 40px;
  text-align: left;
  padding-left: 30px;
}
```


## OUTPUT
![Screenshot (152)](https://github.com/user-attachments/assets/f3857440-6701-4f6a-ad79-a2e9a04b2d2c)

![Screenshot (151)](https://github.com/user-attachments/assets/8cd1efb4-321e-4015-b24b-0ed5e6375fea)
![Screenshot (149)](https://github.com/user-attachments/assets/b61dc8ee-1459-4bb6-9f77-4797c744c84a)



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
