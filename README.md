<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>וופל בלגי על מקל | הזמנה</title>
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
  <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --primary: #ff9f47;
      --primary-dark: #e88b35;
      --secondary: #4a2c1b;
      --bg-color: #fff9f2;
      --card-bg: #ffffff;
      --text-color: #333;
      --success: #25D366;
      --radius: 16px;
      --shadow: 0 10px 30px rgba(0,0,0,0.08);
    }

    body {
      font-family: 'Rubik', sans-serif;
      background: var(--bg-color);
      margin: 0;
      padding: 0;
      color: var(--text-color);
      padding-bottom: 40px;
    }

    /* --- Header Image --- */
    .header-hero {
      width: 100%;
      height: 220px;
      background-image: url('https://images.unsplash.com/photo-1561575558-450371302ee6?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80'); 
      background-size: cover;
      background-position: center;
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.15);
      position: relative;
    }
    
    .header-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: linear-gradient(to top, rgba(0,0,0,0.6), transparent);
      padding: 20px;
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
      text-align: center;
    }

    .header-title {
      color: white;
      font-size: 32px;
      font-weight: 700;
      margin: 0;
      text-shadow: 0 2px 4px rgba(0,0,0,0.3);
    }

    .container {
      max-width: 600px;
      margin: -40px auto 0;
      position: relative;
      padding: 0 15px;
    }

    .card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 25px;
      box-shadow: var(--shadow);
      margin-bottom: 20px;
    }

    .price-badge {
      background: #fff3e6;
      color: var(--secondary);
      padding: 8px 15px;
      border-radius: 50px;
      font-weight: 700;
      display: inline-block;
      margin-bottom: 15px;
      border: 1px solid var(--primary);
    }

    .phone-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      background: #fff;
      border: 2px solid var(--secondary);
      color: var(--secondary);
      padding: 10px;
      border-radius: 10px;
      text-decoration: none;
      font-weight: 700;
      transition: 0.2s;
      margin-bottom: 20px;
    }
    .phone-btn:hover { background: var(--secondary); color: #fff; }

    /* --- Form Elements --- */
    label {
      font-size: 14px;
      font-weight: 700;
      color: var(--secondary);
      margin-bottom: 6px;
      display: block;
    }
    
    input, textarea, select {
      width: 100%;
      padding: 14px;
      background: #f9f9f9;
      border: 1px solid #e0e0e0;
      border-radius: 12px;
      font-family: inherit;
      font-size: 16px;
      box-sizing: border-box;
      transition: 0.3s;
      outline: none;
    }
    input:focus, textarea:focus {
      border-color: var(--primary);
      background: #fff;
      box-shadow: 0 0 0 3px rgba(255, 159, 71, 0.2);
    }

    /* --- Waffle Section --- */
    .waffle-card {
      background: #fff;
      border: 2px solid #eee;
      border-radius: 15px;
      padding: 15px;
      margin-top: 15px;
      animation: slideIn 0.4s ease;
      position: relative;
      overflow: hidden;
    }
    .waffle-card::before {
      content: '';
      position: absolute;
      top: 0; right: 0; width: 6px; height: 100%;
      background: var(--primary);
    }
    
    @keyframes slideIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .waffle-title {
      font-size: 18px;
      color: var(--secondary);
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 5px;
    }

    .options-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 15px;
    }
    
    /* עיצוב כפתורי בחירה מודרניים במקום צ'קבוקס */
    .option-btn input { display: none; }
    .option-btn label {
      cursor: pointer;
      padding: 8px 14px;
      background: #f0f0f0;
      border-radius: 20px;
      font-size: 14px;
      font-weight: 500;
      color: #555;
      border: 1px solid transparent;
      transition: 0.2s;
      display: flex;
      align-items: center;
      gap: 5px;
      margin: 0;
    }
    
    .option-btn input:checked + label {
      background: var(--primary);
      color: white;
      box-shadow: 0 4px 10px rgba(255, 159, 71, 0.4);
    }

    /* --- Payment --- */
    .payment-container {
      background: #fdfdfd;
      border: 1px solid #eee;
      padding: 15px;
      border-radius: 12px;
      margin-top: 20px;
    }
    .payment-hidden { display: none; }

    .payment-radios {
      display: flex;
      gap: 10px;
      margin-bottom: 10px;
    }
    .pay-radio input { display: none; }
    .pay-radio label {
      flex: 1;
      text-align: center;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 500;
      transition: 0.2s;
    }
    .pay-radio input:checked + label {
      border-color: var(--primary);
      background: #fff8f0;
      color: var(--primary-dark);
      font-weight: 700;
    }

    .copy-box {
      background: #fff;
      border: 1px dashed var(--primary);
      padding: 10px;
      border-radius: 8px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
      font-size: 14px;
    }
    .copy-btn-action {
      background: #eee;
      border: none;
      padding: 5px 10px;
      border-radius: 5px;
      font-weight: bold;
      cursor: pointer;
      font-size: 12px;
    }
    .copy-btn-action.copied { background: #4CAF50; color: white; }

    /* --- Buttons --- */
    .btn-main {
      width: 100%;
      padding: 16px;
      background: linear-gradient(135deg, #ff9f47, #ff8520);
      color: white;
      border: none;
      border-radius: 12px;
      font-size: 18px;
      font-weight: 700;
      box-shadow: 0 4px 15px rgba(255, 133, 32, 0.4);
      cursor: pointer;
      margin-top: 25px;
      transition: transform 0.2s;
    }
    .btn-main:active { transform: scale(0.98); }
    
    .btn-app {
      display: block;
      width: 100%;
      text-align: center;
      padding: 12px;
      border-radius: 10px;
      color: white;
      font-weight: 700;
      text-decoration: none;
      margin-top: 10px;
      border: none;
      cursor: pointer;
      font-size: 16px;
    }
    .btn-bit { background: #2b5cff; }
    .btn-paybox { background: #00bfa5; }

    .btn-reset {
      background: none;
      border: none;
      color: #999;
      text-decoration: underline;
      margin-top: 15px;
      width: 100%;
      cursor: pointer;
    }

    .total-bar {
      text-align: center;
      font-size: 24px;
      font-weight: 800;
      color: var(--secondary);
      margin: 20px 0;
      padding: 15px;
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }

    .error-msg { color: #ff3b30; font-size: 12px; display: none; margin-top: 4px; }
    .input-error { border-color: #ff3b30 !important; }

    .receipt-section {
      display: none;
      margin-top: 20px;
      background: #e6ffed;
      padding: 15px;
      border-radius: 12px;
      text-align: center;
      border: 1px solid #b7eac5;
    }
    .receipt-link {
      display: inline-block;
      margin-top: 10px;
      background: #25D366;
      color: white;
      padding: 10px 20px;
      border-radius: 20px;
      text-decoration: none;
      font-weight: bold;
    }

  </style>
</head>
<body>

  <div class="header-hero">
    <div class="header-overlay">
      <h1 class="header-title">וופל בלגי על מקל 🧇</h1>
    </div>
  </div>

  <div class="container">
    <div class="card">
      <div style="text-align:center;">
        <span class="price-badge">רק 7 ש"ח לוופל!</span>
      </div>
      <a href="tel:0542296540" class="phone-btn">📞 להזמנות: 054-2296540</a>

      <label>שם מלא <span style="color:red">*</span></label>
      <input type="text" id="name" placeholder="איך קוראים לך?">
      <div id="err-name" class="error-msg">נא למלא שם</div>

      <label style="margin-top:15px">טלפון <span style="color:red">*</span></label>
      <input type="tel" id="phone" placeholder="מספר נייד">
      <div id="err-phone" class="error-msg">נא למלא טלפון תקין</div>

      <label style="margin-top:15px">שעה לאיסוף</label>
      <input type="time" id="time">
    </div>

    <div class="card">
      <label style="font-size:18px;">כמה וופלים לפנק? 😋</label>
      <div style="display:flex; align-items:center; gap:10px; margin-top:10px;">
        <button onclick="changeQty(-1)" style="width:40px; height:40px; border-radius:10px; border:1px solid #ddd; background:#fff; font-size:20px; cursor:pointer;">-</button>
        <input type="number" id="qty" value="0" min="0" style="text-align:center; font-size:20px; font-weight:bold; width:60px; padding:5px;">
        <button onclick="changeQty(1)" style="width:40px; height:40px; border-radius:10px; border:none; background:var(--primary); color:#fff; font-size:20px; cursor:pointer;">+</button>
      </div>
      <div id="err-qty" class="error-msg">יש לבחור כמות או למלא הערות</div>

      <div id="waffles-container"></div>
    </div>

    <div class="total-bar" id="totalDisplay">סה"כ: 0 ש"ח</div>

    <div id="payment-section" class="card payment-hidden">
      <label>איך תרצו לשלם? <span style="color:red">*</span></label>
      
      <div class="payment-radios">
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_bit" value="ביט">
          <label for="p_bit">ביט</label>
        </div>
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_pb" value="פייבוקס">
          <label for="p_pb">פייבוקס</label>
        </div>
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_cash" value="מזומן">
          <label for="p_cash">מזומן</label>
        </div>
      </div>
      <div id="err-pay" class="error-msg">נא לבחור אמצעי תשלום</div>

      <div id="payment-dynamic-area"></div>
    </div>

    <div class="card">
      <label>הערות / בקשות מיוחדות</label>
      <textarea id="notes" rows="3" placeholder="כאן אפשר לכתוב כל דבר נוסף..."></textarea>
      
      <button class="btn-main" id="sendBtn" onclick="sendOrder()">שליחת הזמנה לווטסאפ 🚀</button>
      
      <div id="receiptBox" class="receipt-section">
        <div style="font-weight:bold; color:#155724; margin-bottom:5px;">ההזמנה נשלחה בהצלחה?</div>
        <div>לחץ כאן כדי לשלוח קבלה ללקוח:</div>
        <a id="receiptLink" href="#" target="_blank" class="receipt-link">שלח קבלה 🧾</a>
      </div>

      <button class="btn-reset" onclick="resetForm()">איפוס טופס</button>
      
      <div style="text-align:center; margin-top:20px; font-size:13px; color:#888;">
        ⭐ חובה ללחוץ על "שלח" בתוך הוואטסאפ כדי שההזמנה תתקבל
      </div>
    </div>
  </div>

<script>
const PRICE = 7;
const MY_PHONE = "972542296540";
const BIT_NUM = "0506205953";
const PB_NUM = "0542296540";

// --- Logic ---

function changeQty(delta) {
  const el = document.getElementById('qty');
  let val = parseInt(el.value) || 0;
  val += delta;
  if(val < 0) val = 0;
  el.value = val;
  updateUI();
}

document.getElementById('qty').addEventListener('input', updateUI);

// Load saved data on start
document.addEventListener('DOMContentLoaded', () => {
  const savedName = localStorage.getItem('waffle_name');
  const savedPhone = localStorage.getItem('waffle_phone');
  if(savedName) document.getElementById('name').value = savedName;
  if(savedPhone) document.getElementById('phone').value = savedPhone;
  updateUI();
});

function updateUI() {
  const qty = parseInt(document.getElementById('qty').value) || 0;
  const container = document.getElementById('waffles-container');
  const paySection = document.getElementById('payment-section');
  const totalDisplay = document.getElementById('totalDisplay');

  // Update Total
  totalDisplay.innerText = `סה"כ: ${qty * PRICE} ש"ח`;

  // Show/Hide Payment
  if (qty > 0) {
    paySection.classList.remove('payment-hidden');
  } else {
    paySection.classList.add('payment-hidden');
    // Clear payment selection if hidden
    document.querySelectorAll('input[name="pay"]').forEach(r => r.checked = false);
    document.getElementById('payment-dynamic-area').innerHTML = '';
  }

  // Generate Waffle Cards (Preserve existing selections if possible logic omitted for simplicity, re-render is safer for simple forms)
  // Note: A smarter diffing algo would be better, but for this scale, re-rendering based on count is OK. 
  // To keep user input when increasing qty, we read values first? 
  // For simplicity in this "upgrade", we will only append if growing, or remove from end if shrinking.
  
  const currentCards = container.children.length;
  
  if (qty > currentCards) {
    for (let i = currentCards + 1; i <= qty; i++) {
      const div = document.createElement('div');
      div.className = 'waffle-card';
      div.innerHTML = getWaffleHTML(i);
      container.appendChild(div);
    }
  } else if (qty < currentCards) {
    while (container.children.length > qty) {
      container.removeChild(container.lastChild);
    }
  }
}

function getWaffleHTML(i) {
  return `
    <div class="waffle-title"><b>🧇 וופל #${i}</b></div>
    
    <label style="font-size:13px; color:#777;">רטבים:</label>
    <div class="options-grid">
      <div class="option-btn">
        <input type="checkbox" id="s_choc_${i}" name="sauce_${i}" value="שוקולד">
        <label for="s_choc_${i}">🍫 שוקולד</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="s_maple_${i}" name="sauce_${i}" value="מייפל">
        <label for="s_maple_${i}">🥞 מייפל</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="s_milk_${i}" name="sauce_${i}" value="ריבת חלב">
        <label for="s_milk_${i}">🥛 ריבת חלב</label>
      </div>
    </div>

    <label style="font-size:13px; color:#777;">תוספות:</label>
    <div class="options-grid">
      <div class="option-btn">
        <input type="checkbox" id="t_oreo_${i}" name="top_${i}" value="אוראו">
        <label for="t_oreo_${i}">⚫ אוראו</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="t_lotus_${i}" name="top_${i}" value="לוטוס">
        <label for="t_lotus_${i}">🍪 לוטוס</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="t_click_${i}" name="top_${i}" value="קליק">
        <label for="t_click_${i}">✨ קליק</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="t_len_${i}" name="top_${i}" value="עדשים">
        <label for="t_len_${i}">🟢 עדשים</label>
      </div>
    </div>

    <label style="font-size:13px; color:#777;">פיניש:</label>
    <div class="options-grid">
      <div class="option-btn">
        <input type="checkbox" id="e_cream_${i}" name="extra_${i}" value="קצפת">
        <label for="e_cream_${i}">🍦 קצפת</label>
      </div>
      <div class="option-btn">
        <input type="checkbox" id="e_sug_${i}" name="extra_${i}" value="סוכריות">
        <label for="e_sug_${i}">🍬 סוכריות</label>
      </div>
    </div>
  `;
}

// Payment Logic
document.querySelectorAll('input[name="pay"]').forEach(radio => {
  radio.addEventListener('change', (e) => {
    const val = e.target.value;
    const area = document.getElementById('payment-dynamic-area');
    
    if (val === 'ביט') {
      area.innerHTML = `
        <div class="copy-box">
          <span>מספר לביט: <b>${BIT_NUM}</b></span>
          <button class="copy-btn-action" onclick="copyText('${BIT_NUM}', this)">העתק</button>
        </div>
        <button class="btn-app btn-bit" onclick="window.location.href='bit://'">פתח ביט לתשלום</button>
        <div style="font-size:12px; margin-top:5px; color:#555;">* נא לצרף צילום מסך אחרי התשלום</div>
      `;
    } else if (val === 'פייבוקס') {
      area.innerHTML = `
        <div class="copy-box">
          <span>מספר לפייבוקס: <b>${PB_NUM}</b></span>
          <button class="copy-btn-action" onclick="copyText('${PB_NUM}', this)">העתק</button>
        </div>
        <button class="btn-app btn-paybox" onclick="window.location.href='paybox://'">פתח פייבוקס לתשלום</button>
        <div style="font-size:12px; margin-top:5px; color:#555;">* נא לצרף צילום מסך אחרי התשלום</div>
      `;
    } else {
      area.innerHTML = `<div style="background:#fff3cd; padding:10px; border-radius:8px; margin-top:10px; color:#856404;">תשלום במזומן בעת האיסוף.</div>`;
    }
  });
});

async function copyText(text, btn) {
  try {
    await navigator.clipboard.writeText(text);
    btn.classList.add('copied');
    btn.innerText = 'הועתק!';
    setTimeout(() => {
      btn.classList.remove('copied');
      btn.innerText = 'העתק';
    }, 1500);
  } catch(e) { alert('העתקה לא נתמכת, המספר הוא: ' + text); }
}

// Validation & Send
function sendOrder() {
  // Save user data
  const name = document.getElementById('name').value.trim();
  const phone = document.getElementById('phone').value.trim();
  localStorage.setItem('waffle_name', name);
  localStorage.setItem('waffle_phone', phone);

  // Validate
  let valid = true;
  if (!name) { document.getElementById('err-name').style.display = 'block'; document.getElementById('name').classList.add('input-error'); valid = false; }
  else { document.getElementById('err-name').style.display = 'none'; document.getElementById('name').classList.remove('input-error'); }
  
  if (phone.length < 9) { document.getElementById('err-phone').style.display = 'block'; document.getElementById('phone').classList.add('input-error'); valid = false; }
  else { document.getElementById('err-phone').style.display = 'none'; document.getElementById('phone').classList.remove('input-error'); }

  const qty = parseInt(document.getElementById('qty').value) || 0;
  const pay = document.querySelector('input[name="pay"]:checked');
  const notes = document.getElementById('notes').value;

  if (qty === 0 && !notes) {
    document.getElementById('err-qty').style.display = 'block';
    valid = false;
  } else { document.getElementById('err-qty').style.display = 'none'; }

  if (qty > 0 && !pay) {
    document.getElementById('err-pay').style.display = 'block';
    valid = false;
  } else { document.getElementById('err-pay').style.display = 'none'; }

  if (!valid) return;

  const btn = document.getElementById('sendBtn');
  btn.disabled = true;
  btn.innerText = "מכין הודעה... ⏳";

  // Build Message
  const orderId = "WFL-" + Math.floor(Math.random()*10000);
  const time = document.getElementById('time').value || '--:--';
  const payMethod = pay ? pay.value : 'ללא (הזמנה ריקה)';
  const total = qty * PRICE;

  let msg = 
    `🧇 *הזמנה חדשה - וופל בלגי* 🧇\n` +
    `🔢 *קוד:* ${orderId}\n` +
    `➖➖➖➖➖➖➖➖\n` +
    `👤 *שם:* ${name}\n` +
    `📞 *טלפון:* ${phone}\n` +
    `🕒 *איסוף:* ${time}\n` +
    `➖➖➖➖➖➖➖➖\n` +
    `📦 *כמות:* ${qty}\n` +
    `💰 *לתשלום:* ${total} ₪\n` +
    `💳 *אמצעי תשלום:* ${payMethod}\n` +
    `➖➖➖➖➖➖➖➖\n` +
    `📋 *פירוט:*\n`;

  if (qty > 0) {
    for(let i=1; i<=qty; i++) {
      const getVal = (n) => [...document.querySelectorAll(`input[name="${n}_${i}"]:checked`)].map(x=>x.value).join(', ');
      const sauces = getVal('sauce') || 'ללא';
      const tops = getVal('top') || 'ללא';
      const extra = getVal('extra') || 'ללא';
      
      msg += `\n🔸 *וופל ${i}*:\n   🍫 ${sauces}\n   🍪 ${tops}\n   🍦 ${extra}\n`;
    }
  } else {
    msg += `(ללא וופלים - פנייה כללית)\n`;
  }

  if (notes) msg += `\n📣 *הערות:* ${notes}\n`;
  if (payMethod !== 'מזומן' && qty > 0) msg += `\n📸 *נא לצרף אישור תשלום*`;

  // Open WA
  window.open(`https://wa.me/${MY_PHONE}?text=${encodeURIComponent(msg)}`, '_blank');

  // Receipt Logic
  let receipt = 
    `🧾 *קבלה - וופל בלגי* 🧾\n` +
    `תאריך: ${new Date().toLocaleDateString()}\n` +
    `שם: ${name}\n` +
    `סה"כ לתשלום: ${total} ₪ (${payMethod})\n\n` +
    `פירוט:\n${msg.split('פירוט:')[1].split('➖➖')[0]}`; // Hacky slice to get details

  const cleanPhone = phone.replace(/\D/g,'').replace(/^0/,'972');
  document.getElementById('receiptLink').href = `https://wa.me/${cleanPhone}?text=${encodeURIComponent(receipt)}`;
  document.getElementById('receiptBox').style.display = 'block';

  setTimeout(() => {
    btn.disabled = false;
    btn.innerText = "שליחת הזמנה לווטסאפ 🚀";
  }, 2000);
}

function resetForm() {
  if(confirm("לאפס הכל?")) {
    location.reload();
  }
}
</script>

</body>
</html>
