# sinh
draft for numerical analysis project
<!DOCTYPE html>
<html>
<head>
	<title>Hyperbolic Function Calculator</title>
</head>
<body>
	<h1>Hyperbolic Function Calculator</h1>

	<label for="x">Enter the value of x:</label>
	<input type="number" id="x" name="x"><br><br>

	<label for="n">Enter the number of decimal places:</label>
	<input type="number" id="n" name="n"><br><br>

	<button onclick="calculate()">Calculate</button>

	<p id="result"></p>

	<script>
		function calculate() {
			var x = parseFloat(document.getElementById("x").value);
			var n = parseInt(document.getElementById("n").value);
			var numerator = Math.exp(x) - Math.exp(-x);
			var denominator = 2;
			var result = numerator / denominator;
			var roundedResult = result.toFixed(n);
			var choppedResult = Math.floor(result * Math.pow(10, n)) / Math.pow(10, n);
			document.getElementById("result").innerHTML = "Rounded Result: " + roundedResult + "<br>Chopped Result: " + choppedResult;
		}
	</script>
</body>
</html>
