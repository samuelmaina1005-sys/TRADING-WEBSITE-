# TRADING-WEBSITE-
my first trading platform 
index.html<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>My Trading Platform</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #111827;
            color: white;
        }

        header {
            padding: 20px;
            background: #1f2937;
            display: flex;
            justify-content: space-between;
        }
Create trading dashboard
        .container {
            padding: 20px;
        }

        .balance {
            font-size: 20px;
            margin-bottom: 20px;
        }

        .chart {
            height: 350px;
            background: #0f172a;
            border: 1px solid #374151;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }

        .price {
            font-size: 28px;
            margin-bottom: 15px;
        }

        input {
            padding: 12px;
            width: 120px;
            margin-bottom: 15px;
        }

        button {
            padding: 14px 30px;
            border: none;
            color: white;
            font-weight: bold;
            cursor: pointer;
            margin-right: 10px;
        }

        .buy {
            background: green;
        }

        .sell {
            background: red;
        }

        table {
            width: 100%;
            margin-top: 30px;
            border-collapse: collapse;
        }

        th, td {
            padding: 12px;
            border-bottom: 1px solid #374151;
            text-align: left;
        }
    </style>
</head>

<body>

<header>
    <strong>My Trading Platform</strong>
    <span>Balance: $10,000</span>
</header>

<div class="container">

    <h2>BTC/USD</h2>

    <div class="price">
        $65,000
    </div>

    <div class="chart">
        📈 CHART WILL GO HERE
    </div>

    <h3>Place Trade</h3>

    <label>Quantity</label><br>

    <input type="number" id="quantity" value="0.01">

    <br>

    <button class="buy" onclick="buy()">BUY</button>

    <button class="sell" onclick="sell()">SELL</button>

    <h3>Trade History</h3>

    <table>
        <tr>
            <th>Type</th>
            <th>Asset</th>
            <th>Quantity</th>
            <th>Price</th>
        </tr>

        <tbody id="trades"></tbody>
    </table>

</div>

<script>

function buy() {

    let quantity =
        document.getElementById("quantity").value;

    addTrade("BUY", quantity);

}

function sell() {

    let quantity =
        document.getElementById("quantity").value;

    addTrade("SELL", quantity);

}

function addTrade(type, quantity) {

    let table =
        document.getElementById("trades");

    let row = table.insertRow();

    row.innerHTML =
        `<td>${type}</td>
         <td>BTC/USD</td>
         <td>${quantity}</td>
         <td>$65,000</td>`;

}

</script>

</body>
</html>