[<!DOCTYPE html>
<html lang="ur" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Home Tuition Center - Mingora, Swat</title>
<link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Noto+Nastaliq+Urdu:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #1a6b3c;
    --gold: #c8a84b;
    --cream: #fdf6e3;
    --dark: #0d2b1a;
    --light-green: #e8f5ee;
    --text: #1a1a1a;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Noto Nastaliq Urdu', 'Amiri', serif;
    background: var(--cream);
    color: var(--text);
    direction: rtl;
  }

  /* HERO */
  .hero {
    background: linear-gradient(135deg, var(--dark) 0%, var(--green) 60%, #2d8a55 100%);
    color: white;
    padding: 0;
    position: relative;
    overflow: hidden;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: url("data:image/svg+xml,%3Csvg width='80' height='80' viewBox='0 0 80 80' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.04'%3E%3Cpath d='M40 40m-35 0a35 35 0 1 1 70 0a35 35 0 1 1-70 0'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    opacity: 0.4;
  }

  .hero-badge {
    background: var(--gold);
    color: var(--dark);
    padding: 6px 24px;
    border-radius: 50px;
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 1px;
    margin-bottom: 20px;
    animation: fadeDown 0.8s ease;
  }

  .hero-logo {
    width: 110px;
    height: 110px;
    background: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 24px;
    box-shadow: 0 8px 40px rgba(0,0,0,0.3);
    animation: popIn 0.8s ease 0.2s both;
    font-size: 3rem;
  }

  .hero h1 {
    font-family: 'Amiri', serif;
    font-size: clamp(2rem, 6vw, 3.5rem);
    font-weight: 700;
    text-align: center;
    line-height: 1.3;
    animation: fadeUp 0.8s ease 0.3s both;
    text-shadow: 0 2px 20px rgba(0,0,0,0.3);
  }

  .hero h1 span { color: var(--gold); }

  .hero-tagline {
    text-align: center;
    font-size: 1.1rem;
    opacity: 0.9;
    margin: 16px 0 32px;
    animation: fadeUp 0.8s ease 0.5s both;
    max-width: 500px;
  }

  .hero-btns {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
    justify-content: center;
    animation: fadeUp 0.8s ease 0.7s both;
  }

  .btn-primary {
    background: var(--gold);
    color: var(--dark);
    padding: 14px 32px;
    border-radius: 50px;
    font-weight: 700;
    font-size: 1rem;
    text-decoration: none;
    border: none;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
    font-family: inherit;
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 25px rgba(200,168,75,0.5); }

  .btn-outline {
    background: transparent;
    color: white;
    padding: 14px 32px;
    border-radius: 50px;
    font-weight: 600;
    font-size: 1rem;
    text-decoration: none;
    border: 2px solid rgba(255,255,255,0.5);
    cursor: pointer;
    transition: all 0.2s;
    font-family: inherit;
  }
  .btn-outline:hover { border-color: white; background: rgba(255,255,255,0.1); }

  .hero-stats {
    display: flex;
    gap: 40px;
    margin-top: 50px;
    animation: fadeUp 0.8s ease 0.9s both;
    flex-wrap: wrap;
    justify-content: center;
  }

  .stat {
    text-align: center;
  }
  .stat-number {
    font-size: 2rem;
    font-weight: 700;
    color: var(--gold);
    font-family: 'Amiri', serif;
  }
  .stat-label { font-size: 0.85rem; opacity: 0.8; }

  .scroll-down {
    position: absolute;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    animation: bounce 2s infinite;
    color: rgba(255,255,255,0.6);
    font-size: 1.5rem;
  }

  /* NAV */
  nav {
    background: var(--dark);
    padding: 16px 24px;
    display: flex;
    justify-content: center;
    gap: 32px;
    flex-wrap: wrap;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 20px rgba(0,0,0,0.3);
  }
  nav a {
    color: rgba(255,255,255,0.8);
    text-decoration: none;
    font-size: 0.95rem;
    transition: color 0.2s;
    padding: 4px 0;
    border-bottom: 2px solid transparent;
  }
  nav a:hover { color: var(--gold); border-bottom-color: var(--gold); }

  /* SECTIONS */
  section { padding: 70px 20px; }
  .section-title {
    text-align: center;
    font-family: 'Amiri', serif;
    font-size: clamp(1.8rem, 4vw, 2.5rem);
    color: var(--green);
    margin-bottom: 12px;
  }
  .section-title span { color: var(--gold); }
  .section-subtitle {
    text-align: center;
    color: #555;
    font-size: 1rem;
    margin-bottom: 50px;
  }
  .divider {
    width: 60px;
    height: 4px;
    background: linear-gradient(to right, var(--green), var(--gold));
    margin: 16px auto 40px;
    border-radius: 2px;
  }

  /* ABOUT */
  .about-section { background: white; }
  .about-grid {
    max-width: 900px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
  }
  .about-text p {
    line-height: 2;
    font-size: 1.05rem;
    color: #444;
    margin-bottom: 16px;
  }
  .about-image {
    background: linear-gradient(135deg, var(--light-green), #c8e6d5);
    border-radius: 20px;
    padding: 40px;
    text-align: center;
    font-size: 5rem;
    box-shadow: 0 10px 40px rgba(26,107,60,0.15);
  }

  /* SUBJECTS */
  .subjects-section { background: var(--light-green); }
  .subjects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    max-width: 900px;
    margin: 0 auto;
  }
  .subject-card {
    background: white;
    border-radius: 16px;
    padding: 28px 20px;
    text-align: center;
    box-shadow: 0 4px 20px rgba(0,0,0,0.06);
    transition: transform 0.2s, box-shadow 0.2s;
    border-top: 4px solid var(--green);
  }
  .subject-card:hover { transform: translateY(-5px); box-shadow: 0 12px 35px rgba(26,107,60,0.15); }
  .subject-icon { font-size: 2.5rem; margin-bottom: 12px; }
  .subject-card h3 { font-size: 1.1rem; color: var(--green); margin-bottom: 6px; }
  .subject-card p { font-size: 0.85rem; color: #777; }

  /* CLASSES */
  .classes-section { background: white; }
  .classes-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
    max-width: 800px;
    margin: 0 auto;
  }
  .class-card {
    background: linear-gradient(135deg, var(--green), #2d8a55);
    color: white;
    border-radius: 16px;
    padding: 32px 20px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 6px 25px rgba(26,107,60,0.3);
    transition: transform 0.2s;
  }
  .class-card:hover { transform: scale(1.03); }
  .class-card::before {
    content: '';
    position: absolute;
    top: -20px; right: -20px;
    width: 80px; height: 80px;
    background: rgba(255,255,255,0.1);
    border-radius: 50%;
  }
  .class-level { font-size: 2rem; margin-bottom: 8px; }
  .class-card h3 { font-size: 1.2rem; font-weight: 700; margin-bottom: 6px; }
  .class-card p { font-size: 0.85rem; opacity: 0.85; }

  /* ACHIEVEMENTS */
  .achievements-section { background: var(--cream); }
  #achievements-container {
    max-width: 900px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px;
  }
  .achievement-card {
    background: white;
    border-radius: 16px;
    overflow: hidden;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    transition: transform 0.2s;
  }
  .achievement-card:hover { transform: translateY(-4px); }
  .achievement-img {
    width: 100%;
    height: 180px;
    object-fit: cover;
    background: linear-gradient(135deg, var(--light-green), #c8e6d5);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 4rem;
    color: var(--green);
  }
  .achievement-body { padding: 20px; }
  .achievement-body h3 { font-size: 1.05rem; color: var(--green); margin-bottom: 6px; }
  .achievement-body p { font-size: 0.85rem; color: #666; line-height: 1.7; }
  .achievement-date { font-size: 0.75rem; color: var(--gold); margin-top: 8px; font-weight: 600; }

  /* GALLERY */
  .gallery-section { background: white; }
  #gallery-container {
    max-width: 900px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 16px;
  }
  .gallery-item {
    border-radius: 12px;
    overflow: hidden;
    aspect-ratio: 4/3;
    background: var(--light-green);
    position: relative;
    cursor: pointer;
  }
  .gallery-item img {
    width: 100%; height: 100%;
    object-fit: cover;
    transition: transform 0.3s;
  }
  .gallery-item:hover img { transform: scale(1.05); }
  .gallery-placeholder {
    width: 100%; height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: var(--green);
    font-size: 0.9rem;
    gap: 8px;
  }

  /* UPLOAD PANEL */
  .admin-section {
    background: var(--dark);
    color: white;
    padding: 60px 20px;
  }
  .admin-section .section-title { color: var(--gold); }
  .admin-section .section-subtitle { color: rgba(255,255,255,0.7); }

  .admin-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
    max-width: 800px;
    margin: 0 auto;
  }

  .upload-box {
    background: rgba(255,255,255,0.05);
    border: 2px dashed rgba(200,168,75,0.4);
    border-radius: 16px;
    padding: 30px 24px;
  }
  .upload-box h3 { color: var(--gold); margin-bottom: 20px; font-size: 1.1rem; }

  .form-group { margin-bottom: 16px; }
  .form-group label { display: block; font-size: 0.85rem; color: rgba(255,255,255,0.7); margin-bottom: 6px; }
  .form-group input, .form-group textarea {
    width: 100%;
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.15);
    border-radius: 8px;
    padding: 10px 14px;
    color: white;
    font-family: inherit;
    font-size: 0.9rem;
    direction: rtl;
  }
  .form-group textarea { min-height: 80px; resize: vertical; }
  .form-group input[type="file"] { padding: 8px; cursor: pointer; }

  .btn-upload {
    width: 100%;
    background: var(--gold);
    color: var(--dark);
    border: none;
    padding: 12px;
    border-radius: 10px;
    font-size: 1rem;
    font-weight: 700;
    font-family: inherit;
    cursor: pointer;
    transition: opacity 0.2s;
    margin-top: 8px;
  }
  .btn-upload:hover { opacity: 0.9; }

  .msg-success {
    background: rgba(26,107,60,0.3);
    border: 1px solid var(--green);
    color: #7fdb9e;
    padding: 10px 16px;
    border-radius: 8px;
    font-size: 0.9rem;
    margin-top: 12px;
    display: none;
  }

  /* CONTACT */
  .contact-section { background: var(--light-green); }
  .contact-cards {
    display: flex;
    gap: 24px;
    justify-content: center;
    flex-wrap: wrap;
    max-width: 800px;
    margin: 0 auto;
  }
  .contact-card {
    background: white;
    border-radius: 16px;
    padding: 28px 32px;
    text-align: center;
    box-shadow: 0 4px 20px rgba(0,0,0,0.07);
    flex: 1;
    min-width: 200px;
    max-width: 240px;
    transition: transform 0.2s;
  }
  .contact-card:hover { transform: translateY(-4px); }
  .contact-icon { font-size: 2.2rem; margin-bottom: 12px; }
  .contact-card h3 { color: var(--green); font-size: 0.95rem; margin-bottom: 8px; }
  .contact-card p { color: #555; font-size: 0.9rem; line-height: 1.7; }
  .contact-card a { color: var(--green); text-decoration: none; font-weight: 600; }

  /* FOOTER */
  footer {
    background: var(--dark);
    color: rgba(255,255,255,0.7);
    text-align: center;
    padding: 30px 20px;
    font-size: 0.9rem;
    line-height: 2;
  }
  footer span { color: var(--gold); }

  /* LIGHTBOX */
  .lightbox {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.92);
    z-index: 1000;
    align-items: center;
    justify-content: center;
  }
  .lightbox.active { display: flex; }
  .lightbox img { max-width: 90vw; max-height: 85vh; border-radius: 12px; object-fit: contain; }
  .lightbox-close {
    position: absolute;
    top: 20px;
    left: 20px;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    background: none;
    border: none;
    line-height: 1;
  }

  /* ANIMATIONS */
  @keyframes fadeDown { from { opacity:0; transform:translateY(-20px); } to { opacity:1; transform:translateY(0); } }
  @keyframes fadeUp   { from { opacity:0; transform:translateY(20px);  } to { opacity:1; transform:translateY(0); } }
  @keyframes popIn    { from { opacity:0; transform:scale(0.5); } to { opacity:1; transform:scale(1); } }
  @keyframes bounce   { 0%,100% { transform:translateX(-50%) translateY(0); } 50% { transform:translateX(-50%) translateY(-10px); } }

  @media (max-width: 700px) {
    .about-grid { grid-template-columns: 1fr; }
    .admin-grid  { grid-template-columns: 1fr; }
    .hero-stats  { gap: 24px; }
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-badge">🌟 منگورہ، سوات</div>
  <div class="hero-logo">📚</div>
  <h1>Home <span>Tuition</span> Center</h1>
  <p class="hero-tagline">جہاں علم روشنی بنتا ہے — تمام جماعتوں کے لیے معیاری تعلیم</p>
  <div class="hero-btns">
    <a href="#contact" class="btn-primary">ابھی رابطہ کریں</a>
    <a href="#subjects" class="btn-outline">مضامین دیکھیں</a>
  </div>
  <div class="hero-stats">
    <div class="stat">
      <div class="stat-number">١٢</div>
      <div class="stat-label">جماعتیں (1 تا FSc)</div>
    </div>
    <div class="stat">
      <div class="stat-number">١٠٠٪</div>
      <div class="stat-label">محنت و لگن</div>
    </div>
    <div class="stat">
      <div class="stat-number">🏆</div>
      <div class="stat-label">ثابت شدہ نتائج</div>
    </div>
  </div>
  <div class="scroll-down">↓</div>
</section>

<!-- NAV -->
<nav>
  <a href="#home">گھر</a>
  <a href="#about">ہمارے بارے میں</a>
  <a href="#subjects">مضامین</a>
  <a href="#classes">جماعتیں</a>
  <a href="#achievements">کامیابیاں</a>
  <a href="#gallery">تصویریں</a>
  <a href="#contact">رابطہ</a>
</nav>

<!-- ABOUT -->
<section class="about-section" id="about">
  <h2 class="section-title">ہمارے <span>بارے میں</span></h2>
  <div class="divider"></div>
  <div class="about-grid">
    <div class="about-text">
      <p>Home Tuition Center منگورہ، سوات میں ایک معیاری تعلیمی مرکز ہے جہاں پرائمری سے FSc تک تمام جماعتوں کے طلبہ کو ان کے گھر جیسے ماحول میں بہترین تعلیم فراہم کی جاتی ہے۔</p>
      <p>ہمارا مقصد ہر بچے کی انفرادی صلاحیتوں کو نکھارنا اور انہیں امتحانات میں بہترین نتائج دلوانا ہے۔ تجربہ کار اساتذہ، محبت بھرا ماحول، اور نتیجہ خیز تدریس — یہی ہماری پہچان ہے۔</p>
    </div>
    <div class="about-image">🎓</div>
  </div>
</section>

<!-- SUBJECTS -->
<section class="subjects-section" id="subjects">
  <h2 class="section-title">ہمارے <span>مضامین</span></h2>
  <p class="section-subtitle">تمام اہم مضامین ایک ہی چھت تلے</p>
  <div class="divider"></div>
  <div class="subjects-grid">
    <div class="subject-card">
      <div class="subject-icon">🔬</div>
      <h3>فزکس</h3>
      <p>نظریہ و عملی</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">➕</div>
      <h3>ریاضی</h3>
      <p>بنیاد سے کیلکولس تک</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">🧪</div>
      <h3>کیمسٹری</h3>
      <p>نظریہ و لیب</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">🌿</div>
      <h3>بیالوجی</h3>
      <p>حیاتیاتی علوم</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">🇬🇧</div>
      <h3>انگریزی</h3>
      <p>گرامر و تحریر</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">📖</div>
      <h3>اردو</h3>
      <p>ادب و گرامر</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">🌍</div>
      <h3>سوشل اسٹڈیز</h3>
      <p>سماجی علوم</p>
    </div>
    <div class="subject-card">
      <div class="subject-icon">💻</div>
      <h3>کمپیوٹر</h3>
      <p>بنیادی تعلیم</p>
    </div>
  </div>
</section>

<!-- CLASSES -->
<section class="classes-section" id="classes">
  <h2 class="section-title">ہماری <span>جماعتیں</span></h2>
  <p class="section-subtitle">پرائمری سے FSc تک — سب کے لیے</p>
  <div class="divider"></div>
  <div class="classes-grid">
    <div class="class-card">
      <div class="class-level">🌱</div>
      <h3>پرائمری</h3>
      <p>جماعت ۱ تا ۵</p>
    </div>
    <div class="class-card">
      <div class="class-level">📗</div>
      <h3>مڈل</h3>
      <p>جماعت ۶ تا ۸</p>
    </div>
    <div class="class-card">
      <div class="class-level">🎯</div>
      <h3>میٹرک</h3>
      <p>جماعت ۹ تا ۱۰</p>
    </div>
    <div class="class-card">
      <div class="class-level">🚀</div>
      <h3>FSc</h3>
      <p>جماعت ۱۱ تا ۱۲</p>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section class="achievements-section" id="achievements">
  <h2 class="section-title">بچوں کی <span>کامیابیاں</span></h2>
  <p class="section-subtitle">ہمارے ہونہار طلبہ کی شاندار کارکردگی</p>
  <div class="divider"></div>
  <div id="achievements-container">
    <!-- Default achievement cards -->
    <div class="achievement-card">
      <div class="achievement-img">🏆</div>
      <div class="achievement-body">
        <h3>پوزیشن ہولڈر طالب علم</h3>
        <p>بورڈ امتحان میں شاندار نتیجہ — اے پلس گریڈ حاصل کیا</p>
        <div class="achievement-date">2024</div>
      </div>
    </div>
    <div class="achievement-card">
      <div class="achievement-img">⭐</div>
      <div class="achievement-body">
        <h3>ریاضی اولمپیاڈ</h3>
        <p>ضلعی سطح پر پہلی پوزیشن — طالب علم احمد خان</p>
        <div class="achievement-date">2024</div>
      </div>
    </div>
    <div class="achievement-card">
      <div class="achievement-img">🎖️</div>
      <div class="achievement-body">
        <h3>سائنس فیئر انعام</h3>
        <p>اسکول سطح پر سائنس پروجیکٹ میں اول انعام</p>
        <div class="achievement-date">2023</div>
      </div>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section class="gallery-section" id="gallery">
  <h2 class="section-title">ہماری <span>تصویریں</span></h2>
  <p class="section-subtitle">مرکز کی سرگرمیاں اور یادیں</p>
  <div class="divider"></div>
  <div id="gallery-container">
    <div class="gallery-item">
      <div class="gallery-placeholder">📷<span>تصویر جلد آئے گی</span></div>
    </div>
    <div class="gallery-item">
      <div class="gallery-placeholder">📷<span>تصویر جلد آئے گی</span></div>
    </div>
    <div class="gallery-item">
      <div class="gallery-placeholder">📷<span>تصویر جلد آئے گی</span></div>
    </div>
  </div>
</section>

<!-- ADMIN UPLOAD PANEL -->
<section class="admin-section" id="admin">
  <h2 class="section-title">مواد اپلوڈ کریں</h2>
  <p class="section-subtitle">تصویریں اور کامیابیاں شامل کریں</p>
  <div class="admin-grid">

    <!-- Upload Achievement -->
    <div class="upload-box">
      <h3>🏆 کامیابی شامل کریں</h3>
      <div class="form-group">
        <label>طالب علم کا نام</label>
        <input type="text" id="ach-name" placeholder="مثلاً: احمد خان">
      </div>
      <div class="form-group">
        <label>تفصیل</label>
        <textarea id="ach-desc" placeholder="مثلاً: بورڈ میں اے پلس حاصل کیا"></textarea>
      </div>
      <div class="form-group">
        <label>سال</label>
        <input type="text" id="ach-year" placeholder="مثلاً: 2025">
      </div>
      <div class="form-group">
        <label>تصویر (اختیاری)</label>
        <input type="file" id="ach-img" accept="image/*">
      </div>
      <button class="btn-upload" onclick="addAchievement()">کامیابی شامل کریں ✓</button>
      <div class="msg-success" id="ach-msg">✓ کامیابی شامل ہو گئی!</div>
    </div>

    <!-- Upload Gallery Photo -->
    <div class="upload-box">
      <h3>📷 تصویر اپلوڈ کریں</h3>
      <div class="form-group">
        <label>تصویر منتخب کریں</label>
        <input type="file" id="gal-img" accept="image/*" multiple>
      </div>
      <div class="form-group">
        <label>عنوان (اختیاری)</label>
        <input type="text" id="gal-title" placeholder="مثلاً: سالانہ تقریب 2025">
      </div>
      <button class="btn-upload" onclick="addGalleryPhoto()">گیلری میں شامل کریں ✓</button>
      <div class="msg-success" id="gal-msg">✓ تصویر شامل ہو گئی!</div>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <h2 class="section-title">ہم سے <span>رابطہ کریں</span></h2>
  <p class="section-subtitle">داخلے کے لیے آج ہی رابطہ کریں</p>
  <div class="divider"></div>
  <div class="contact-cards">
    <div class="contact-card">
      <div class="contact-icon">📍</div>
      <h3>پتہ</h3>
      <p>منگورہ، سوات، خیبر پختونخوا، پاکستان</p>
    </div>
    <div class="contact-card">
      <div class="contact-icon">📞</div>
      <h3>فون</h3>
      <p><a href="tel:+923499236145">0349-9236145</a></p>
    </div>
    <div class="contact-card">
      <div class="contact-icon">🕐</div>
      <h3>اوقات</h3>
      <p>صبح ۸ بجے تا شام ۸ بجے<br>پیر تا ہفتہ</p>
    </div>
    <div class="contact-card">
      <div class="contact-icon">📧</div>
      <h3>ای میل</h3>
      <p><a href="mailto:ar2108912@gmail.com">ar2108912@gmail.com</a></p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2025 <span>Home Tuition Center</span> — منگورہ، سوات</p>
  <p>علم روشنی ہے — ہر بچے کا حق</p>
</footer>

<!-- LIGHTBOX -->
<div class="lightbox" id="lightbox">
  <button class="lightbox-close" onclick="closeLightbox()">✕</button>
  <img id="lightbox-img" src="" alt="">
</div>

<script>
// ACHIEVEMENT UPLOAD
function addAchievement() {
  const name = document.getElementById('ach-name').value.trim();
  const desc = document.getElementById('ach-desc').value.trim();
  const year = document.getElementById('ach-year').value.trim();
  const imgFile = document.getElementById('ach-img').files[0];

  if (!name || !desc) { alert('براہ کرم نام اور تفصیل لکھیں۔'); return; }

  const card = document.createElement('div');
  card.className = 'achievement-card';

  if (imgFile) {
    const reader = new FileReader();
    reader.onload = e => {
      card.innerHTML = `
        <img src="${e.target.result}" class="achievement-img" style="width:100%;height:180px;object-fit:cover;">
        <div class="achievement-body">
          <h3>${name}</h3>
          <p>${desc}</p>
          <div class="achievement-date">${year || '2025'}</div>
        </div>`;
      document.getElementById('achievements-container').prepend(card);
    };
    reader.readAsDataURL(imgFile);
  } else {
    card.innerHTML = `
      <div class="achievement-img">🏆</div>
      <div class="achievement-body">
        <h3>${name}</h3>
        <p>${desc}</p>
        <div class="achievement-date">${year || '2025'}</div>
      </div>`;
    document.getElementById('achievements-container').prepend(card);
  }

  // Reset form
  ['ach-name','ach-desc','ach-year'].forEach(id => document.getElementById(id).value = '');
  document.getElementById('ach-img').value = '';
  const msg = document.getElementById('ach-msg');
  msg.style.display = 'block';
  setTimeout(() => msg.style.display = 'none', 3000);
}

// GALLERY UPLOAD
function addGalleryPhoto() {
  const files = document.getElementById('gal-img').files;
  const title = document.getElementById('gal-title').value.trim();
  if (!files.length) { alert('براہ کرم تصویر منتخب کریں۔'); return; }

  const container = document.getElementById('gallery-container');
  // Remove placeholders on first real upload
  container.querySelectorAll('.gallery-placeholder').forEach(p => p.parentElement.remove());

  Array.from(files).forEach(file => {
    const reader = new FileReader();
    reader.onload = e => {
      const item = document.createElement('div');
      item.className = 'gallery-item';
      const img = document.createElement('img');
      img.src = e.target.result;
      img.alt = title || 'تصویر';
      img.onclick = () => openLightbox(e.target.result);
      item.appendChild(img);
      container.prepend(item);
    };
    reader.readAsDataURL(file);
  });

  document.getElementById('gal-img').value = '';
  document.getElementById('gal-title').value = '';
  const msg = document.getElementById('gal-msg');
  msg.style.display = 'block';
  setTimeout(() => msg.style.display = 'none', 3000);
}

// LIGHTBOX
function openLightbox(src) {
  document.getElementById('lightbox-img').src = src;
  document.getElementById('lightbox').classList.add('active');
}
function closeLightbox() {
  document.getElementById('lightbox').classList.remove('active');
}
document.getElementById('lightbox').addEventListener('click', function(e) {
  if (e.target === this) closeLightbox();
});

// SMOOTH SCROLL
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', e => {
    e.preventDefault();
    document.querySelector(a.getAttribute('href'))?.scrollIntoView({ behavior: 'smooth' });
  });
});
</script>
</body>
</html>
](https://drive.google.com/file/d/1n-jt26AKbP_zy_WB27PKUBN3xPBT6imu/view?usp=sharing)
