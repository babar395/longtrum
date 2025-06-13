<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Longtrum - Crypto Investment Platform</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #0a0a0a;
      color: #00ff99;
      overflow-x: hidden;
    }
    header {
      padding: 1rem;
      text-align: center;
      background-color: #000;
      border-bottom: 2px solid #00ff99;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin: 1rem 0;
      flex-wrap: wrap;
    }
    nav a {
      color: #00ff99;
      text-decoration: none;
      font-weight: bold;
    }
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1rem;
    }
    .plans, .dashboard, .referral, .about, .team, .blog, .deposit, .howto, .daily-update {
      margin-top: 2rem;
      background-color: #111;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 0 10px #00ff99;
    }
    .plans h2, .dashboard h2, .referral h2, .about h2, .team h2, .blog h2, .deposit h2, .howto h2, .daily-update h2 {
      border-bottom: 1px solid #00ff99;
      padding-bottom: 0.5rem;
    }
    .plan {
      margin: 1rem 0;
      padding: 1rem;
      border: 1px dashed #00ff99;
      border-radius: 8px;
    }
    .footer {
      text-align: center;
      padding: 1rem;
      background-color: #000;
      margin-top: 2rem;
      border-top: 2px solid #00ff99;
    }
    .support-button {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #00ff99;
      color: #000;
      padding: 10px 15px;
      border-radius: 50px;
      text-decoration: none;
      box-shadow: 0 0 10px #00ff99;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 5px;
      font-size: 1rem;
    }
    button {
      background-color: #00ff99;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }
    ol {
      padding-left: 1.5rem;
    }
    ol li {
      margin-bottom: 0.5rem;
    }
    .extra-deposit-note {
      background: #000;
      border-left: 4px solid #00ff99;
      padding: 10px;
      margin: 10px 0;
      font-size: 0.95rem;
    }
    .language-container {
      margin-top: 10px;
    }
    .language-container label {
      margin-right: 10px;
    }
    .language-container select {
      max-width: 200px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Longtrum – Smart Crypto Investment</h1>
  </header>
  <nav>
    <a href="#dashboard">Dashboard</a>
    <a href="#plans">Plans</a>
    <a href="#deposit">Deposit</a>
    <a href="#referral">Referral</a>
    <a href="#about">About</a>
    <a href="#team">Team</a>
    <a href="#blog">Blog</a>
    <a href="#howto">How to Use</a>
    <a href="#dailyupdate">Daily Update</a>
  </nav>

  <div class="container">
    <section id="plans" class="plans">
      <h2>Investment Plans</h2>
      <div class="plan">$10 Investment → <strong>2% Daily Profit</strong></div>
      <div class="plan">$50 Investment → <strong>3% Daily Profit</strong></div>
      <div class="plan">$100 Investment → <strong>4% Daily Profit</strong></div>
      <div class="plan">$200 Investment → <strong>5% Daily Profit</strong></div>
      <div class="plan">$500 Investment → <strong>6% Daily Profit</strong></div>
      <div class="plan">$1000 Investment → <strong>7% Daily Profit</strong></div>
      <div class="plan">$2000 Investment → <strong>8% Daily Profit</strong></div>
    </section>

    <section id="calculator" class="plans">
      <h2>Profit Calculator</h2>
      <label for="amount">Enter Amount ($):</label>
      <input type="number" id="amount" placeholder="Enter investment amount">
      <label for="rate">Select Plan (% Daily):</label>
      <select id="rate">
        <option value="2">2%</option>
        <option value="3">3%</option>
        <option value="4">4%</option>
        <option value="5">5%</option>
        <option value="6">6%</option>
        <option value="7">7%</option>
        <option value="8">8%</option>
      </select>
      <button onclick="calculateProfit()">Calculate Daily Profit</button>
      <p id="result"></p>
    </section>
  </div>

  <div class="footer">
    <p>&copy; 2025 Longtrum. All rights reserved.</p>
  </div>

  <a class="support-button" href="mailto:abubakarkhalilzad@gmail.com">
    <i class="fas fa-envelope"></i> Support
  </a>

  <script>
    function calculateProfit() {
      const amount = parseFloat(document.getElementById('amount').value);
      const rate = parseFloat(document.getElementById('rate').value);
      if (!amount || amount <= 0) {
        document.getElementById('result').innerText = 'Enter a valid amount.';
        return;
      }
      const profit = (amount * rate) / 100;
      document.getElementById('result').innerText = `Daily Profit: $${profit.toFixed(2)}`;
    }
  </script>
</body>
</html>
