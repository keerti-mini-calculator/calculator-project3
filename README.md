# calculator-project
<!DOCTYPE html>
<html>
<head>
<title>Simple Calculator</title>
<style>
body{
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    background:#f2f2f2;
}
.calculator{
    background:white;
    padding:20px;
    border-radius:10px;
    box-shadow:0 0 10px gray;
}
#display{
    width:100%;
    height:40px;
    margin-bottom:10px;
    font-size:20px;
}
button{
    width:50px;
    height:50px;
    font-size:18px;
    margin:5px;
}
</style>
</head>
<body>

<div class="calculator">
<input type="text" id="display" disabled><br>

<button onclick="clearDisplay()">C</button>
<button onclick="append('7')">7</button>
<button onclick="append('8')">8</button>
<button onclick="append('9')">9</button><br>

<button onclick="append('4')">4</button>
<button onclick="append('5')">5</button>
<button onclick="append('6')">6</button>
<button onclick="append('+')">+</button><br>

<button onclick="append('1')">1</button>
<button onclick="append('2')">2</button>
<button onclick="append('3')">3</button>
<button onclick="append('-')">-</button><br>

<button onclick="append('0')">0</button>
<button onclick="append('*')">*</button>
<button onclick="append('/')">/</button>
<button onclick="calculate()">=</button>

</div>

<script>
function append(value){
    document.getElementById("display").value += value;
}
function clearDisplay(){
    document.getElementById("display").value = "";
}
function calculate(){
    document.getElementById("display").value = 
    eval(document.getElementById("display").value);
}
</script>

</body>
</html>
