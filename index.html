
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>SWIFT BANK TERMINAL - PRO</title>
  <style>
    body {
      background-color: black;
      color: #00FF00;
      font-family: monospace;
      padding: 0;
      margin: 0;
    }
    .terminal, .login, .form-container {
      display: none;
      padding: 20px;
    }
    .visible {
      display: block;
    }
    .terminal {
      border-top: 2px solid #00FF00;
      height: 70vh;
      overflow-y: auto;
    }
    input, button {
      background: black;
      color: #00FF00;
      border: 1px solid #00FF00;
      padding: 5px;
      margin: 5px 0;
      font-family: monospace;
    }
    table {
      border-collapse: collapse;
      margin-top: 10px;
      width: 100%;
    }
    td, th {
      border: 1px solid #00FF00;
      padding: 5px;
      font-size: 12px;
    }
    .typewriter {
      overflow: hidden;
      border-right: .15em solid #00FF00;
      white-space: nowrap;
      animation: typing 1s steps(40, end), blink-caret .75s step-end infinite;
    }
    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }
    @keyframes blink-caret {
      from, to { border-color: transparent }
      50% { border-color: #00FF00 }
    }
  </style>
</head>
<body>

  <div class="login visible" id="login">
    <h2>ENTER TERMINAL PASSWORD</h2>
    <input type="password" id="password" placeholder="Enter password..." />
    <button onclick="login()">Access Terminal</button>
  </div>

  <div class="form-container" id="formContainer">
    <h2>SWIFT MT103 Form</h2>
    <input id="ref" placeholder="Ref ID (e.g. TRX123456)" /><br>
    <input id="from" placeholder="Sender Name" /><br>
    <input id="to" placeholder="Receiver Name" /><br>
    <input id="iban" placeholder="Receiver IBAN" /><br>
    <input id="amount" placeholder="Amount (EUR)" /><br>
    <button onclick="send()">Send MT103</button>
  </div>

  <div class="terminal" id="terminal"></div>

  <div class="history" id="history">
    <h3>Message History</h3>
    <table><thead><tr><th>Ref</th><th>Sender</th><th>Receiver</th><th>Amount</th></tr></thead>
    <tbody id="historyBody"></tbody></table>
  </div>

  <script>
    const PASSWORD = "swift123";

    function login() {
      const input = document.getElementById("password").value;
      if (input === PASSWORD) {
        document.getElementById("login").classList.remove("visible");
        document.getElementById("formContainer").classList.add("visible");
        document.getElementById("terminal").classList.add("visible");
        loadHistory();
      } else {
        alert("Incorrect password.");
      }
    }

    function send() {
      const ref = document.getElementById("ref").value;
      const from = document.getElementById("from").value;
      const to = document.getElementById("to").value;
      const iban = document.getElementById("iban").value;
      const amount = document.getElementById("amount").value;
      const terminal = document.getElementById("terminal");

      terminal.innerHTML = "";
      print(`> CONNECTING TO SWIFT NETWORK...`);
      print(`> SENDING MT103...`);
      print(`> REF: ${ref}`);
      print(`> FROM: ${from}`);
      print(`> TO: ${to} - ${iban}`);
      print(`> AMOUNT: EUR ${amount}`);
      print(`> STATUS: IN TRANSIT`);

      saveToHistory(ref, from, to, amount);

      setTimeout(() => {
        print(`\n> MT900 RECEIVED FROM RECEIVING BANK`);
        print(`:20:${ref}\n:25:HSBCBANKUK\n:32A:250506EUR${amount},00\n:61:CONFIRMED`);
        print(`\n> TRANSACTION CONFIRMED`);
        print(`> STATUS: FINALIZED`);
      }, 7000);
    }

    function print(text) {
      const terminal = document.getElementById("terminal");
      const line = document.createElement("div");
      line.classList.add("message");
      line.textContent = text;
      terminal.appendChild(line);
      terminal.scrollTop = terminal.scrollHeight;
    }

    function saveToHistory(ref, from, to, amount) {
      const data = JSON.parse(localStorage.getItem("swiftHistory") || "[]");
      data.push({ ref, from, to, amount });
      localStorage.setItem("swiftHistory", JSON.stringify(data));
      loadHistory();
    }

    function loadHistory() {
      const data = JSON.parse(localStorage.getItem("swiftHistory") || "[]");
      const tbody = document.getElementById("historyBody");
      tbody.innerHTML = "";
      data.forEach(item => {
        const row = `<tr><td>${item.ref}</td><td>${item.from}</td><td>${item.to}</td><td>${item.amount}</td></tr>`;
        tbody.innerHTML += row;
      });
    }
  </script>

</body>
</html>
