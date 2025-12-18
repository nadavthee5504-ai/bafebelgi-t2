<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Waffle Delight | וופל בלגי חם</title>
    <link href="https://fonts.googleapis.com/css2?family=Assistant:wght@400;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --warm-bg: #fffbf5;
            --waffle-gold: #ffb347;
            --chocolate: #5d4037;
            --accent: #ff8c00;
        }

        /* איפוס בסיסי למניעת גלילה לצדדים */
        * { 
            box-sizing: border-box; 
            -webkit-tap-highlight-color: transparent; 
        }
        
        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            max-width: 100%;
            overflow-x: hidden; /* מונע "בריחה" של המסך ימינה או שמאלה */
            background-color: var(--warm-bg);
            color: var(--chocolate);
            font-family: 'Assistant', sans-serif;
        }

        /* באנר עליון מותאם לרוחב מסך טלפון */
        .top-banner {
            background: linear-gradient(135deg, #ffcc33 0%, #ffb347 100%);
            padding: 30px 20px;
            text-align: center;
            border-bottom-left-radius: 40px;
            border-bottom-right-radius: 40px;
            box-shadow: 0 10px 20px rgba(255, 179, 71, 0.2);
            color: white;
            width: 100%;
        }

        .top-banner h1 { 
            margin: 0; 
            font-size: 1.8rem; /* גודל אופטימלי למובייל */
            font-weight: 800; 
            text-shadow: 1px 2px 4px rgba(0,0,0,0.1); 
        }
        
        .top-banner p { margin: 5px 0 0; font-weight: 600; opacity: 0.9; }

        .container {
            width: 100%;
            max-width: 480px; /* רווח מקסימלי שמתאים לטלפונים */
            margin: -25px auto 0;
            padding: 0 15px 140px; /* פדינג תחתון בשביל הפוטר הצף */
        }

        .card {
            background: white;
            border-radius: 25px;
            padding: 20px;
            box-shadow: 0 12px 30px rgba(93, 64, 55, 0.06);
            margin-bottom: 20px;
            border: 1px solid rgba(255, 179, 71, 0.1);
            width: 100%;
        }

        .section-title {
            font-weight: 800;
            font-size: 1.1rem;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .label-text { display: block; font-weight: 700; font-size: 0.9rem; margin-bottom: 8px; }
        .hint { font-size: 0.75rem; color: #999; font-weight: 400; }

        input[type="text"], input[type="tel"], input[type="time"], textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #f2f2f2;
            border-radius: 18px;
            font-family: inherit;
            background: #fafafa;
            transition: 0.3s;
            color: var(--chocolate);
            font-size: 16px; /* מונע זום אוטומטי באייפון */
        }

        input:focus { border-color: var(--waffle-gold); outline: none; background: white; }

        .qty-wrapper {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 25px;
            background: #fff8ee;
            padding: 15px;
            border-radius: 20px;
        }

        .qty-btn {
            width: 45px;
            height: 45px;
            border-radius: 15px;
            border: none;
            background: white;
            font-size: 20px;
            font-weight: 800;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            color: var(--accent);
        }

        #qty-num { font-size: 1.6rem; font-weight: 800; }

        .waffle-box {
            border: 2px solid #f9f9f9;
            border-radius: 20px;
            margin-top: 15px;
            transition: 0.3s;
        }
        .waffle-box.open { border-color: var(--waffle-gold); background: #fffdfa; }

        .waffle-header { padding: 15px; display: flex; justify-content: space-between; cursor: pointer; font-weight: 800; }
        .waffle-content { padding: 0 15px 15px; display: none; }
        .waffle-box.open .waffle-content { display: block; }

        .chips-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 8px; margin-bottom: 15px; }
        .chip-input { display: none; }
        .chip-label {
            padding: 12px;
            background: #f4f4f4;
            border-radius: 14px;
            text-align: center;
            font-size: 0.85rem;
            font-weight: 700;
            cursor: pointer;
            transition: 0.2s;
        }
        .chip-input:checked + .chip-label { background: var(--waffle-gold); color: white; }

        .pay-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            width: 100%;
            padding: 14px;
            border-radius: 15px;
            color: white;
            font-weight: 800;
            margin-top: 10px;
            text-decoration: none;
        }
        .btn-bit { background: #2b5cff; }
        .btn-pb { background: #00bfa5; }

        .copy-box {
            background: #f0f4ff;
            padding: 10px;
            border-radius: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 10px;
            border: 1px dashed #2b5cff;
        }
        .btn-copy { background: white; border: 1px solid #ccc; padding: 6px 10px; border-radius: 8px; font-size: 0.8rem; font-weight: 700; cursor: pointer; }

        .floating-footer {
            position: fixed;
            bottom: 20px;
            left: 15px;
            right: 15px;
            background: var(--chocolate);
            border-radius: 25px;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            z-index: 1000;
        }

        .total-display { color: white; }
        .total-display span { font-size: 0.8rem; opacity: 0.8; display: block; }
        .total-display b { font-size: 1.4rem; }

        .order-now-btn {
            background: var(--waffle-gold);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 18px;
            font-weight: 800;
            font-size: 1.1rem;
            cursor: pointer;
        }

        .hidden { display: none !important; }
    </style>
</head>
<body>

<div class="top-banner">
    <h1>Waffle Delight</h1>
    <p>הפינוק המושלם מחכה לך ✨</p>
</div>

<div class="container">
    <div class="card">
        <div class="section-title">✨ פרטים אישיים</div>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
            <div>
                <span class="label-text">שם מלא</span>
                <input type="text" id="cust-name" placeholder="מי מזמין?">
            </div>
            <div>
                <span class="label-text">טלפון</span>
                <input type="tel" id="cust-phone" placeholder="ליצירת קשר">
            </div>
        </div>
        <div style="margin-top: 15px;">
            <span class="label-text">שעת איסוף <span class="hint">(לא חובה - רק אם בא לך לעזור לנו)</span></span>
            <input type="time" id="cust-time">
        </div>
    </div>

    <div class="card">
        <div class="section-title">🧇 בחרו את הכמות</div>
        <div class="qty-wrapper">
            <button class="qty-btn" onclick="changeQty(-1)">−</button>
            <div id="qty-num">0</div>
            <button class="qty-btn" style="background: var(--waffle-gold); color: white;" onclick="changeQty(1)">+</button>
        </div>
        <div id="waffles-list"></div>
    </div>

    <div id="payment-card" class="card hidden">
        <div class="section-title">💳 תשלום מהיר</div>
        <div style="display: flex; gap: 8px; margin-bottom: 15px;">
            <label style="flex:1;"><input type="radio" name="pay" value="ביט" class="chip-input" onchange="updatePayInfo()"><div class="chip-label">Bit</div></label>
            <label style="flex:1;"><input type="radio" name="pay" value="פייבוקס" class="chip-input" onchange="updatePayInfo()"><div class="chip-label">PayBox</div></label>
            <label style="flex:1;"><input type="radio" name="pay" value="מזומן" class="chip-input" onchange="updatePayInfo()"><div class="chip-label">מזומן</div></label>
        </div>

        <div id="pay-apps" class="hidden">
            <div class="copy-box">
                <span id="display-num" style="font-weight: 800;"></span>
                <button class="btn-copy" onclick="copyNum()">העתק מספר</button>
            </div>
            <a href="bit://" id="bit-link" class="pay-btn btn-bit">פתח Bit ➔</a>
            <a href="paybox://" id="pb-link" class="pay-btn btn-pb">פתח PayBox ➔</a>
        </div>
        <div id="cash-info" class="hidden" style="text-align:center; padding:15px; background:#f9f9f9; border-radius:15px; font-weight:700;">
            💰 התשלום במזומן אצל משפחת טי
        </div>
    </div>

    <div class="card">
        <div class="section-title">💬 הערות מיוחדות</div>
        <textarea id="cust-notes" rows="2" placeholder="אלרגיות או בקשות..."></textarea>
    </div>
</div>

<div class="floating-footer">
    <div class="total-display">
        <span>סה"כ לתשלום</span>
        <b id="total-price">0 ₪</b>
    </div>
    <button class="order-now-btn" id="main-btn" onclick="handleAction()">בואו נזמין!</button>
</div>

<script>
    const CONFIG = {
        price: 7,
        whatsapp: "972542296540",
        bit: "0506205953",
        paybox: "0542296540",
        menu: {
            "רטבים": ["🍫 סירופ שוקולד", "🥞 סירופ מייפל", "🥛 ריבת חלב", "🏠 רוטב הבית"],
            "תוספות": ["⚫ אוראו", "🍪 לוטוס", "✨ קליק", "🟢 עדשים", "🍫 שוקולד צ'יפס"],
            "פיניש": ["🍦 קצפת", "🍬 סוכריות"]
        }
    };

    let state = { qty: 0, step: 1 };

    function changeQty(n) {
        state.qty = Math.max(0, state.qty + n);
        document.getElementById('qty-num').innerText = state.qty;
        document.getElementById('total-price').innerText = `${state.qty * CONFIG.price} ₪`;
        renderWaffles();
    }

    function renderWaffles() {
        const list = document.getElementById('waffles-list');
        const count = list.children.length;
        if (state.qty > count) {
            for (let i = count + 1; i <= state.qty; i++) {
                const div = document.createElement('div');
                div.className = 'waffle-box open';
                div.id = `wbox-${i}`;
                div.innerHTML = `<div class="waffle-header" onclick="toggleWbox(${i})"><span>וופל #${i}</span><span>⌄</span></div><div class="waffle-content"><input type="text" id="wname-${i}" placeholder="שם הוופל (למשל: לאבא)" style="margin-bottom:12px; font-size:16px;">${Object.entries(CONFIG.menu).map(([cat, opts]) => `<div style="font-weight:700; font-size:0.8rem; margin-bottom:5px;">${cat}</div><div class="chips-grid">${opts.map(o => `<label><input type="checkbox" class="chip-input" data-w="${i}" value="${o}"><div class="chip-label">${o}</div></label>`).join('')}</div>`).join('')}</div>`;
                list.appendChild(div);
            }
        } else { while (list.children.length > state.qty) list.lastChild.remove(); }
    }

    function toggleWbox(i) { document.getElementById(`wbox-${i}`).classList.toggle('open'); }

    function updatePayInfo() {
        const method = document.querySelector('input[name="pay"]:checked').value;
        const apps = document.getElementById('pay-apps');
        const cash = document.getElementById('cash-info');
        if(method === 'מזומן') {
            apps.classList.add('hidden');
            cash.classList.remove('hidden');
        } else {
            apps.classList.remove('hidden');
            cash.classList.add('hidden');
            const num = method === 'ביט' ? CONFIG.bit : CONFIG.paybox;
            document.getElementById('display-num').innerText = num;
            document.getElementById('bit-link').style.display = method === 'ביט' ? 'flex' : 'none';
            document.getElementById('pb-link').style.display = method === 'פייבוקס' ? 'flex' : 'none';
        }
    }

    function copyNum() {
        const num = document.getElementById('display-num').innerText;
        navigator.clipboard.writeText(num).then(() => alert('המספר הועתק: ' + num));
    }

    function handleAction() {
        if (state.step === 1) {
            if (state.qty === 0 || !document.getElementById('cust-name').value) return alert('נא למלא שם ולבחור וופל');
            state.step = 2;
            document.getElementById('payment-card').classList.remove('hidden');
            document.getElementById('payment-card').scrollIntoView({ behavior: 'smooth' });
            document.getElementById('main-btn').innerText = 'שלח הזמנה 📲';
        } else {
            const pay = document.querySelector('input[name="pay"]:checked');
            if (!pay) return alert('נא לבחור אמצעי תשלום');
            let orderText = "";
            for (let i = 1; i <= state.qty; i++) {
                const wname = document.getElementById(`wname-${i}`).value;
                const choices = [...document.querySelectorAll(`input[data-w="${i}"]:checked`)].map(c => c.value);
                orderText += `\n*וופל ${i}${wname ? ' ('+wname+')' : ''}:* ${choices.join(', ') || 'בלי תוספות'}`;
            }
            const msg = `🧇 *הזמנה חדשה - Waffle Delight* 🧇\n\n👤 שם: ${document.getElementById('cust-name').value}\n🕒 שעה: ${document.getElementById('cust-time').value || 'בהקדם'}\n💰 סה"כ: ${state.qty * CONFIG.price} ₪\n💳 תשלום: ${pay.value}${pay.value === 'מזומן' ? ' (משפחת טי)' : ''}\n\n*פירוט:*${orderText}\n\n📝 הערות: ${document.getElementById('cust-notes').value || 'אין'}`;
            window.open(`https://wa.me/${CONFIG.whatsapp}?text=${encodeURIComponent(msg)}`);
        }
    }
</script>

</body>
</html>
