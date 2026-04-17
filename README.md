<!DOCTYPE html>
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
  
  /* Reset margins and padding for full width */
  * { margin: 0; padding: 0; box-sizing: border-box; }
  
  body { 
    font-family: 'Noto Nastaliq Urdu', 'Amiri', serif; 
    background: var(--cream); 
    color: var(--text); 
    direction: rtl;
    width: 100%;
    overflow-x: hidden; /* Side scrolling ko rokne ke liye */
  }

  /* HERO - Isko full screen aur full width kar diya gaya hai */
  .hero {
    background: linear-gradient(135deg, var(--dark) 0%, var(--green) 60%, #2d8a55 100%);
    color: white;
    padding: 60px 0; /* Padding adjust ki gayi hai */
    width: 100vw;   /* Viewport width taake poori screen cover ho */
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  /* Baki sections ko bhi full width karne ke liye */
  section { 
    width: 100%; 
    padding: 70px 5%; /* Side padding thodi rakhi hai taake text bilkul kone se na jude */
  }

  /* Images ko responsive banaya gaya hai */
  .hero-logo {
    width: 130px;
    height: 130px;
    border-radius: 50%;
    margin: 0 auto 24px;
    box-shadow: 0 8px 40px rgba(0,0,0,0.4);
    background: white;
    border: 4px solid var(--gold);
    overflow: hidden;
  }
  
  .hero-logo img { width: 100%; height: 100%; object-fit: cover; }

  /* Navigation ko full width bar banane ke liye */
  nav {
    background: var(--dark);
    padding: 16px 0;
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 32px;
    position: sticky;
    top: 0;
    z-index: 100;
  }

  /* Content Containers (Inki max-width barha di gayi hai) */
  .about-grid, .subjects-grid, .classes-grid, #achievements-container, #gallery-container {
    max-width: 1200px; /* Isay barhane se content zyada phail jaye ga */
    margin: 0 auto;
  }

  /* Animations and other styles (Remaining the same) */
  .hero-badge { background: var(--gold); color: var(--dark); padding: 6px 24px; border-radius: 50px; margin-bottom: 24px; }
  .btn-primary { background: var(--gold); color: var(--dark); padding: 14px 32px; border-radius: 50px; text-decoration: none; font-weight: bold; }
  
  @media (max-width: 700px) {
    .about-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<section class="hero" id="home">
  <div class="hero-badge">🌟 منگورہ، سوات</div>
  <div class="hero-logo">
    <img src="YOUR_LOGO_URL_HERE" alt="Logo">
  </div>
  <h1>Home <span>Tuition</span> Center</h1>
  <p class="hero-tagline">جہاں علم روشنی بنتا ہے — تمام جماعتوں کے لیے معیاری تعلیم</p>
  <div class="hero-btns">
    <a href="#" class="btn-primary">داخلہ لیں</a>
    <a href="#" class="btn-outline">مزید معلومات</a>
  </div>
</section>

<nav>
  <a href="#home">ہوم</a>
  <a href="#about">ہمارے بارے میں</a>
  <a href="#subjects">مضامین</a>
  <a href="#contact">رابطہ</a>
</nav>

</body>
</html>
