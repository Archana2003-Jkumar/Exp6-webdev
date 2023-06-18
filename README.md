# Exp6-webdev
# Simple calculator 
## Aim:
To develop a simple calculator using React. 
## Algorithm:
1. Code all the necessary Css elements.
2. And connect it with the HTML page.
3. Then execute it.
4. Display the results.
## Code:
```
App.js

import React, { useState } from 'react';
import './App.css';

function App() {
  const [result, setResult] = useState('');

  const handleClick = (e) => {
    setResult(result.concat(e.target.name));
  };

  const handleClear = () => {
    setResult('');
  };

  const handleCalculate = () => {
    try {
      setResult(eval(result).toString());
    } catch (error) {
      setResult('Error');
    }
  };

  return (
    <body>
      <p>SIMPLE CALCULATOR</p>
      <div className="calculator">
        <input type="text" value={result} readOnly />
        <div className="keypad">
          <button name="7" onClick={handleClick}>7</button>
          <button name="8" onClick={handleClick}>8</button>
          <button name="9" onClick={handleClick}>9</button>
          <button className="operator" name="/" onClick={handleClick}>&divide;</button>
          <button name="4" onClick={handleClick}>4</button>
          <button name="5" onClick={handleClick}>5</button>
          <button name="6" onClick={handleClick}>6</button>
          <button className="operator" name="*" onClick={handleClick}>&times;</button>
          <button name="1" onClick={handleClick}>1</button>
          <button name="2" onClick={handleClick}>2</button>
          <button name="3" onClick={handleClick}>3</button>
          <button className="operator" name="-" onClick={handleClick}>&ndash;</button>
          <button name="0" onClick={handleClick}>0</button>
          <button name="." onClick={handleClick}>.</button>
          <button className="operator" id="equals" onClick={handleCalculate}>=</button>
          <button className="operator" name="%" onClick={handleClick}>%</button>
          <button className="operator clear" onClick={handleClear}>Clear</button>
        </div>
      </div>
    </body>
  );
}

export default App;
```
```
App.css
.calculator {
  width: 300px;
  margin: 50px auto;
  background-color: #3da9bc;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(172, 179, 255, 0.99);
}
body{
  background-color: rgb(154, 192, 225);
  margin:200px;
}
p{
  color:rgba(255, 255, 255, 0.848);
  text-align:center;
  font-size:40px;
  font-weight:700;
}

input[type="text"] {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  font-size: 18px;
  padding: 5px;
}

.keypad {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 5px;
}

button {
  width: 100%;
  height: 40px;
  font-size: 18px;
  border: none;
  background-color: #fff;
  cursor: pointer;
}

.operator {
  background-color: #c55585;
  color: #000000;
}

#equals {
  background-color: #795278;
  color: #fff;
}
.operator.clear {
  grid-column: span 4;
}
```
## Output:
![image](https://github.com/Archana2003-Jkumar/Exp6-webdev/assets/93427594/14a1587b-0960-4693-b481-eb23307e6271)
![image](https://github.com/Archana2003-Jkumar/Exp6-webdev/assets/93427594/e635ee78-4d1e-4e47-8326-21d567d6a87c)

## Result:
Thus the code has been implemented successfully.
