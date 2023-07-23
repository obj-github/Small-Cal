<!DOCTYPE html>

<html>
<head>
  <link rel="icon" type="image/gif" href="https://lordicon.com/icons/wired/lineal/1541-education-mathematics-abacus.gif">
  <meta http-equiv="CONTENT-TYPE" content="text/html; charset=UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello, World!</title>
  <script src="https://cdn.lordicon.com/bhenfmcm.js"></script>
  <style>
  body{
    background-color:#0F0F0F;
    align-items:center;
    display:block;
  }

  
  h1, h2{
    color: #FFFFFF;
    border-radius:8px;
    padding:12px;
    display:inline-block;
  }
  
  input{
    padding:10px;
    border-radius:9px;
    border:2px;
    display: block;
    align-content:center;
    width:80%;
    font-weight: bold;
    font-size:16px;
  }
  
  div{
    align-content:center;
  }
  
  button{
    background-color:green;
    color:#FFFFFF;
    font-size:20px;
    font-weight:bold;
    border:6px;
    border-radius:5px;
    padding:15px;
    width:60%;
  }

  p{
    color:#FFFFFF;
    font-size: 18px;
    font-weight:bold;
  }

lord-icon{
  height:50px;
  width:50px;
}
.logo{
  height:70px;
  widht:70px;
  background-color:#FFFFFF;
  border-radius:50%;
  display:inline-block;
}

.icon{
  height:50px;
  widht:50px;
  border-radius:50%;
  background-color:#F0F0F0;
}
  </style>
</head>
<body>
  <header>
  <img class="logo" src="https://lordicon.com/icons/wired/lineal/1541-education-mathematics-abacus.gif">
    <h1>Calculator Box</h1>
  </header>
  
    <center>
  <div>
  <h2 class="hquad">
    Balance the Equation <img class="icon"src="https://lordicon.com/icons/wired/flat/402-legal-balance-legal.gif"/>
  </h2>
  <p>Quadratic Equation e.g. 6x² + 11x - 35 = 0</p>
  <div class="equation">
    <input type="number" id="quad-a" placeholder="6" value=""/>
    <br />
        <input type="number" id="quad-b" placeholder="11" value=""/>
    <br />
        <input type="number" id="quad-c" placeholder="-35" value=""/>
    
    <p id="quad"> </p>
    
    <button onclick="quadraticEquation()">Solve</button>
  </div>
  </div>
  <br />
  
  <div>
    <h2>
    Modular Arithmetic <img class="icon" src="https://lordicon.com/icons/wired/lineal/1879-countdown.gif"/>
  </h2>
  <p></p>
    <input type="number" id="mod1" placeholder="Number e.g. 5"/>
    <br />
        <input type="number" id="mod2" placeholder="Mod e.g. 2"/>
    
    <p id="modout"></p>
    <button onclick="modularArithmetic()"> calculate</button>
  </div>
  <br />
  
  <div>
    <h2>
    Area of Circle <lord-icon src="https://cdn.lordicon.com/hrkhavyt.json"></lord-icon>
  </h2>
    <p>Enter only value of radius, r</p>
    <input type="number" id="radius" placeholder="5"/>
    <p id="area-value"></p>
    <p id="circumference"></p>
    <button onclick = "circle()">Calculate</button>
  </div>
  <br />
  
  <div>
    <h2>
    Simple Interest <img class="icon" src="https://lordicon.com/icons/wired/lineal/2367-loan.gif"/>
  </h2>
  
    <input type="number" id="sp" placeholder="Principal e.g. 5000"/>
    <br />
        <input type="number" id="sr" placeholder="Rate e.g. 50%"/>
    <br />
        <input type="number" id="st" placeholder="Time e.g. 1year"/>
    <br />
    <p id="interest"></p>
    <button onclick="simpleInterest()">Calculate</button>
  </div>
  <br />
  </center>
  
  <script>
  //Quadratic Equation//
  
  function quadraticEquation(){
    let a = document.getElementById("quad-a").value;
    let b = document.getElementById("quad-b").value;
    let c = document.getElementById("quad-c").value;
    let cal1 = Math.sqrt(b**2-4*a*c);
    let cal2 = (-b + cal1)/2*a;
    let cal3 = (-b - cal1)/2*a;
    let result = `x = ${cal2} or ${cal3}`;
    let p = document.getElementById(`quad`);
    p.innerHTML = `the result is ` + result;
  }
  
  //Modular Arithmetics//
  
  function modularArithmetic(){
    const num = document.getElementById(`mod1`).value;
    const mod = document.getElementById(`mod2`).value;
    const mode = num % mod;
    const modoutput = document.getElementById(`modout`);
    modoutput.innerHTML = mode;
  }
  
  //Area of Circle//
  
  function circle(){
    let radius = document.getElementById(`radius`).value;
    let area = 3.142*radius**2;
    let perimeter = 2*3.142*radius;
    let r1 = document.getElementById(`area-value`);
   let p1 =  document.getElementById(`circumference`);
  
  r1.innerHTML = `Area = ${area}`;
  p1.innerHTML = `Circumference =  ${perimeter}`;
  }
  
  //simple interest//
  
  function simpleInterest(){
    let principal = document.getElementById(`sp`).value;
    let rate = document.getElementById(`sr`).value;
    let time = document.getElementById(`st`).value;
    let simpleinterest = (principal*rate*time)/100;
    let si = document.getElementById(`interest`);
    si.innerHTML = `Interest = ` + simpleinterest;
  }
  
  </script>
</body>
</html>
