# 📧 EmailJS Setup Guide - Japan Market

## Бэлтгэл

### 1. EmailJS Account үүсгэх
1. **https://www.emailjs.com/** руу орж бүртгүүлнэ
2. Email хаягаа баталгаажуулна
3. Dashboard руу нэвтэрнэ

---

## Email Service холбох

### 2. Gmail Service нэмэх
1. Dashboard дээр **"Email Services"** дарна
2. **"Add New Service"** дарна
3. **Gmail** сонгоно
4. **"Connect Account"** дарж Gmail нэвтэрнэ
5. **Service ID** хуулж авна (Жишээ: `service_abc123`)

---

## Email Template үүсгэх

### 3. Template үүсгэх
1. Dashboard дээр **"Email Templates"** дарна
2. **"Create New Template"** дарна
3. **Template Name:** `japan_market_order`
4. Доорх template-ийг хуулж буулгана:

#### **Subject:**
```
🇯🇵 Japan Market - Захиалга #{{order_number}}
```

#### **Content (HTML):**
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background: #f9f9f9;
        }
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            text-align: center;
            border-radius: 10px 10px 0 0;
        }
        .content {
            background: white;
            padding: 30px;
            border-radius: 0 0 10px 10px;
        }
        .info-row {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        .info-label {
            font-weight: bold;
            color: #667eea;
        }
        .items-list {
            background: #f5f5f5;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
        }
        .total {
            font-size: 1.5rem;
            color: #667eea;
            font-weight: bold;
            text-align: right;
            margin-top: 20px;
        }
        .footer {
            text-align: center;
            margin-top: 20px;
            color: #999;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🇯🇵 JAPAN MARKET</h1>
            <h2>Захиалгын баталгаажуулалт</h2>
        </div>
        
        <div class="content">
            <p>Сайн байна уу, <strong>{{user_name}}</strong>!</p>
            <p>Таны захиалгыг хүлээн авлаа. Баярлалаа! 🎉</p>
            
            <div class="info-row">
                <span class="info-label">📋 Захиалгын дугаар:</span>
                <span>{{order_number}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">📅 Огноо:</span>
                <span>{{order_date}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">👤 Хэрэглэгч:</span>
                <span>{{user_email}}</span>
            </div>
            
            <h3>🛍️ Захиалсан бараа:</h3>
            <div class="items-list">
                <pre>{{items_list}}</pre>
            </div>
            
            <div class="info-row">
                <span class="info-label">💰 Дэд дүн:</span>
                <span>{{subtotal}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">🎫 Хөнгөлөлт:</span>
                <span>{{discount}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">📦 Хүргэлт:</span>
                <span>{{shipping}}</span>
            </div>
            
            <div class="total">
                Нийт: {{total}}
            </div>
            
            <hr>
            
            <div class="info-row">
                <span class="info-label">💳 Төлбөрийн хэлбэр:</span>
                <span>{{payment_method}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">🚚 Хүргэлтийн хэлбэр:</span>
                <span>{{delivery_method}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">📍 Хаяг:</span>
                <span><pre>{{address}}</pre></span>
            </div>
            
            <div class="info-row">
                <span class="info-label">🎫 Промо код:</span>
                <span>{{promo_code}}</span>
            </div>
            
            <div class="info-row">
                <span class="info-label">📝 Тэмдэглэл:</span>
                <span>{{notes}}</span>
            </div>
            
            <hr>
            
            <p><strong>Дараагийн алхам:</strong></p>
            <ul>
                <li>✅ Таны захиалга боловсруулагдаж байна</li>
                <li>📦 Бэлтгэж дууссаны дараа мэдэгдэх болно</li>
                <li>🚚 Хүргэлтийн мэдээллийг SMS/Email-ээр илгээнэ</li>
            </ul>
            
            <p>Асуулт байвал бидэнтэй холбогдоорой:</p>
            <p>📧 support@japanmarket.mn<br>
            📱 +976 9999-9999</p>
        </div>
        
        <div class="footer">
            <p>© 2025 Japan Market - Япон бараа шууд Монголд</p>
            <p>Энэхүү и-мэйл автомат илгээгдсэн.</p>
        </div>
    </div>
</body>
</html>
```

5. **Save** дарна
6. **Template ID** хуулж авна (Жишээ: `template_xyz789`)

---

## Public Key авах

### 4. Public Key олох
1. Dashboard дээр **"Account"** руу орно
2. **"API Keys"** хэсэгт орно
3. **Public Key** хуулж авна (Жишээ: `user_abc123xyz`)

---

## Code-д холбох

### 5. japan_script.js файл засах

`japan_script.js` файлын **437 мөрийг** засна:

```javascript
// Өмнө:
emailjs.init("YOUR_PUBLIC_KEY");

// Дараа (өөрийн Public Key оруулна):
emailjs.init("user_abc123xyz");
```

**1803 мөрийг** засна:

```javascript
// Өмнө:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)

// Дараа (өөрийн Service ID болон Template ID оруулна):
emailjs.send('service_abc123', 'template_xyz789', templateParams)
```

---

## Туршилт

### 6. Test хийх

1. Browser дээр `index.html` нээнэ
2. Бараа сонгоод **"⚡ Худалдаж авах"** дарна
3. Төлбөрийн мэдээлэл бөглөнө
4. **"Төлбөр төлөх"** дарна
5. Gmail-аа шалгана:
   - **Захиалгын баталгаажуулалт** ирсэн эсэхийг харна
   - tsewegmidmonhotgon@gmail.com хаяг руу очсон эсэхийг шалгана

---

## Анхаарах зүйлс

### ⚠️ Important Notes:

1. **EmailJS Free Plan:**
   - Сард 200 и-мэйл үнэгүй
   - Хэрэв илүү их хэрэгтэй бол upgrade хийнэ

2. **Gmail Settings:**
   - "Less secure app access" асаалттай байх хэрэггүй
   - OAuth2 автомат ажиллана

3. **Admin Email:**
   - Одоогоор `tsewegmidmonhotgon@gmail.com` руу очно
   - Өөрчлөхийг хүсвэл `sendOrderEmail` функц дотор `to_email` өөрчилнө

4. **Testing:**
   - Эхлээд test email илгээж үзнэ үү
   - Spam folder-т ороогүй эсэхийг шалгана

---

## Troubleshooting

### ❌ Хэрэв и-мэйл ирэхгүй бол:

1. **Console шалгах:**
   ```javascript
   F12 → Console tab
   // Алдааны мэдээлэл харагдах
   ```

2. **EmailJS Dashboard шалгах:**
   - Usage statistics харах
   - Failed sends байгаа эсэхийг шалгах

3. **Spam folder шалгах**

4. **Email Service status шалгах:**
   - Gmail service холболт идэвхтэй эсэх

---

## Хувилбар сайжруулалт

### 💡 Дараагийн удаа нэмж болох:

1. **Customer Email:** Хэрэглэгч өөртөө ч и-мэйл авах
2. **Order Status Updates:** Захиалгын статус өөрчлөгдөх бүрт и-мэйл
3. **SMS Notification:** Утсаар мэдэгдэл
4. **Admin Dashboard:** И-мэйл түүх харах

---

## ✅ Дууссан!

Одоо бүх захиалга **tsewegmidmonhotgon@gmail.com** руу автомат илгээгдэх болно! 🎉📧

**Асуулт байвал:**
- EmailJS Documentation: https://www.emailjs.com/docs/
- Support: support@emailjs.com
