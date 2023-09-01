# Temperature-convert-
Bharat Intern project 1
Tempracher coveter TARUN YEWALE [23/08/2023]<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Temperature Converter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      
      border-image-width: auto;
    }
    .container {
      
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
      background-color: #139fdf;
      box-shadow: 0 0 10px rgba(212, 12, 12, 0.2);
      justify-content: center;
      
    }
    
    h1 {
      color: #0f0a0a;
    }
    input[type="number"] {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      box-sizing: border-box;
    }
    select {
      width: 100%;
      padding: 10px;
      margin-bottom: 10px;
      box-sizing: border-box;
    }
    button {
      background-color: #ee1597;
      color: #fff;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
    .result {
      font-size: 20px;
      font-weight: bold;
      margin-top: 20px;
    }
    #a{
      height: 100%;
      width: 100%;
      display: flex;
      scroll-behavior:auto;
    }
  </style>
</head>
<body>
  
  
  <div class="container">
    
    <h1>Temperature Converter</h1>
    <label for="temperature">Enter temperature:</label>
    <input type="number" id="temperature" placeholder="Enter temperature" required>
    <select id="unit">
      <option value="celsius">Celsius (°C)</option>
      <option value="fahrenheit">Fahrenheit (°F)</option>
    </select>
    <button onclick="convertTemperature()">Convert</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    function convertTemperature() {
      const temperature = parseFloat(document.getElementById("temperature").value);
      const unit = document.getElementById("unit").value;
      let convertedTemperature;

      if (unit === "celsius") {
        convertedTemperature = (temperature * 9/5) + 32;
      } else {
        convertedTemperature = (temperature - 32) * 5/9;
      }
      document.getElementById("result").textContent = `Converted temperature: ${convertedTemperature.toFixed(2)} °${unit === "celsius" ? "F" : "C"}`;
    }
  </script>
</body>
</html>
