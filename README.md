# TaxProject2
This is Project2
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tax Payment Platform</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            margin-top: 50px;
        }

        .input-group {
            margin-bottom: 15px;
        }

        .input-group label {
            display: block;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .input-group input[type="text"] {
            width: 100%;
            padding: 8px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .input-group button {
            background-color: #4caf50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }

        .input-group button:hover {
            background-color: #45a049;
        }

        .result {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="input-group">
            <label for="income">Enter your income:</label>
            <input type="text" id="income">
        </div>
        <div class="input-group">
            <button onclick="calculateTax()">Calculate Tax</button>
        </div>
        <div class="result" id="taxResult"></div>
    </div>

    <script>
        function calculateTax() {
            var income = document.getElementById("income").value;
            var tax = 0;
            if (income <= 50000) {
                tax = 0.1 * income;
            } else if (income <= 100000) {
                tax = 0.2 * income;
            } else {
                tax = 0.3 * income;
            }

            document.getElementById("taxResult").textContent = "Tax to be paid: $" + tax.toFixed(2);
        }
    </script>
</body>

</html>
