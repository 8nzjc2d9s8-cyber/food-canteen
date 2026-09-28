# index.html
<! DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Food Canteen Management System</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: auto;
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        h1 {
            text-align: center;
            color: #333;
        }

        h2 {
            color: #444;
        }

        .customer {
            margin-bottom: 20px;
        }

        input, select, button {
            padding: 10px;
            margin: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        input {
            width: 90%;
        }

        button {
            background-color: #333;
            color: white;
            cursor: pointer;
        }

        button:hover {
            background-color: #555;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

        th, td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: center;
        }

        th {
            background-color: #333;
            color: white;
        }

        .total {
            text-align: right;
            font-size: 20px;
            font-weight: bold;
            margin-top: 20px;
        }

        .receipt {
            margin-top: 25px;
            padding: 20px;
            background-color: #f9f9f9;
            border: 1px solid #ddd;
        }

        .hidden {
            display: none;
        }
    </style>
</head>

<body>

<div class="container">

    <h1>FOOD CANTEEN MANAGEMENT SYSTEM</h1>

    <div class="customer">
        <h2>Customer Information</h2>

        <label>Customer Name:</label><br>

        <input
            type="text"
            id="customerName"
            placeholder="Enter customer name"
        >
    </div>

    <h2>Food Menu</h2>

    <table>
        <thead>
            <tr>
                <th>Food</th>
                <th>Price</th>
                <th>Quantity</th>
                <th>Add</th>
            </tr>
        </thead>

        <tbody id="menuTable">

            <tr>
                <td>White Rice</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty1" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('White Rice', 200, 'qty1')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Jollof Rice</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty2" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Jollof Rice', 200, 'qty2')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Beans</td>
                <td>₦300</td>
                <td>
                    <input type="number" id="qty3" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Beans', 300, 'qty3')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Yam</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty4" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Yam', 200, 'qty4')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Spaghetti</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty5" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Spaghetti', 200, 'qty5')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Pounded Yam</td>
                <td>₦300</td>
                <td>
                    <input type="number" id="qty6" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Pounded Yam', 300, 'qty6')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Eba</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty7" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Eba', 200, 'qty7')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Meat</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty8" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Meat', 200, 'qty8')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Egg</td>
                <td>₦300</td>
                <td>
                    <input type="number" id="qty9" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Egg', 300, 'qty9')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Fish</td>
                <td>₦500</td>
                <td>
                    <input type="number" id="qty10" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Fish', 500, 'qty10')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Soft Drink</td>
                <td>₦500</td>
                <td>
                    <input type="number" id="qty11" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Soft Drink', 500, 'qty11')">
                        Add
                    </button>
                </td>
            </tr>

            <tr>
                <td>Bottled Water</td>
                <td>₦200</td>
                <td>
                    <input type="number" id="qty12" min="1" value="1">
                </td>
                <td>
                    <button onclick="addFood('Bottled Water', 200, 'qty12')">
                        Add
                    </button>
                </td>
            </tr>

        </tbody>
    </table>

    <div class="receipt">

        <h2>Order Summary</h2>

        <table>
            <thead>
                <tr>
                    <th>Food</th>
                    <th>Quantity</th>
                    <th>Price</th>
                    <th>Total</th>
                </tr>
            </thead>

            <tbody id="orderList"></tbody>
        </table>

        <div class="total">
            Total: ₦<span id="total">0</span>
        </div>

        <br>

        <label>Amount Paid:</label>

        <input
            type="number"
            id="amountPaid"
            placeholder="Enter amount paid"
        >

        <button onclick="calculateChange()">
            Calculate Change
        </button>

        <h3>
            Change: ₦<span id="change">0</span>
        </h3>

        <button onclick="printReceipt()">
            Print Receipt
        </button>

        <button onclick="clearOrder()">
            Clear Order
        </button>

    </div>

</div>


<script>

    let total = 0;

    function addFood(foodName, price, quantityId) {

        let quantity = parseInt(
            document.getElementById(quantityId).value
        );

        if (quantity <= 0 || isNaN(quantity)) {
            alert("Please enter a valid quantity.");
            return;
        }

        let itemTotal = price * quantity;

        total += itemTotal;

        let orderList = document.getElementById("orderList");

        let row = document.createElement("tr");

        row.innerHTML = `
            <td>${foodName}</td>
            <td>${quantity}</td>
            <td>₦${price}</td>
            <td>₦${itemTotal}</td>
        `;

        orderList.appendChild(row);

        document.getElementById("total").innerText = total;
    }


    function calculateChange() {

        let amountPaid = parseFloat(
            document.getElementById("amountPaid").value
        );

        if (isNaN(amountPaid)) {
            alert("Please enter the amount paid.");
            return;
        }

        if (amountPaid < total) {
            alert("Insufficient payment.");
            return;
        }

        let change = amountPaid - total;

        document.getElementById("change").innerText = change;
    }


    function clearOrder() {

        total = 0;

        document.getElementById("orderList").innerHTML = "";

        document.getElementById("total").innerText = "0";

        document.getElementById("amountPaid").value = "";

        document.getElementById("change").innerText = "0";
    }


    function printReceipt() {

        let customerName =
            document.getElementById("customerName").value;

        if (customerName === "") {
            alert("Please enter the customer's name.");
            return;
        }

        if (total === 0) {
            alert("No food has been ordered.");
            return;
        }

        window.print();
    }

</script>

</body>
</html>
