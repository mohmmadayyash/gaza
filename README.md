# gaza
مشروع لتوزيع المياه بشمال غزة 
<!DOCTYPE html><html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تبرع لأهل غزة</title>
  <style>
    body {
      font-family: sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    header {
      background-color: #007c91;
      color: white;
      padding: 1.5rem;
    }
    .logo {
      width: 120px;
      margin: 1rem auto;
    }
    .container {
      max-width: 600px;
      margin: 2rem auto;
      padding: 1.5rem;
      background: white;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    label, input, select, button {
      display: block;
      width: 100%;
      margin-bottom: 1rem;
    }
    input, select {
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      background-color: #28a745;
      color: white;
      padding: 0.75rem;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="تبرع لأهل غزة" class="logo">
    <h1>تبرع لأهل غزة - توزيع المياه</h1>
  </header>
  <div class="container">
    <form id="donationForm">
      <label>الاسم الكامل</label>
      <input type="text" name="name" required><label>رقم الهاتف</label>
  <input type="text" name="phone" required>

  <label>قيمة التبرع (بالدولار)</label>
  <input type="number" name="amount" required>

  <label>طريقة الدفع</label>
  <select name="payment">
    <option value="paypal">PayPal</option>
    <option value="bank">بنك فلسطين</option>
  </select>

  <button type="submit">تبرع الآن</button>
</form>

  </div>  <script>
    document.getElementById('donationForm').addEventListener('submit', function(e) {
      e.preventDefault();

      const data = new FormData(e.target);
      const name = data.get('name');
      const phone = data.get('phone');
      const amount = data.get('amount');
      const payment = data.get('payment');

      const message = `تسجيل تبرع جديد:\nالاسم: ${name}\nالهاتف: ${phone}\nالمبلغ: $${amount}\nطريقة الدفع: ${payment}`;

      // رابط WhatsApp مخصص للإشعار
      const whatsappURL = `https://wa.me/970597895439?text=${encodeURIComponent(message)}`;
      window.open(whatsappURL, '_blank');
    });
  </script></body>
</html>
