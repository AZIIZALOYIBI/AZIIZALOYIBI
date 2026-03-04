## Hi there 👋

<!--
**AZIIZALOYIBI/AZIIZALOYIBI** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- <!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AZIIZ ALOYIBI — Full-Stack Developer</title>
  <meta name="description" content="Aziiz Aloyibi — Full-Stack Developer, Open Source Enthusiast. Building scalable web applications." />
  <style>
    /* ── Reset & Base ──────────────────────────────── */
    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; font-size: 16px; }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #0d1117;
      color: #c9d1d9;
      line-height: 1.7;
      overflow-x: hidden;
    }
    a { color: #58a6ff; text-decoration: none; transition: color .3s; }
    a:hover { color: #79c0ff; }
    img { max-width: 100%; height: auto; }

    /* ── Utility ───────────────────────────────────── */
    .container { max-width: 1100px; margin: 0 auto; padding: 0 1.5rem; }
    .section { padding: 5rem 0; }
    .section-title {
      font-size: 2rem;
      font-weight: 700;
      color: #58a6ff;
      margin-bottom: 2.5rem;
      text-align: center;
      position: relative;
    }
    .section-title::after {
      content: '';
      display: block;
      width: 60px;
      height: 3px;
      background: #58a6ff;
      margin: .6rem auto 0;
      border-radius: 2px;
    }

    /* ── Animations ─────────────────────────────────── */
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50%      { transform: translateY(-10px); }
    }
    @keyframes glow {
      0%, 100% { box-shadow: 0 0 5px rgba(88,166,255,.4); }
      50%      { box-shadow: 0 0 20px rgba(88,166,255,.8); }
    }
    .fade-in {
      opacity: 0;
      animation: fadeInUp .8s ease forwards;
    }
    .fade-in.d1 { animation-delay: .1s; }
    .fade-in.d2 { animation-delay: .2s; }
    .fade-in.d3 { animation-delay: .3s; }
    .fade-in.d4 { animation-delay: .4s; }

    /* ── Navbar ─────────────────────────────────────── */
    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(13,17,23,.92);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid #21262d;
      z-index: 1000;
      transition: background .3s;
    }
    .navbar .container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 64px;
    }
    .nav-logo {
      font-size: 1.4rem;
      font-weight: 700;
      color: #58a6ff;
      letter-spacing: 1px;
    }
    .nav-links { display: flex; gap: 1.8rem; list-style: none; }
    .nav-links a {
      color: #8b949e;
      font-weight: 500;
      font-size: .95rem;
      transition: color .3s;
    }
    .nav-links a:hover { color: #58a6ff; }
    .nav-toggle {
      display: none;
      flex-direction: column;
      gap: 5px;
      cursor: pointer;
      background: none;
      border: none;
      padding: 4px;
    }
    .nav-toggle span {
      width: 24px;
      height: 2px;
      background: #c9d1d9;
      border-radius: 2px;
      transition: .3s;
    }

    /* ── Hero ───────────────────────────────────────── */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      background: radial-gradient(ellipse at 50% 0%, #16213e 0%, #0d1117 70%);
      position: relative;
    }
    .hero-content { position: relative; z-index: 1; }
    .hero-avatar {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 3px solid #58a6ff;
      animation: glow 3s ease-in-out infinite, float 4s ease-in-out infinite;
      margin-bottom: 1.5rem;
    }
    .hero h1 {
      font-size: 3rem;
      color: #e6edf3;
      margin-bottom: .5rem;
    }
    .hero .subtitle {
      font-size: 1.25rem;
      color: #8b949e;
      margin-bottom: 2rem;
    }
    .hero .cta-group { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
    .btn {
      display: inline-flex;
      align-items: center;
      gap: .5rem;
      padding: .75rem 1.8rem;
      border-radius: 8px;
      font-size: 1rem;
      font-weight: 600;
      transition: transform .3s, box-shadow .3s, background .3s;
      cursor: pointer;
      border: none;
    }
    .btn-primary {
      background: #58a6ff;
      color: #0d1117;
    }
    .btn-primary:hover {
      background: #79c0ff;
      color: #0d1117;
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(88,166,255,.35);
    }
    .btn-outline {
      background: transparent;
      color: #58a6ff;
      border: 2px solid #58a6ff;
    }
    .btn-outline:hover {
      background: rgba(88,166,255,.1);
      transform: translateY(-2px);
      color: #58a6ff;
    }

    /* ── Particles (decorative) ─────────────────────── */
    .particles {
      position: absolute;
      inset: 0;
      overflow: hidden;
      pointer-events: none;
    }
    .particles span {
      position: absolute;
      width: 4px;
      height: 4px;
      background: #58a6ff;
      border-radius: 50%;
      opacity: .25;
      animation: float 6s ease-in-out infinite;
    }
    .particles span:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
    .particles span:nth-child(2) { top: 60%; left: 80%; animation-delay: 1s; }
    .particles span:nth-child(3) { top: 40%; left: 50%; animation-delay: 2s; }
    .particles span:nth-child(4) { top: 80%; left: 25%; animation-delay: 3s; }
    .particles span:nth-child(5) { top: 15%; left: 70%; animation-delay: 4s; }

    /* ── About ──────────────────────────────────────── */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: center;
    }
    .about-text p { margin-bottom: 1rem; color: #8b949e; font-size: 1.05rem; }
    .about-highlights {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
      margin-top: 1.5rem;
    }
    .highlight-card {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 12px;
      padding: 1.2rem;
      text-align: center;
      transition: transform .3s, border-color .3s;
    }
    .highlight-card:hover {
      transform: translateY(-4px);
      border-color: #58a6ff;
    }
    .highlight-card .icon { font-size: 1.6rem; margin-bottom: .4rem; }
    .highlight-card h4 { color: #e6edf3; font-size: .95rem; }

    /* ── Skills ─────────────────────────────────────── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
    }
    .skill-category {
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 14px;
      padding: 2rem;
      transition: transform .3s, border-color .3s;
    }
    .skill-category:hover {
      transform: translateY(-4px);
      border-color: #58a6ff;
    }
    .skill-category h3 {
      color: #e6edf3;
      margin-bottom: 1rem;
      font-size: 1.15rem;
    }
    .skill-tags { display: flex; flex-wrap: wrap; gap: .5rem; }
    .skill-tag {
      background: rgba(88,166,255,.1);
      color: #58a6ff;
      padding: .35rem .85rem;
      border-radius: 20px;
      font-size: .85rem;
      font-weight: 500;
      border: 1px solid rgba(88,166,255,.2);
      transition: background .3s, transform .3s;
    }
    .skill-tag:hover {
      background: rgba(88,166,255,.2);
      transform: scale(1.05);
    }

    /* ── Stats ──────────────────────────────────────── */
    .stats-cards {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      justify-content: center;
    }
    .stats-cards img {
      border-radius: 10px;
      transition: transform .3s;
    }
    .stats-cards img:hover { transform: scale(1.03); }

    /* ── Contact ────────────────────────────────────── */
    .contact-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
    }
    .contact-card {
      display: flex;
      align-items: center;
      gap: .75rem;
      background: #161b22;
      border: 1px solid #21262d;
      border-radius: 12px;
      padding: 1rem 1.5rem;
      font-weight: 600;
      transition: transform .3s, border-color .3s;
      color: #c9d1d9;
    }
    .contact-card:hover {
      transform: translateY(-4px);
      border-color: #58a6ff;
      color: #58a6ff;
    }
    .contact-card .c-icon { font-size: 1.4rem; }

    /* ── Footer ─────────────────────────────────────── */
    .footer {
      text-align: center;
      padding: 2.5rem 0;
      border-top: 1px solid #21262d;
      color: #484f58;
      font-size: .9rem;
    }
    .footer span { color: #58a6ff; }

    /* ── Responsive ─────────────────────────────────── */
    @media (max-width: 768px) {
      .nav-links { display: none; }
      .nav-links.open {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 64px;
        right: 0;
        left: 0;
        background: rgba(13,17,23,.97);
        padding: 1.5rem;
        border-bottom: 1px solid #21262d;
      }
      .nav-toggle { display: flex; }
      .hero h1 { font-size: 2rem; }
      .hero .subtitle { font-size: 1rem; }
      .about-grid { grid-template-columns: 1fr; }
      .about-highlights { grid-template-columns: 1fr 1fr; }
    }
  </style>
</head>
<body>

  <!-- ── Navbar ──────────────────────────────────── -->
  <nav class="navbar" id="navbar">
    <div class="container">
      <a href="#" class="nav-logo">AZIIZ</a>
      <ul class="nav-links" id="navLinks">
        <li><a href="#hero">الرئيسية</a></li>
        <li><a href="#about">عني</a></li>
        <li><a href="#skills">المهارات</a></li>
        <li><a href="#stats">الإحصائيات</a></li>
        <li><a href="#contact">تواصل</a></li>
      </ul>
      <button class="nav-toggle" id="navToggle" aria-label="Toggle menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </nav>

  <!-- ── Hero ────────────────────────────────────── -->
  <section class="hero" id="hero">
    <div class="particles">
      <span></span><span></span><span></span><span></span><span></span>
    </div>
    <div class="hero-content fade-in">
      <img
        src="https://github.com/AZIIZALOYIBI.png"
        alt="Aziiz Aloyibi"
        class="hero-avatar"
      />
      <h1>AZIIZ ALOYIBI</h1>
      <p class="subtitle">مطوّر Full-Stack &nbsp;|&nbsp; مساهم في المصادر المفتوحة</p>
      <div class="cta-group">
        <a href="https://github.com/AZIIZALOYIBI" class="btn btn-primary" target="_blank" rel="noopener">
          &#128187; GitHub
        </a>
        <a href="mailto:aziizaloyibi@gmail.com" class="btn btn-outline">
          &#9993; تواصل معي
        </a>
      </div>
    </div>
  </section>

  <!-- ── About ───────────────────────────────────── -->
  <section class="section" id="about">
    <div class="container">
      <h2 class="section-title fade-in">👨‍💻 عني</h2>
      <div class="about-grid">
        <div class="about-text fade-in d1">
          <p>
            أنا <strong style="color:#e6edf3;">عزيز العويبي</strong>، مطوّر Full-Stack شغوف ببناء تطبيقات ويب عالية الأداء وقابلة للتوسع.
          </p>
          <p>
            أسعى دائمًا لتعلم تقنيات جديدة والمساهمة في مشاريع المصادر المفتوحة، مع التركيز على كتابة كود نظيف واتباع أفضل الممارسات.
          </p>
          <p>
            أتعلم حاليًا: <strong style="color:#58a6ff;">Cloud Architecture</strong>، <strong style="color:#58a6ff;">DevOps</strong>، <strong style="color:#58a6ff;">AI/ML</strong>
          </p>
        </div>
        <div class="about-highlights fade-in d2">
          <div class="highlight-card">
            <div class="icon">🚀</div>
            <h4>تطبيقات قابلة للتوسع</h4>
          </div>
          <div class="highlight-card">
            <div class="icon">🌟</div>
            <h4>مصادر مفتوحة</h4>
          </div>
          <div class="highlight-card">
            <div class="icon">🧹</div>
            <h4>كود نظيف</h4>
          </div>
          <div class="highlight-card">
            <div class="icon">🤝</div>
            <h4>تعاون وعمل جماعي</h4>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── Skills ──────────────────────────────────── -->
  <section class="section" id="skills" style="background:#161b2233;">
    <div class="container">
      <h2 class="section-title fade-in">🛠️ المهارات والأدوات</h2>
      <div class="skills-grid">
        <div class="skill-category fade-in d1">
          <h3>🎨 الواجهة الأمامية</h3>
          <div class="skill-tags">
            <span class="skill-tag">HTML5</span>
            <span class="skill-tag">CSS3</span>
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">TypeScript</span>
            <span class="skill-tag">React</span>
            <span class="skill-tag">Next.js</span>
            <span class="skill-tag">Tailwind CSS</span>
          </div>
        </div>
        <div class="skill-category fade-in d2">
          <h3>⚙️ الواجهة الخلفية</h3>
          <div class="skill-tags">
            <span class="skill-tag">Node.js</span>
            <span class="skill-tag">Python</span>
            <span class="skill-tag">Express.js</span>
            <span class="skill-tag">FastAPI</span>
          </div>
        </div>
        <div class="skill-category fade-in d3">
          <h3>🗄️ قواعد البيانات</h3>
          <div class="skill-tags">
            <span class="skill-tag">PostgreSQL</span>
            <span class="skill-tag">MongoDB</span>
            <span class="skill-tag">Redis</span>
            <span class="skill-tag">MySQL</span>
          </div>
        </div>
        <div class="skill-category fade-in d4">
          <h3>🔧 DevOps والأدوات</h3>
          <div class="skill-tags">
            <span class="skill-tag">Git</span>
            <span class="skill-tag">GitHub</span>
            <span class="skill-tag">Docker</span>
            <span class="skill-tag">Linux</span>
            <span class="skill-tag">VS Code</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── GitHub Stats ────────────────────────────── -->
  <section class="section" id="stats">
    <div class="container">
      <h2 class="section-title fade-in">📊 إحصائيات GitHub</h2>
      <div class="stats-cards fade-in d1">
        <img
          src="https://github-readme-stats.vercel.app/api?username=AZIIZALOYIBI&show_icons=true&theme=github_dark&include_all_commits=true&count_private=true&hide_border=true&bg_color=161b22&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9"
          alt="GitHub Stats"
          loading="lazy"
        />
        <img
          src="https://github-readme-stats.vercel.app/api/top-langs/?username=AZIIZALOYIBI&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22&title_color=58a6ff&text_color=c9d1d9"
          alt="Top Languages"
          loading="lazy"
        />
      </div>
      <div class="stats-cards fade-in d2" style="margin-top:1.5rem;">
        <img
          src="https://github-readme-streak-stats.herokuapp.com/?user=AZIIZALOYIBI&theme=github-dark-blue&hide_border=true&background=161b22&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff"
          alt="GitHub Streak"
          loading="lazy"
        />
      </div>
    </div>
  </section>

  <!-- ── Contact ─────────────────────────────────── -->
  <section class="section" id="contact" style="background:#161b2233;">
    <div class="container">
      <h2 class="section-title fade-in">🤝 تواصل معي</h2>
      <div class="contact-links fade-in d1">
        <a href="https://github.com/AZIIZALOYIBI" class="contact-card" target="_blank" rel="noopener">
          <span class="c-icon">&#128025;</span> GitHub
        </a>
        <a href="https://www.linkedin.com/in/" class="contact-card" target="_blank" rel="noopener">
          <span class="c-icon">&#128188;</span> LinkedIn
        </a>
        <a href="https://x.com/" class="contact-card" target="_blank" rel="noopener">
          <span class="c-icon">&#128172;</span> X (Twitter)
        </a>
        <a href="mailto:aziizaloyibi@gmail.com" class="contact-card">
          <span class="c-icon">&#9993;</span> البريد الإلكتروني
        </a>
      </div>
    </div>
  </section>

  <!-- ── Footer ──────────────────────────────────── -->
  <footer class="footer">
    <div class="container">
      <p>&copy; 2026 <span>AZIIZ ALOYIBI</span>. جميع الحقوق محفوظة.</p>
    </div>
  </footer>

  <!-- ── Scripts ─────────────────────────────────── -->
  <script>
    // Mobile nav toggle
    document.getElementById('navToggle').addEventListener('click', function () {
      document.getElementById('navLinks').classList.toggle('open');
    });

    // Close menu on link click
    document.querySelectorAll('.nav-links a').forEach(function (link) {
      link.addEventListener('click', function () {
        document.getElementById('navLinks').classList.remove('open');
      });
    });

    // Intersection Observer for fade-in animations
    const observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.style.animationPlayState = 'running';
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.15 });

    document.querySelectorAll('.fade-in').forEach(function (el) {
      el.style.animationPlayState = 'paused';
      observer.observe(el);
    });

    // Navbar shrink on scroll
    window.addEventListener('scroll', function () {
      const navbar = document.getElementById('navbar');
      if (window.scrollY > 50) {
        navbar.style.background = 'rgba(13,17,23,.98)';
      } else {
        navbar.style.background = 'rgba(13,17,23,.92)';
      }
    });
  </script>
</body>
</html>🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
