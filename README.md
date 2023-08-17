# unit-converter
 Unit Converter application that converts metric units to imperial units using HTML and CSS:
 <!DOCTYPE html>
<html>
<head>
<title>Unit Converter</title>
<style>
body {
  font-family: sans-serif;
}

.container {
  width: 500px;
  margin: 0 auto;
}

.section {
  margin-bottom: 20px;
}

.input-group {
  display: flex;
  justify-content: space-between;
}

.input-group input {
  width: 100px;
}

.button {
  background-color: #000;
  color: #fff;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}
</style>
</head>
<body>
<div class="container">
  <h1>Unit Converter</h1>

  <div class="section">
    <h2>Temperature</h2>
    <div class="input-group">
      <input type="number" placeholder="Celsius" id="celsius">
      <button id="convert-temperature">Convert</button>
    </div>
    <p id="fahrenheit"></p>
  </div>

  <div class="section">
    <h2>Weight</h2>
    <div class="input-group">
      <input type="number" placeholder="Kilograms" id="kilograms">
      <button id="convert-weight">Convert</button>
    </div>
    <p id="pounds"></p>
  </div>

  <div class="section">
    <h2>Distance</h2>
    <div class="input-group">
      <input type="number" placeholder="Kilometers" id="kilometers">
      <button id="convert-distance">Convert</button>
    </div>
    <p id="miles"></p>
  </div>
</div>

<script>
function convertTemperature() {
  const celsius = document.getElementById("celsius").value;
  const fahrenheit = celsius * 1.8 + 32;
  document.getElementById("fahrenheit").innerHTML = fahrenheit;
}

function convertWeight() {
  const kilograms = document.getElementById("kilograms").value;
  const pounds = kilograms * 2.20462262185;
  document.getElementById("pounds").innerHTML = pounds;
}

function convertDistance() {
  const kilometers = document.getElementById("kilometers").value;
  const miles = kilometers * 0.621371192;
  document.getElementById("miles").innerHTML = miles;
}

document.getElementById("convert-temperature").addEventListener("click", convertTemperature);
document.getElementById("convert-weight").addEventListener("click", convertWeight);
document.getElementById("convert-distance").addEventListener("click", convertDistance);
</script>
</body>
</html>

