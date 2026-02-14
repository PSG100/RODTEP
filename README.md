<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>RoDTEP License Exchange</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#f4f6f9;
color:#333;
}

header{
background:#0a2a43;
color:white;
padding:60px 20px;
text-align:center;
}

header h1{
font-size:34px;
margin-bottom:10px;
}

.btn{
display:inline-block;
margin-top:20px;
padding:12px 28px;
background:#ff9800;
color:white;
text-decoration:none;
border-radius:25px;
font-weight:600;
}

section{
padding:60px 20px;
text-align:center;
}

.container{
max-width:1100px;
margin:auto;
}

.form-box{
background:white;
padding:40px;
border-radius:12px;
box-shadow:0 10px 25px rgba(0,0,0,0.08);
margin-top:30px;
}

input, select, textarea{
width:100%;
padding:12px;
margin-bottom:15px;
border-radius:8px;
border:1px solid #ccc;
}

label{
font-weight:600;
display:block;
margin-bottom:6px;
text-align:left;
}

button{
padding:12px 25px;
border:none;
background:#0a2a43;
color:white;
border-radius:25px;
font-weight:600;
cursor:pointer;
}

.note{
background:#fff3cd;
padding:20px;
margin-top:30px;
border-radius:8px;
font-size:14px;
text-align:left;
}

footer{
background:#0a2a43;
color:white;
padding:20px;
text-align:center;
margin-top:50px;
font-size:14px;
}
</style>

<script>
function calculateSell() {
  let value = document.getElementById("sellValue").value;
  let rate = 0.97;
  if(value){
    document.getElementById("sellAmount").value = (value * rate).toFixed(2);
  }
}

function calculateBuy() {
  let value = document.getElementById("buyValue").value;
  let rate = 0.98;
  if(value){
    document.getElementById("buyAmount").value = (value * rate).toFixed(2);
  }
}
</script>

</head>

<body>

<header>
<h1>RoDTEP License Exchange</h1>
<p>Secure & Compliance-Driven Trading Platform</p>
<a href="#trade" class="btn">Submit Trade Request</a>
</header>

<section id="trade">
<div class="container">
<h2>Buy / Sell RoDTEP License</h2>

<div class="form-box">
<form>

<label>Company Name</label>
<input type="text" required>

<label>IEC Number</label>
<input type="text" required>

<label>Contact Person Name (Buyer/Seller)</label>
<input type="text" required>

<label>Email ID</label>
<input type="email" required>

<label>Contact Mobile Number</label>
<input type="tel" pattern="[0-9]{10}" placeholder="10-digit mobile number" required>

<label>Transaction Type</label>
<select required>
<option value="">Select</option>
<option>Sell License</option>
<option>Purchase License</option>
</select>

<hr style="margin:25px 0;">

<h3>Sell License Details</h3>

<label>Sell License Value (₹)</label>
<input type="number" id="sellValue" onkeyup="calculateSell()">

<label>Expected Sale License Amount (₹)</label>
<input type="number" id="sellAmount" readonly>

<hr style="margin:25px 0;">

<h3>Purchase License Details</h3>

<label>Purchase License Value (₹)</label>
<input type="number" id="buyValue" onkeyup="calculateBuy()">

<label>Expected Purchase License Amount (₹)</label>
<input type="number" id="buyAmount" readonly>

<hr style="margin:25px 0;">

<h3>BRC / FIRC Compliance Details</h3>

<label>Confirm Shipping Bill Realised with BRC/FIRC</label>
<select required>
<option value="">Select</option>
<option>Yes – Realised</option>
<option>No</option>
</select>

<label>Upload BRC Details (Excel Format)</label>
<input type="file" accept=".xls,.xlsx" required>

<label>Upload Bank Realisation Certificate</label>
<input type="file" accept=".pdf,.jpg,.png" required>

<label>Additional Remarks</label>
<textarea rows="4"></textarea>

<button type="submit">Submit Request</button>

</form>

<div class="note">
<strong>Important Instructions:</strong><br><br>
• Please provide Email ID and Contact Mobile Number of Buyer/Seller along with his name.<br>
• Shipping Bill against the RoDTEP License must have realised BRC/FIRC.<br>
• BRC details must be furnished in Excel format.<br>
• Bank Certificate confirming realisation is mandatory.<br>
• Subject to verification before trade execution.
</div>

</div>
</div>
</section>

<footer>
© 2026 RoDTEP License Exchange | All Rights Reserved
</footer>

</body>
</html>
