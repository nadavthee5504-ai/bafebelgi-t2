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
      --danger: #ff3b30;
      --muted: #777;
    }

    * { box-sizing: border-box; }
    body {
      font-family: 'Rubik', sans-serif;
      background: var(--bg-color);
      margin: 0 !important;
      padding: 0 !important;
      color: var(--text-color);
      padding-bottom: 120px !important;
      overflow-x: hidden;
    }

    .header-hero {
      width: 100%;
      height: 110px;
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      box-shadow: 0 5px 15px rgba(0,0,0,0.15);
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .header-title {
      color: white;
      font-size: 32px;
      font-weight: 700;
      margin: 0;
      text-shadow: 0 1px 3px rgba(0,0,0,0.2);
    }

    .container {
      max-width: 600px;
      width: 95vw;
      margin: -20px auto 0;
      padding: 0 15px;
    }

    .card {
      background: var(--card-bg);
      border-radius: var(--radius);
      padding: 22px;
      box-shadow: var(--shadow);
      margin-bottom: 16px;
    }
    
    /* תוספת קטנה לעיצוב התמונה */
    .waffle-promo-img {
      width: 100%;
      border-radius: 12px;
      display: block;
      margin-bottom: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    .step-title {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 14px;
      color: var(--secondary);
      font-weight: 800;
      font-size: 16px;
    }
    .step-badge {
      width: 28px;
      height: 28px;
      border-radius: 10px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      background: #fff3e6;
      border: 1px solid rgba(255,159,71,0.6);
      color: var(--secondary);
      font-weight: 800;
      flex: 0 0 auto;
    }

    .price-badge {
      background: #fff3e6;
      color: var(--secondary);
      padding: 8px 15px;
      border-radius: 50px;
      font-weight: 700;
      display: inline-block;
      margin-bottom: 12px;
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
      margin-bottom: 16px;
    }
    .phone-btn:hover { background: var(--secondary); color: #fff; }

    label {
      font-size: 14px;
      font-weight: 800;
      color: var(--secondary);
      margin-bottom: 6px;
      display: block;
    }

    input, textarea {
      width: 100%;
      padding: 14px;
      background: #f9f9f9;
      border: 1px solid #e0e0e0;
      border-radius: 12px;
      font-family: inherit;
      font-size: 16px;
      transition: 0.3s;
      outline: none;
    }
    input:focus, textarea:focus {
      border-color: var(--primary);
      background: #fff;
      box-shadow: 0 0 0 3px rgba(255, 159, 71, 0.2);
    }

    /* Quantity */
    .qty-row {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 10px;
    }
    .qty-btn {
      width: 46px;
      height: 46px;
      border-radius: 12px;
      font-size: 22px;
      font-weight: 900;
      cursor: pointer;
      border: 1px solid #ddd;
      background: #fff;
      transition: transform .08s, box-shadow .2s, background .2s;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      user-select: none;
    }
    .qty-btn:hover { box-shadow: 0 6px 16px rgba(0,0,0,0.08); }
    .qty-btn:active { transform: scale(0.97); }
    .qty-btn.plus {
      border: none;
      background: var(--primary);
      color: #fff;
    }
    #qty {
      text-align: center;
      font-size: 20px;
      font-weight: 900;
      width: 80px;
      padding: 10px 8px;
    }

    /* Waffles accordion */
    .waffle-card {
      background: #fff;
      border: 2px solid #eee;
      border-radius: 15px;
      margin-top: 14px;
      overflow: hidden;
      animation: slideIn 0.35s ease;
      position: relative;
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

    .waffle-head {
      padding: 14px 14px 12px 14px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      cursor: pointer;
      user-select: none;
      background: #fff;
    }
    .waffle-title { display: flex; flex-direction: column; gap: 4px; min-width: 0; }
    .waffle-title b { font-size: 16px; color: var(--secondary); }
    .waffle-summary {
      font-size: 12px;
      color: var(--muted);
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      max-width: 420px;
    }
    .chev {
      width: 36px; height: 36px;
      border-radius: 12px;
      border: 1px solid #eee;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
      color: var(--secondary);
      background: #fff;
      transition: transform .2s;
    }
    .waffle-card.open .chev { transform: rotate(180deg); }
    .waffle-body { display: none; padding: 0 14px 14px 14px; }
    .waffle-card.open .waffle-body { display: block; }

    .waffle-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin: 10px 0 14px 0;
    }
    .mini-btn {
      border: 1px solid #e7e7e7;
      background: #fff;
      border-radius: 12px;
      padding: 9px 10px;
      font-weight: 900;
      cursor: pointer;
      font-size: 13px;
      transition: .2s;
    }
    .mini-btn:hover { box-shadow: 0 6px 16px rgba(0,0,0,0.08); }
    .mini-btn.primary { border: none; background: #fff3e6; color: var(--secondary); }

    /* ✅ פידבק לכפתורי השכפול */
    .mini-btn.done {
      background: var(--primary) !important;
      border-color: var(--primary) !important;
      color: #fff !important;
      box-shadow: 0 8px 18px rgba(255,159,71,0.35);
      transform: translateY(-1px);
    }

    .options-grid { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 12px; }
    .option-btn input { display: none; }
    .option-btn label {
      cursor: pointer;
      padding: 9px 14px;
      background: #f0f0f0;
      border-radius: 20px;
      font-size: 14px;
      font-weight: 800;
      color: #555;
      border: 1px solid transparent;
      transition: 0.2s;
      display: flex;
      align-items: center;
      gap: 6px;
      margin: 0;
    }
    .option-btn input:checked + label {
      background: var(--primary);
      color: white;
      box-shadow: 0 4px 10px rgba(255, 159, 71, 0.4);
    }
    .allergen {
      font-size: 11px;
      color: #a04b00;
      background: #fff3e6;
      border: 1px solid rgba(255,159,71,0.45);
      padding: 2px 7px;
      border-radius: 999px;
      font-weight: 900;
    }

    /* Payment */
    .payment-hidden { display: none; }
    .payment-radios { display: flex; gap: 10px; margin-bottom: 10px; }
    .pay-radio input { display: none; }
    .pay-radio label {
      flex: 1;
      text-align: center;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 12px;
      cursor: pointer;
      font-weight: 900;
      transition: 0.2s;
      background: #fff;
    }
    .pay-radio input:checked + label {
      border-color: var(--primary);
      background: #fff8f0;
      color: var(--primary-dark);
    }

    .copy-box {
      background: #fff;
      border: 1px dashed var(--primary);
      padding: 10px;
      border-radius: 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
      font-size: 14px;
      gap: 10px;
    }
    .copy-btn-action {
      background: #eee;
      border: none;
      padding: 7px 10px;
      border-radius: 10px;
      font-weight: 900;
      cursor: pointer;
      font-size: 12px;
      white-space: nowrap;
    }
    .copy-btn-action.copied { background: #4CAF50; color: white; }

    /* ✅ כפתור לפתיחת אפליקציה (החזרנו) */
    .btn-app {
      display: block;
      width: 100%;
      text-align: center;
      padding: 12px;
      border-radius: 12px;
      color: white;
      font-weight: 900;
      text-decoration: none;
      margin-top: 10px;
      border: none;
      cursor: pointer;
      font-size: 16px;
    }
    .btn-bit { background: #2b5cff; }
    .btn-paybox { background: #00bfa5; }

    .hint { font-size: 12px; color: #555; margin-top: 8px; line-height: 1.4; font-weight: 700; }
    .warn { background:#fff3cd; padding:10px; border-radius:10px; margin-top:10px; color:#856404; border: 1px solid rgba(133,100,4,0.25); font-weight: 800; }

    /* Errors */
    .error-msg { color: var(--danger); font-size: 12px; display: none; margin-top: 6px; font-weight: 900; }
    .input-error { border-color: var(--danger) !important; }

    /* Receipt */
    .receipt-section {
      display: none;
      margin-top: 14px;
      background: #e6ffed;
      padding: 15px;
      border-radius: 12px;
      text-align: center;
      border: 1px solid #b7eac5;
    }
    .receipt-link {
      display: block;
      color: white;
      padding: 12px 20px;
      border-radius: 12px;
      text-decoration: none;
      font-weight: 900;
      background: #25D366;
      box-shadow: 0 4px 12px rgba(37, 211, 102, 0.4);
      font-size: 18px;
      margin-top: 12px;
    }

    .btn-reset {
      background: none;
      border: none;
      color: #999;
      text-decoration: underline;
      margin-top: 12px;
      width: 100%;
      cursor: pointer;
      font-weight: 900;
    }

    /* Sticky bottom bar */
    .sticky-bar {
      position: fixed;
      left: 0; right: 0; bottom: 0;
      background: rgba(255,255,255,0.92);
      backdrop-filter: blur(8px);
      border-top: 1px solid rgba(0,0,0,0.06);
      padding: 10px 12px;
      z-index: 9999;
    }
    .sticky-inner {
      max-width: 600px;
      margin: 0 auto;
      display: flex;
      gap: 10px;
      align-items: center;
      justify-content: space-between;
    }
    .total-pill {
      flex: 1;
      border-radius: 14px;
      padding: 10px 12px;
      background: #fff;
      box-shadow: 0 6px 18px rgba(0,0,0,0.06);
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      min-width: 0;
      transition: transform .15s;
    }
    /* ✅ אנימציה קטנה לסה״כ */
    .total-pill.bump { transform: scale(1.02); }

    .total-pill .t1 { font-weight: 900; color: var(--secondary); }
    .total-pill .t2 { font-weight: 900; color: var(--secondary); font-size: 18px; white-space: nowrap; }

    .btn-main {
      border: none;
      border-radius: 14px;
      padding: 14px 14px;
      font-size: 16px;
      font-weight: 900;
      cursor: pointer;
      color: #fff;
      background: linear-gradient(135deg, #ff9f47, #ff8520);
      box-shadow: 0 8px 18px rgba(255, 133, 32, 0.35);
      transition: transform .08s, filter .2s;
      white-space: nowrap;
    }
    .btn-main:active { transform: scale(0.98); }
    .btn-main:disabled { filter: grayscale(0.4); opacity: 0.7; cursor: not-allowed; }

    .small-note {
      text-align:center;
      margin-top: 14px;
      font-size: 13px;
      color:#888;
      font-weight: 800;
      line-height: 1.3;
    }
    .focus-ring:focus-visible { box-shadow: 0 0 0 3px rgba(37, 211, 102, 0.25); }
  </style>
</head>

<body>
  <div class="header-hero">
    <h1 class="header-title">וופל בלגי על מקל 🧇</h1>
  </div>

  <div class="container">

    <div class="card" style="text-align: center; padding: 10px;">
        <img src="https://lh3.googleusercontent.com/d/1A3muQYsX909oRKPHZNZQYZ6ny2XpRTYz" class="waffle-promo-img" alt="וופל בלגי על מקל">
        <div style="font-weight: 800; color: var(--secondary); font-size: 18px;">הוופל הכי טעים בשכונה! 😍</div>
    </div>

    <div class="card">
      <div class="step-title"><span class="step-badge">1</span> פרטים</div>
      <div style="text-align:center;">
        <span class="price-badge">רק 7 ש"ח לוופל!</span>
      </div>
      <a href="tel:0542296540" class="phone-btn focus-ring">📞 להזמנות: 054-2296540</a>

      <label for="name">שם מלא <span style="color:var(--danger)">*</span></label>
      <input class="focus-ring" type="text" id="name" placeholder="איך קוראים לך?" autocomplete="name">
      <div id="err-name" class="error-msg">נא למלא שם</div>

      <label for="phone" style="margin-top:14px">טלפון <span style="color:var(--danger)">*</span></label>
      <input class="focus-ring" type="tel" id="phone" placeholder="מספר נייד (למשל 05XXXXXXXX)" inputmode="tel" autocomplete="tel">
      <div id="err-phone" class="error-msg">נא למלא טלפון ישראלי תקין</div>

      <label for="time" style="margin-top:14px">שעה לאיסוף</label>
      <input class="focus-ring" type="time" id="time">
    </div>

    <div class="card">
      <div class="step-title"><span class="step-badge">2</span> בחירת וופלים</div>

      <label style="font-size:18px;">כמה וופלים לפנק? 😋</label>
      <div class="qty-row">
        <button class="qty-btn focus-ring" id="minusBtn" type="button" aria-label="הפחת כמות">−</button>
        <input class="focus-ring" type="number" id="qty" value="0" min="0" aria-label="כמות וופלים">
        <button class="qty-btn plus focus-ring" id="plusBtn" type="button" aria-label="הוסף כמות">+</button>
      </div>
      <div id="err-qty" class="error-msg">יש לבחור כמות או למלא הערות</div>

      <div id="waffles-container"></div>
    </div>

    <div id="payment-section" class="card payment-hidden">
      <div class="step-title"><span class="step-badge">3</span> תשלום</div>

      <label>איך תרצו לשלם? <span style="color:var(--danger)">*</span></label>
      <div class="payment-radios">
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_bit" value="ביט">
          <label class="focus-ring" for="p_bit">ביט</label>
        </div>
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_pb" value="פייבוקס">
          <label class="focus-ring" for="p_pb">פייבוקס</label>
        </div>
        <div class="pay-radio">
          <input type="radio" name="pay" id="p_cash" value="מזומן">
          <label class="focus-ring" for="p_cash">מזומן</label>
        </div>
      </div>

      <div id="err-pay" class="error-msg">נא לבחור אמצעי תשלום</div>
      <div id="payment-dynamic-area"></div>
    </div>

    <div class="card">
      <div class="step-title"><span class="step-badge">4</span> הערות</div>

      <label for="notes">הערות / בקשות מיוחדות</label>
      <textarea class="focus-ring" id="notes" rows="3" placeholder="כאן אפשר לכתוב כל דבר נוסף..."></textarea>

      <div id="receiptBox" class="receipt-section">
        <div style="font-weight:900; color:#155724; margin-bottom:6px;">ההזמנה נשלחה בהצלחה!</div>
        <div style="font-size:14px; color:#333; font-weight:700;">לחץ לשליחת אישור קבלה לנייד שלך:</div>
        <a id="receiptLink" href="#" target="_blank" class="receipt-link focus-ring">שלח לי קבלה 📲</a>
      </div>

      <button class="btn-reset focus-ring" id="resetBtn" type="button">איפוס טופס</button>

      <div class="small-note">
        ⭐ חובה ללחוץ על "שלח" בתוך הוואטסאפ כדי שההזמנה תתקבל
      </div>
    </div>

  </div>

  <div class="sticky-bar">
    <div class="sticky-inner">
      <div class="total-pill" id="totalPill" aria-live="polite">
        <span class="t1">סה״כ</span>
        <span class="t2" id="totalAmount">0 ₪</span>
      </div>
      <button class="btn-main focus-ring" id="sendBtn" type="button">שליחת הזמנה 🚀</button>
    </div>
  </div>

  <script>
    const PRICE = 7;
    const MY_PHONE = "972542296540";
    const BIT_NUM = "0506205953";
    const PB_NUM  = "0542296540";

    const state = {
      waffles: [],
      checkoutMode: false,   // ✅ חדש: רק בסוף חושפים תשלום
    };

    const $ = (id) => document.getElementById(id);

    function ensureWaffle(i) {
      if (!state.waffles[i-1]) {
        state.waffles[i-1] = { name: "", sauce: [], top: [], extra: [] };
      }
      return state.waffles[i-1];
    }

    document.addEventListener('DOMContentLoaded', () => {
      const savedName  = localStorage.getItem('waffle_name');
      const savedPhone = localStorage.getItem('waffle_phone');
      if (savedName)  $('name').value  = savedName;
      if (savedPhone) $('phone').value = savedPhone;

      $('plusBtn').addEventListener('click', () => changeQty(1));
      $('minusBtn').addEventListener('click', () => changeQty(-1));
      $('qty').addEventListener('input', updateUI);

      $('resetBtn').addEventListener('click', resetForm);
      $('sendBtn').addEventListener('click', onSendClick);

      document.querySelectorAll('input[name="pay"]').forEach(radio => {
        radio.addEventListener('change', onPaymentChange);
      });

      $('waffles-container').addEventListener('input', handleWaffleInputChange);
      $('waffles-container').addEventListener('change', handleWaffleInputChange);
      $('waffles-container').addEventListener('click', handleWaffleClicks);

      updateUI();
    });

    function changeQty(delta) {
      const el = $('qty');
      let val = parseInt(el.value) || 0;
      val += delta;
      if (val < 0) val = 0;
      el.value = val;

      // אם המשתמש שינה כמות באמצע checkout – נשאר ב-checkout אבל נעדכן UI
      updateUI();
    }

    function updateUI() {
      const qty = parseInt($('qty').value) || 0;
      const total = qty * PRICE;
      $('totalAmount').innerText = `${total} ₪`;

      // ✅ אנימציית "באמפ" קטנה לסה״כ
      const pill = $('totalPill');
      pill.classList.add('bump');
      setTimeout(() => pill.classList.remove('bump'), 160);

      renderWaffles(qty);

      // ✅ תשלום רק אם checkoutMode פעיל וגם qty>0
      if (state.checkoutMode && qty > 0) {
        $('payment-section').classList.remove('payment-hidden');
      } else {
        $('payment-section').classList.add('payment-hidden');
        // נקה בחירת תשלום כשחבוי
        document.querySelectorAll('input[name="pay"]').forEach(r => r.checked = false);
        $('payment-dynamic-area').innerHTML = '';
      }

      for (let i=1; i<=qty; i++) updateWaffleSummary(i);
    }

    function renderWaffles(qty) {
      const container = $('waffles-container');
      const existing = container.querySelectorAll('.waffle-card').length;

      if (qty > existing) {
        for (let i = existing + 1; i <= qty; i++) {
          ensureWaffle(i);
          const div = document.createElement('div');
          div.className = 'waffle-card open';
          div.dataset.index = String(i);
          div.innerHTML = getWaffleHTML(i);
          container.appendChild(div);
          applyWaffleStateToDOM(i);
          updateWaffleSummary(i);
        }
      }

      if (qty < existing) {
        const cards = [...container.querySelectorAll('.waffle-card')];
        for (let i = cards.length; i > qty; i--) cards[i-1].remove();
      }
    }

    function getWaffleHTML(i) {
      return `
        <div class="waffle-head" role="button" tabindex="0" aria-expanded="true" aria-controls="waffle_body_${i}">
          <div class="waffle-title">
            <b>🧇 וופל #${i}</b>
            <div class="waffle-summary" id="waffle_summary_${i}">—</div>
          </div>
          <div class="chev" aria-hidden="true">⌄</div>
        </div>

        <div class="waffle-body" id="waffle_body_${i}">
          <div class="waffle-actions">
            <button class="mini-btn primary focus-ring" type="button" data-action="copy-next" data-index="${i}">שכפל לוופל הבא</button>
            <button class="mini-btn focus-ring" type="button" data-action="copy-all" data-index="${i}">העתק לכל הוופלים</button>
            <button class="mini-btn focus-ring" type="button" data-action="clear" data-index="${i}">נקה וופל</button>
          </div>

          <label for="waffle_name_${i}" style="font-size:14px; color:var(--primary-dark);">איך אתה קורא לוופל שלך?</label>
          <input class="focus-ring" type="text" id="waffle_name_${i}" data-field="name" data-index="${i}" placeholder="שם הוופל (אופציונלי)" style="margin-bottom: 14px;">

          <label style="font-size:13px; color:#777;">רטבים:</label>
          <div class="options-grid">
            ${opt(i,'sauce','סירופ שוקולד','🍫 סירופ שוקולד')}
            ${opt(i,'sauce','סירופ מייפל','🥞 סירופ מייפל')}
            ${opt(i,'sauce','ריבת חלב','🥛 ריבת חלב ')}
            ${opt(i,'sauce','רוטב הבית','🏠 רוטב הבית')}
          </div>

          <label style="font-size:13px; color:#777;">תוספות:</label>
          <div class="options-grid">
            ${opt(i,'top','אוראו','⚫ אוראו')}
            ${opt(i,'top','לוטוס','🍪 לוטוס')}
            ${opt(i,'top','קליק','✨ קליק')}
            ${opt(i,'top','עדשים','🟢 עדשים')}
          </div>

          <label style="font-size:13px; color:#777;">פיניש:</label>
          <div class="options-grid">
            ${opt(i,'extra','קצפת','🍦 קצפת ')}
            ${opt(i,'extra','סוכריות','🍬 סוכריות')}
            ${opt(i,'extra','שוקולד צ׳יפס','🍫 שוקולד צ׳יפס')}
          </div>
        </div>
      `;
    }

    function opt(i, group, value, labelHtml) {
      const id = `${group}_${i}_${slug(value)}`;
      return `
        <div class="option-btn">
          <input type="checkbox" id="${id}" data-field="${group}" data-index="${i}" value="${escapeHtml(value)}">
          <label class="focus-ring" for="${id}">${labelHtml}</label>
        </div>
      `;
    }
    function slug(s) { return String(s).replace(/\s+/g,'_').replace(/[^\w\u0590-\u05FF]+/g,''); }

    function handleWaffleClicks(e) {
      const head = e.target.closest('.waffle-head');
      if (head) {
        const card = head.closest('.waffle-card');
        toggleAccordion(card, head);
        return;
      }

      const btn = e.target.closest('button[data-action]');
      if (!btn) return;

      const action = btn.dataset.action;
      const i = parseInt(btn.dataset.index, 10);

      if (action === 'clear') {
        state.waffles[i-1] = { name: "", sauce: [], top: [], extra: [] };
        applyWaffleStateToDOM(i);
        updateWaffleSummary(i);
        flashButton(btn, 'נוקה ✅');
        return;
      }

      if (action === 'copy-next') {
        const qty = parseInt($('qty').value) || 0;
        if (i >= qty) { flashButton(btn, 'אין וופל הבא'); return; }
        state.waffles[i] = deepClone(state.waffles[i-1]);
        applyWaffleStateToDOM(i+1);
        updateWaffleSummary(i+1);
        flashButton(btn, 'שוכפל ✅');
        return;
      }

      if (action === 'copy-all') {
        const qty = parseInt($('qty').value) || 0;
        for (let k=1; k<=qty; k++) {
          if (k === i) continue;
          state.waffles[k-1] = deepClone(state.waffles[i-1]);
          applyWaffleStateToDOM(k);
          updateWaffleSummary(k);
        }
        flashButton(btn, 'הועתק ✅');
        return;
      }
    }

    function flashButton(btn, tempText) {
      const oldText = btn.textContent;
      btn.classList.add('done');
      btn.textContent = tempText;
      setTimeout(() => {
        btn.classList.remove('done');
        btn.textContent = oldText;
      }, 1200);
    }

    function toggleAccordion(card, head) {
      const isOpen = card.classList.contains('open');
      card.classList.toggle('open', !isOpen);
      head.setAttribute('aria-expanded', String(!isOpen));
    }

    document.addEventListener('keydown', (e) => {
      if (e.key !== 'Enter' && e.key !== ' ') return;
      const head = e.target.closest('.waffle-head');
      if (!head) return;
      e.preventDefault();
      const card = head.closest('.waffle-card');
      toggleAccordion(card, head);
    });

    function handleWaffleInputChange(e) {
      const el = e.target;
      const idx = parseInt(el.dataset.index || '', 10);
      const field = el.dataset.field;
      if (!idx || !field) return;

      ensureWaffle(idx);

      if (field === 'name') {
        state.waffles[idx-1].name = el.value.trim();
      } else if (field === 'sauce' || field === 'top' || field === 'extra') {
        const checked = [...document.querySelectorAll(`input[type="checkbox"][data-index="${idx}"][data-field="${field}"]:checked`)]
          .map(x => x.value);
        state.waffles[idx-1][field] = checked;
      }
      updateWaffleSummary(idx);
    }

    function applyWaffleStateToDOM(i) {
      const w = ensureWaffle(i);
      const nameEl = $(`waffle_name_${i}`);
      if (nameEl) nameEl.value = w.name || '';

      ['sauce','top','extra'].forEach(group => {
        const boxes = document.querySelectorAll(`input[type="checkbox"][data-index="${i}"][data-field="${group}"]`);
        boxes.forEach(b => b.checked = (w[group] || []).includes(b.value));
      });
    }

    function updateWaffleSummary(i) {
      const w = ensureWaffle(i);
      const parts = [];
      const nm = (w.name || '').trim();
      if (nm) parts.push(`“${nm}”`);
      if ((w.sauce||[]).length) parts.push(`רטבים: ${(w.sauce||[]).join(', ')}`);
      if ((w.top||[]).length) parts.push(`תוספות: ${(w.top||[]).join(', ')}`);
      if ((w.extra||[]).length) parts.push(`פיניש: ${(w.extra||[]).join(', ')}`);

      const text = parts.length ? parts.join(' | ') : 'עדיין לא בחרת תוספות';
      const el = $(`waffle_summary_${i}`);
      if (el) el.textContent = text;
    }

    /** ✅ תשלום בסוף: קליק ראשון = כניסה ל-checkout (גילוי תשלום)
        קליק שני = שליחה סופית (אחרי בחירת תשלום) */
    function onSendClick() {
      const qty = parseInt($('qty').value) || 0;

      // אימות בסיסי לפני מעבר ל-checkout (כמו “סיום הזמנה”)
      const name = $('name').value.trim();
      const phoneRaw = $('phone').value.trim();

      localStorage.setItem('waffle_name', name);
      localStorage.setItem('waffle_phone', phoneRaw);

      let ok = true;
      if (!name) { showError('err-name','name'); ok = false; } else hideError('err-name','name');

      const cleanPhone = normalizeILPhone(phoneRaw);
      if (!cleanPhone) { showError('err-phone','phone'); ok = false; } else hideError('err-phone','phone');

      const notes = $('notes').value.trim();
      if (qty === 0 && !notes) { $('err-qty').style.display = 'block'; ok = false; } else $('err-qty').style.display = 'none';

      if (!ok) return;

      // אם עוד לא ב-checkout — נכנסים אליו ומראים תשלום
      if (!state.checkoutMode) {
        state.checkoutMode = true;
        updateUI();

        // גלילה לתשלום
        $('payment-section').scrollIntoView({ behavior: 'smooth', block: 'start' });

        $('sendBtn').textContent = 'שליחה סופית ✅';
        return;
      }

      // כבר ב-checkout => חייבים אמצעי תשלום אם qty>0
      const pay = document.querySelector('input[name="pay"]:checked');
      if (qty > 0 && !pay) {
        $('err-pay').style.display = 'block';
        $('payment-section').scrollIntoView({ behavior: 'smooth', block: 'start' });
        return;
      }
      $('err-pay').style.display = 'none';

      // שליחה סופית
      sendOrder(cleanPhone);
    }

    /** ✅ החזרנו כפתור פתיחת אפליקציה + נשארה העתקה */
    function onPaymentChange(e) {
      const val = e.target.value;
      const area = $('payment-dynamic-area');

      if (val === 'ביט') {
        area.innerHTML = `
          <div class="copy-box">
            <span>מספר לביט: <b>${BIT_NUM}</b></span>
            <button class="copy-btn-action focus-ring" type="button" data-copy="${BIT_NUM}">העתק</button>
          </div>
          <button class="btn-app btn-bit focus-ring" type="button" id="openBitBtn">פתח ביט לתשלום</button>
          <div class="hint">אם לא נפתח — פתח ביט ידנית ושלח לפי המספר 👆</div>
          <div class="hint"><b>* נא לצרף צילום מסך אחרי התשלום</b></div>
        `;
        $('openBitBtn').addEventListener('click', () => openAppLink('bit://'));
      } else if (val === 'פייבוקס') {
        area.innerHTML = `
          <div class="copy-box">
            <span>מספר לפייבוקס: <b>${PB_NUM}</b></span>
            <button class="copy-btn-action focus-ring" type="button" data-copy="${PB_NUM}">העתק</button>
          </div>
          <button class="btn-app btn-paybox focus-ring" type="button" id="openPbBtn">פתח פייבוקס לתשלום</button>
          <div class="hint">אם לא נפתח — פתח פייבוקס ידנית ושלח לפי המספר 👆</div>
          <div class="hint"><b>* נא לצרף צילום מסך אחרי התשלום</b></div>
        `;
        $('openPbBtn').addEventListener('click', () => openAppLink('paybox://'));
      } else {
        area.innerHTML = `<div class="warn">תשלום במזומן בעת האיסוף.</div>`;
      }
    }

    // ניסיון פתיחת אפליקציה (אין דרך 100% לדעת אם נפתח, אז אנחנו נותנים fallback ברור)
    function openAppLink(uri) {
      try {
        window.location.href = uri;
      } catch (e) {
        alert('לא הצלחתי לפתוח את האפליקציה אוטומטית. פתח ידנית ושלם לפי המספר שמופיע.');
      }
    }

    /** copy buttons */
    document.addEventListener('click', async (e) => {
      const btn = e.target.closest('button[data-copy]');
      if (!btn) return;
      const text = btn.getAttribute('data-copy');
      await copyTextSmart(text, btn);
    });

    async function copyTextSmart(text, btn) {
      try {
        await navigator.clipboard.writeText(text);
        btn.classList.add('copied');
        btn.innerText = 'הועתק!';
        setTimeout(() => {
          btn.classList.remove('copied');
          btn.innerText = 'העתק';
        }, 1400);
      } catch (e) {
        const tmp = document.createElement('input');
        tmp.value = text;
        tmp.style.position = 'fixed';
        tmp.style.left = '-9999px';
        document.body.appendChild(tmp);
        tmp.focus(); tmp.select();
        alert('העתקה אוטומטית לא נתמכת כאן. סימנתי לך את המספר להעתקה ידנית: ' + text);
        document.body.removeChild(tmp);
      }
    }

    function normalizeILPhone(raw) {
      let d = String(raw || '').replace(/\D/g, '');
      if (d.startsWith('972')) {
        d = '972' + d.slice(3).replace(/^0+/, '');
        return d.length >= 11 ? d : null;
      }
      if (d.startsWith('0')) d = d.slice(1);
      if (d.length === 9 && d.startsWith('5')) return '972' + d;
      return null;
    }

    function showError(id, inputId) {
      $(id).style.display = 'block';
      if (inputId) $(inputId).classList.add('input-error');
    }
    function hideError(id, inputId) {
      $(id).style.display = 'none';
      if (inputId) $(inputId).classList.remove('input-error');
    }

    /** ✅ sendOrder מקבל cleanPhone שכבר נבדק */
    function sendOrder(cleanPhone) {
      const name = $('name').value.trim();
      const phoneRaw = $('phone').value.trim();

      const qty = parseInt($('qty').value) || 0;
      const pay = document.querySelector('input[name="pay"]:checked');
      const notes = $('notes').value.trim();

      const btn = $('sendBtn');
      btn.disabled = true;
      btn.textContent = "שולח... ⏳";

      const orderId = "WFL-" + Math.floor(Math.random()*10000);
      const time = $('time').value || '--:--';
      const payMethod = pay ? pay.value : 'ללא';
      const total = qty * PRICE;

      let msg =
        `🧇 *הזמנה חדשה - וופל בלגי* 🧇\n` +
        `🔢 *קוד:* ${orderId}\n` +
        `➖➖➖➖➖➖➖➖\n` +
        `👤 *שם:* ${name}\n` +
        `📞 *טלפון:* ${phoneRaw}\n` +
        `🕒 *איסוף:* ${time}\n` +
        `➖➖➖➖➖➖➖➖\n` +
        `📦 *כמות:* ${qty}\n` +
        `💰 *לתשלום:* ${total} ₪\n` +
        `💳 *אמצעי תשלום:* ${payMethod}\n` +
        `➖➖➖➖➖➖➖➖\n` +
        `📋 *פירוט:*\n`;

      let detailsText = '';
      if (qty > 0) {
        for (let i=1; i<=qty; i++) {
          const w = ensureWaffle(i);
          const title = (w.name && w.name.trim()) ? `*וופל ${i} - ${w.name.trim()}*` : `*וופל ${i}*`;
          const sauces = (w.sauce||[]).length ? (w.sauce||[]).join(', ') : 'ללא';
          const tops   = (w.top||[]).length ? (w.top||[]).join(', ') : 'ללא';
          const extra  = (w.extra||[]).length ? (w.extra||[]).join(', ') : 'ללא';

          const waffleDetails =
            `\n🔸 ${title}:\n` +
            `   🍫 רטבים: ${sauces}\n` +
            `   🍪 תוספות: ${tops}\n` +
            `   🍦 פיניש: ${extra}\n`;

          msg += waffleDetails;
          detailsText += waffleDetails;
        }
      } else {
        msg += `(ללא וופלים - פנייה כללית)\n`;
        detailsText = '(אין וופלים בהזמנה זו)';
      }

      if (notes) msg += `\n📣 *הערות:* ${notes}\n`;
      if (payMethod !== 'מזומן' && qty > 0) msg += `\n📸 *נא לצרף אישור תשלום*`;

      window.open(`https://wa.me/${MY_PHONE}?text=${encodeURIComponent(msg)}`, '_blank');

      const receipt =
        `🧾 *קבלה - וופל בלגי* 🧾\n` +
        `שלום ${name}!\n` +
        `תאריך: ${new Date().toLocaleDateString('he-IL')}\n` +
        `➖➖➖➖➖➖➖➖\n` +
        `💰 *סה"כ לתשלום:* ${total} ₪\n` +
        `💳 *אמצעי תשלום:* ${payMethod}\n` +
        `🕒 *איסוף משוער:* ${time}\n` +
        `➖➖➖➖➖➖➖➖\n` +
        `*פירוט הזמנה:*\n${detailsText}\n` +
        `תודה רבה שהזמנת מאיתנו! נתראה בקרוב! ✨`;

      $('receiptLink').href = `https://wa.me/${cleanPhone}?text=${encodeURIComponent(receipt)}`;
      $('receiptBox').style.display = 'block';

      setTimeout(() => {
        btn.disabled = false;
        btn.textContent = 'שליחה סופית ✅';
      }, 1200);
    }

    function resetForm() {
      const resetAll = confirm("לאפס את הטופס?\n(שם וטלפון יישארו שמורים)");
      if (!resetAll) return;

      $('time').value = '';
      $('notes').value = '';
      $('qty').value = 0;
      $('waffles-container').innerHTML = '';
      $('receiptBox').style.display = 'none';

      document.querySelectorAll('input[name="pay"]').forEach(r => r.checked = false);
      $('payment-dynamic-area').innerHTML = '';
      $('payment-section').classList.add('payment-hidden');

      ['err-name','err-phone','err-qty','err-pay'].forEach(id => $(id).style.display = 'none');
      ['name','phone'].forEach(id => $(id).classList.remove('input-error'));

      state.waffles = [];
      state.checkoutMode = false;
      $('sendBtn').textContent = 'שליחת הזמנה 🚀';

      updateUI();

      const clearSaved = confirm("למחוק גם שם וטלפון שמורים?");
      if (clearSaved) {
        localStorage.removeItem('waffle_name');
        localStorage.removeItem('waffle_phone');
        $('name').value = '';
        $('phone').value = '';
      }
    }

    function deepClone(obj) { return JSON.parse(JSON.stringify(obj)); }
    function escapeHtml(s) {
      return String(s).replace(/[&<>"']/g, (m) => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#039;'}[m]));
    }
  </script>

</body>
</html>
