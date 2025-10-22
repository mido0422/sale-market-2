# 🚀 Japan Market - Deployment Guide (Хостлох Заавар)

Таны Japan Market вэбсайтыг интернет дээр хостлох 3 хялбар арга.

---

## 📌 Арга 1: GitHub Pages (Үнэгүй, Хамгийн хялбар)

### Шаардлагатай зүйлс:
- GitHub бүртгэл
- Git суулгасан байх

### Алхам 1: GitHub Repository үүсгэх

1. **GitHub.com руу нэвтрэх**
   - [https://github.com](https://github.com) руу орох
   - Эсвэл шинэ бүртгэл үүсгэх

2. **Repository үүсгэх**
   - Баруун дээд буланд `+` дарж **New repository** сонгох
   - Repository name: `japan-market`
   - ✅ Public сонгох
   - **Create repository** дарах

### Алхам 2: Кодоо GitHub руу Upload хийх

**Арга A: Веб дээр Upload (Хялбар)**

```
1. GitHub repository хуудасан дээр "uploading an existing file" линк дарах
2. Дараах файлуудыг drag & drop хийх:
   - index.html
   - japan_script.js
   - japan_styles.css
   - profile.html
   - profile_script.js
   - profile_styles.css
   - Бүх зургийн folder (images/)
   - css/ folder
   
3. "Commit changes" дарах
```

**Арга B: Git Terminal ашиглах (Мэргэжлийн)**

```powershell
# 1. Таны project folder руу очих
cd "\\a01\study2025\250164\python\seller web site\japan_market"

# 2. Git эхлүүлэх
git init

# 3. Бүх файлыг нэмэх
git add .

# 4. Commit хийх
git commit -m "Initial commit - Japan Market E-commerce Site"

# 5. GitHub repository холбох (YOUR-USERNAME солих)
git remote add origin https://github.com/YOUR-USERNAME/japan-market.git

# 6. Push хийх
git branch -M main
git push -u origin main
```

### Алхам 3: GitHub Pages идэвхжүүлэх

1. Repository хуудасан дээр **Settings** tab дарах
2. Зүүн талын menu-с **Pages** сонгох
3. **Source** хэсэгт:
   - Branch: `main` сонгох
   - Folder: `/ (root)` сонгох
4. **Save** дарах

### ✅ Бэлэн! 

5-10 минутын дараа таны сайт энд ажиллана:
```
https://YOUR-USERNAME.github.io/japan-market/
```

---

## 📌 Арга 2: Netlify (Үнэгүй, Drag & Drop)

### Давуу тал:
- ⚡ Маш хурдан
- 🔄 Автомат deployment
- 🌐 Custom domain холбох боломжтой
- 📊 Analytics үнэгүй

### Алхам 1: Netlify бүртгэл үүсгэх

1. [https://www.netlify.com](https://www.netlify.com) руу орох
2. **Sign up** дарж бүртгүүлэх (GitHub-аар нэвтэрч болно)

### Алхам 2: Deploy хийх

**Арга A: Drag & Drop (Хамгийн хялбар)**

1. Netlify dashboard руу орох
2. **Add new site** > **Deploy manually** сонгох
3. Таны project folder-ийг drag & drop хийх:
   ```
   japan_market folder бүхэлд нь чирж оруулах
   ```
4. Автоматаар deploy эхэлнэ!

**Арга B: GitHub холбох (Автомат update)**

1. **Add new site** > **Import from Git** сонгох
2. **GitHub** сонгож холбох
3. **japan-market** repository сонгох
4. Build settings:
   - Build command: (хоосон үлдээх)
   - Publish directory: `.` эсвэл `/`
5. **Deploy site** дарах

### Алхам 3: Custom Domain (Заавал биш)

1. **Domain settings** руу орох
2. **Add custom domain** дарах
3. Өөрийн domain нэр оруулах (жишээ: `japan-market.mn`)

### ✅ Бэлэн!

Таны сайт одоо ажиллаж байна:
```
https://random-name-123.netlify.app
```

**Custom domain өгөх:**
- Site settings > Change site name > хүссэн нэр оруулах
- Жишээ: `japan-market-store.netlify.app`

---

## 📌 Арга 3: Vercel (Үнэгүй, Хурдан)

### Давуу тал:
- 🚀 Хамгийн хурдан хостинг
- ⚡ Автомат SSL certificate
- 🌏 Global CDN

### Алхам:

1. [https://vercel.com](https://vercel.com) руу орох
2. **Sign up** (GitHub-аар нэвтрэх)
3. **Add new project** дарах
4. **Import Git Repository** сонгож japan-market сонгох
5. **Deploy** дарах

### ✅ Бэлэн!

```
https://japan-market.vercel.app
```

---

## 📌 Арга 4: Firebase Hosting (Google)

### Шаардлагатай:
- Google бүртгэл
- Node.js суулгасан байх

### Алхам 1: Firebase CLI суулгах

```powershell
npm install -g firebase-tools
```

### Алхам 2: Firebase эхлүүлэх

```powershell
# Login хийх
firebase login

# Project folder руу очих
cd "\\a01\study2025\250164\python\seller web site\japan_market"

# Firebase эхлүүлэх
firebase init hosting

# Асуултуудад хариулах:
# - Create a new project
# - Public directory: . (одоогийн folder)
# - Single-page app: No
# - Automatic builds: No
```

### Алхам 3: Deploy хийх

```powershell
firebase deploy
```

### ✅ Бэлэн!

```
https://your-project-id.web.app
```

---

## 🎯 Санал болгож байгаа арга:

### Хөгжүүлэлтийн үед:
✅ **Арга 1: GitHub Pages**
- Үнэгүй
- Хялбар
- Git сурах боломж

### Бизнест ашиглах бол:
✅ **Арга 2: Netlify**
- Маш хурдан
- Custom domain
- Автомат deployment
- Analytics

---

## 🔧 Deployment өмнө шалгах зүйлс:

### 1. Файлын замууд шалгах

Бүх файл **харьцангуй зам** ашиглаж байгаа эсэхийг шалгана:

**✅ Зөв:**
```html
<link rel="stylesheet" href="japan_styles.css">
<script src="japan_script.js"></script>
<img src="images/product1.jpg">
```

**❌ Буруу:**
```html
<link rel="stylesheet" href="C:/Users/.../japan_styles.css">
```

### 2. Case-sensitive файлын нэрс

Linux серверүүд дээр файлын нэр case-sensitive байна:
- `Profile.html` ≠ `profile.html`
- `Images/` ≠ `images/`

### 3. localStorage асуудал

Deployment хийсний дараа localStorage хоосон байх болно. Demo data автоматаар үүсгэх код танд байна, тэгэхээр асуудалгүй.

---

## 📱 Mobile тест хийх:

Deploy хийсний дараа:

1. **Google Mobile-Friendly Test:**
   ```
   https://search.google.com/test/mobile-friendly
   ```

2. **Browser Developer Tools:**
   - F12 дарах
   - Toggle device toolbar (Ctrl+Shift+M)
   - Өөр төхөөрөмжүүд дээр үзэх

---

## 🔐 .gitignore файл үүсгэх (GitHub-д оруулахгүй байх зүйлс)

```bash
# Node modules
node_modules/

# OS файлууд
.DS_Store
Thumbs.db

# IDE
.vscode/
.idea/

# Logs
*.log

# Env files
.env
.env.local

# Build files
dist/
build/
```

---

## 🆘 Түгээмэл асуудал & Шийдэл:

### Асуудал 1: "404 Not Found"
**Шийдэл:** 
- Файлын нэр зөв эсэхийг шалгах
- index.html repository-ийн үндсэн folder-т байгаа эсэхийг шалгах

### Асуудал 2: CSS ажиллахгүй байна
**Шийдэл:**
- Browser cache цэвэрлэх (Ctrl+F5)
- CSS файлын зам зөв эсэхийг шалгах
- Browser Console-д алдаа шалгах (F12)

### Асуудал 3: Зураг харагдахгүй
**Шийдэл:**
- Зургийн файлууд upload хийгдсэн эсэхийг шалгах
- Зургийн замын case (том/жижиг үсэг) зөв эсэхийг шалгах
- Зургийн хэмжээ хэт их биш эсэхийг шалгах

### Асуудал 4: JavaScript ажиллахгүй
**Шийдэл:**
- Browser Console алдаа шалгах (F12)
- Script файл зөв холбогдсон эсэхийг шалгах
- HTTPS дээр ажиллуулж байгаа эсэхийг шалгах

---

## 📊 Performance сайжруулах:

Deploy хийсний дараа:

1. **Зургуудыг optimize хийх:**
   - [TinyPNG](https://tinypng.com) - Зураг багасгах
   - WebP формат ашиглах

2. **Minify CSS/JS:**
   - [CSS Minifier](https://cssminifier.com)
   - [JavaScript Minifier](https://javascript-minifier.com)

3. **CDN ашиглах:**
   - Netlify/Vercel автоматаар CDN өгнө

---

## 🎉 Амжилттай Deploy хийх дараалал:

### Зөвлөмж дараалал (Эхлэгчдэд):

1. ✅ **GitHub Pages** - Анхны deploy (Үнэгүй, хялбар)
2. ✅ **Domain худалдаж авах** - [Namecheap](https://namecheap.com) эсвэл [Hostinger](https://hostinger.com)
3. ✅ **Netlify руу шилжих** - Custom domain холбох
4. ✅ **Analytics нэмэх** - Google Analytics эсвэл Netlify Analytics

---

## 💡 Дараагийн алхмууд:

### Backend нэмэх (Ирээдүйд):
- Node.js + Express
- MongoDB/PostgreSQL
- User authentication (JWT)
- Payment gateway integration
- Email notifications

### Recommended Stack:
```
Frontend: HTML, CSS, JavaScript (одоо байгаа)
Backend: Node.js + Express
Database: MongoDB
Hosting: Netlify (Frontend) + Heroku/Railway (Backend)
```

---

## 📞 Туслах холбоосууд:

- **GitHub Pages Docs:** https://pages.github.com
- **Netlify Docs:** https://docs.netlify.com
- **Vercel Docs:** https://vercel.com/docs
- **Firebase Docs:** https://firebase.google.com/docs/hosting

---

## ✅ Checklist өмнө Deploy хийх:

- [ ] Бүх файлууд бэлэн байна
- [ ] Харьцангуй замууд ашигласан
- [ ] Зургууд optimize хийсэн
- [ ] Mobile responsive шалгасан
- [ ] Browser compatibility тест хийсэн
- [ ] Console error байхгүй
- [ ] localStorage demo data ажиллаж байна
- [ ] Бүх линкүүд ажиллаж байна

---

**Амжилт хүсье! 🚀**

Хэрэв асуудал гарвал, deploy хийсний дараа хэлээрэй, би туслах болно!
