# TECLADO.CCSIT.2026_THE-FIFTH-GEAR
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Tech Fest Registration</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
      color: #fff;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .container {
  background: linear-gradient(180deg, rgba(10,10,20,0.85), rgba(0,0,0,0.95));
  border-radius: 14px;
  padding: 30px;
  width: 100%;
  max-width: 420px;
  border: 1px solid rgba(255,0,0,0.4);
  box-shadow:
    0 0 20px rgba(255,0,0,0.4),
    inset 0 0 25px rgba(255,0,0,0.15);
  position: relative;
  overflow: hidden;
}

.container::after {
  content: "";
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    to bottom,
    rgba(255,255,255,0.03),
    rgba(255,255,255,0.03) 1px,
    transparent 1px,
    transparent 4px
  );
  pointer-events: none;
  animation: scan 6s linear infinite;
}

@keyframes scan {
  from { background-position: 0 0; }
  to { background-position: 0 100%; }
}


h1 {
  text-align: center;
  font-size: 26px;
  letter-spacing: 3px;
  color: #ff2e2e;
  text-shadow: 0 0 10px rgba(255,46,46,0.8);
}


    p {
      text-align: center;
      font-size: 14px;
      opacity: 0.8;
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-size: 13px;
      opacity: 0.9;
    }

    input, select {
      width: 100%;
      padding: 12px;
      margin-bottom: 18px;
      border-radius: 8px;
      border: none;
      outline: none;
      font-family: inherit;
    }

    input:focus, select:focus {
      box-shadow: 0 0 8px #ff2e2e;
    }

    button {
  background: linear-gradient(90deg, #ff0000, #ff8800);
  letter-spacing: 2px;
  font-weight: bold;
  position: relative;
}

button::after {
  position: absolute;
  right: 20px;
  opacity: 0.6;
}

    button:hover {
      transform: scale(1.03);
      box-shadow: 0 0 15px rgba(255,75,43,0.7);
    }

    .success {
      display: none;
      text-align: center;
      margin-top: 20px;
      color: #00ff99;
    }

    footer {
      text-align: center;
      margin-top: 15px;
      font-size: 12px;
      opacity: 0.6;
    }
    .checkbox-group {
  margin-bottom: 20px;
}

.checkbox {
  padding: 10px 14px;
  border: 1px solid rgba(255,255,255,0.15);
  border-radius: 8px;
  transition: all 0.25s ease;
  background: rgba(0,0,0,0.4);
}

.checkbox:hover {
  border-color: #ff2e2e;
  box-shadow: 0 0 10px rgba(255,46,46,0.6);
  transform: translateX(4px);
}

.checkbox input:checked + span {
  color: #00ffcc;
}


.checkbox input {
  accent-color: #ff2e2e;
  width: 16px;
  height: 16px;
}
/* 🔘 Floating Action Buttons */
.fab {
  position: fixed;
  bottom: 20px;
  z-index: 999;
}

.call-fab {
  left: 20px;
}

.insta-fab {
  right: 20px;
}

.fab a {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 16px;
  border-radius: 50px;
  background: linear-gradient(90deg, #ff0000, #ff4b2b);
  color: #fff;
  text-decoration: none;
  font-size: 13px;
  box-shadow: 0 0 15px rgba(255,0,0,0.6);
  transition: transform 0.2s, box-shadow 0.2s;
}

.fab a:hover {
  transform: scale(1.05);
  box-shadow: 0 0 25px rgba(255,75,43,0.9);
}
.score-box {
  font-family: monospace;
  background: rgba(0,0,0,0.6);
  border-left: 4px solid #ffd700;
  padding: 10px;
  margin-bottom: 15px;
  text-shadow: 0 0 5px rgba(255,215,0,0.6);
}
#entryPass img {
  box-shadow: 0 0 25px rgba(0,255,200,0.8);
}

  </style>
</head>
<body>

  <div class="container">
    <h1>TECLADO</h1>
    <p>CCSIT PALAKKAD</p>

    <form id="regForm">
       <input type="text" id="name" required />
<input type="email" id="email" required />
<input type="tel" id="phone" required />
<input type="text" id="college" required />

<label>Select Events</label>

<div class="checkbox-group">
  <label class="checkbox">
    <input type="checkbox" name="events" value="Hackathon">
    <span>Hackathon</span>
    
  </label>

  <label class="checkbox">
    <input type="checkbox" name="events" value="Code Debugging">
    <span>Debugging</span> 
  </label>

  <label class="checkbox">
    <input type="checkbox" name="events" value="Tech Quiz">
    <span>Tech Quiz</span>
  </label>

  <label class="checkbox">
    <input type="checkbox" name="events" value="Gaming">
    <span>Gaming</span>
  </label>
</div>
<div id="feeBox">
  💰 TOTAL FEES: ₹100
</div>

<div id="qrBox" style="display:none; text-align:center; margin-bottom:15px;">
  <p style="font-size:13px; opacity:0.8;">Scan to Pay</p>
  <img id="qrImg" style="width:200px; border-radius:10px;" />
</div>
<label>Payment Method</label>
<select id="paymentMode" required>
  <option value="UPI QR">UPI QR</option>
</select>

<label>Upload Payment Screenshot</label>
<input type="file" id="paymentProof" accept="image/*" />


<button type="button" id="paidBtn" style="margin-bottom:15px;">
  ✅ Confirm Payment & Register
</button>

    </form>
    <div id="entryPass" style="display:none; text-align:center; margin-top:20px;">
      <h3>🎟 Entry Pass</h3>
      <img id="entryQR" style="width:220px;border-radius:10px;">
      <p style="font-size:13px;opacity:0.8;">Show this at the entry gate</p>
    </div>
    
    <div class="success" id="successMsg">
      ✅ Registration Successful!<br />
      See you at the fest 🚀
    
      <br><br>
    
      <a href="https://chat.whatsapp.com/GbVDdVB3pSFKymxNxYkdv7">
        👉 Join Official WhatsApp Group
      </a>
    </div>
    

    <footer>
      © 2026 TECLADO, THE FIFTH GEAR
    </footer>
  </div>

  <script>
  const feeBox = document.getElementById('feeBox');
  const qrBox = document.getElementById('qrBox');
  const qrImg = document.getElementById('qrImg');
  const checkboxes = document.querySelectorAll('input[name="events"]');

  const UPI_ID = "umasreeram333@oksbi";   // 🔴 CHANGE THIS
  const PAYEE_NAME = "TECLADO";

  function calculateFee() {
    let fee = 100;
    checkboxes.forEach(cb => {
      if (cb.checked && (cb.value === "Hackathon" || cb.value === "Gaming")) {
        fee += 50;
      }
    });
    feeBox.innerHTML = `💰 Total Fee: ₹${fee}`;
    generateQR(fee);
    return fee;
  }

  function generateQR(amount) {
  const name = document.getElementById("name").value.trim() || "Participant";
    const upiURL = `upi://pay?pa=${UPI_ID}&pn=${encodeURIComponent(PAYEE_NAME)}&am=${amount}&cu=INR&tn=${encodeURIComponent("TECLADO Registration - " + name)}`;

    qrImg.src =
      "https://api.qrserver.com/v1/create-qr-code/?size=300x300&data=" +
      encodeURIComponent(upiURL);

    qrBox.style.display = "block";
  }

  checkboxes.forEach(cb => cb.addEventListener('change', calculateFee));
  calculateFee();
</script>

<script>
const SCRIPT_URL = "https://script.google.com/macros/s/AKfycbwZD34qmlEVMxWrGxd7_jyORkO9l4M--KOqH0pOrXDPSwe2JKHhZHScK7QQmNO9NuKdUg/exec"; // 🔴 IMPORTANT

const paidBtn = document.getElementById("paidBtn");
const entryPass = document.getElementById("entryPass");
const entryQR = document.getElementById("entryQR");
const form = document.getElementById("regForm");
const success = document.getElementById("successMsg");

paidBtn.addEventListener("click", () => {

  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const phone = document.getElementById("phone").value.trim();
  const college = document.getElementById("college").value.trim();
  const paymentMode = document.getElementById("paymentMode").value;
  const file = document.getElementById("paymentProof").files[0];

  const events = [...document.querySelectorAll('input[name="events"]:checked')]
                .map(e => e.value);

  if (!name || !email || !phone || !college) {
    alert("Please fill all personal details");
    return;
  }

  if (events.length === 0) {
    alert("Please select at least one event");
    return;
  }

  if (!file) {
    alert("Upload payment screenshot");
    return;
  }

  paidBtn.disabled = true;
  paidBtn.innerText = "⏳ Registering...";

  const reader = new FileReader();

  reader.onload = async () => {
    const payload = {
      name,
      email,
      phone,
      college,
      events,
      amount: calculateFee(),
      paymentMode,
      screenshot: reader.result.split(",")[1],
      mimeType: file.type
    };

    try {
      const res = await fetch(SCRIPT_URL, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(payload)
      });

      const result = await res.json();

      if (!result.success) {
        throw new Error(result.error || "Server error");
      }

      entryQR.src =
        "https://api.qrserver.com/v1/create-qr-code/?size=300x300&data=" +
        encodeURIComponent(result.qrData);

      form.style.display = "none";
      entryPass.style.display = "block";
      success.style.display = "block";

    } catch (err) {
      console.error(err);
      alert("❌ Registration failed. Please try again.");
      paidBtn.disabled = false;
      paidBtn.innerText = "✅ Confirm Payment & Register";
    }
  };

  reader.readAsDataURL(file);
});
</script>

  

<!-- 📸 INSTAGRAM BUTTON (BOTTOM RIGHT) -->
<div class="fab insta-fab">
  <a href="https://www.instagram.com/ccsit.palakkad_official" target="_blank">
    📸 Instagram
  </a>
</div>
</body>
</html> 
