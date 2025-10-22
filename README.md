<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SharkTech | Smart Digital Solutions</title>
  <style>
    /* --- RESET --- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: #050915;
      color: #fff;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }

    /* --- NAVIGATION BAR --- */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 60px;
      background: rgba(0, 0, 0, 0.5);
      backdrop-filter: blur(10px);
      z-index: 1000;
      border-bottom: 1px solid rgba(0, 255, 255, 0.2);
    }

    .logo {
      font-size: 1.8rem;
      font-weight: 700;
      color: #0ff;
      text-shadow: 0 0 10px #0ff;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 30px;
    }

    nav ul li a {
      color: #cfefff;
      text-decoration: none;
      font-weight: 500;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #0ff;
      text-shadow: 0 0 10px #0ff;
    }

    /* --- HERO SECTION --- */
    .hero {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-align: center;
      position: relative;
      overflow: hidden;
      padding-top: 100px;
    }

    .hero::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle at center, #0ff3ff15, #0ff3ff05),
                  linear-gradient(115deg, #0ff3ff33 1px, transparent 1px),
                  linear-gradient(245deg, #0ff3ff33 1px, transparent 1px);
      background-size: 100px 100px;
      animation: moveBackground 20s linear infinite;
      z-index: 0;
    }

    @keyframes moveBackground {
      0% { transform: translate(0, 0); }
      100% { transform: translate(-50px, -50px); }
    }

    .content {
      position: relative;
      z-index: 2;
      max-width: 800px;
      padding: 0 20px;
      animation: fadeInUp 2s ease-out;
    }

    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(40px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    h1 {
      font-size: 3rem;
      line-height: 1.2;
      color: #0ff;
      text-shadow: 0 0 20px #0ff;
      animation: glowPulse 3s infinite alternate;
    }

    @keyframes glowPulse {
      0% { text-shadow: 0 0 10px #0ff; }
      100% { text-shadow: 0 0 25px #0ff; }
    }

    p {
      font-size: 1.2rem;
      margin: 20px 0 40px;
      color: #cfefff;
    }

    .btn-group {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    a.btn {
      text-decoration: none;
      background: #0ff;
      color: #000;
      padding: 12px 30px;
      border-radius: 50px;
      font-weight: 600;
      letter-spacing: 0.5px;
      transition: all 0.3s ease;
      box-shadow: 0 0 15px #0ff;
    }

    a.btn:hover {
      background: #00d4ff;
      box-shadow: 0 0 25px #00eaff, 0 0 40px #00eaff;
      transform: scale(1.05);
    }

    /* --- FLOATING EFFECT --- */
    .floating {
      animation: floatUpDown 5s ease-in-out infinite;
    }

    @keyframes floatUpDown {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }

    /* --- SECTION: SERVICES --- */
    section#services {
      background: #0a0f20;
      padding: 100px 20px;
      text-align: center;
    }

    #services h2 {
      font-size: 2.5rem;
      color: #0ff;
      margin-bottom: 40px;
      text-shadow: 0 0 10px #0ff;
    }

    .service-boxes {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 40px;
    }

    .service {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(0, 255, 255, 0.2);
      border-radius: 15px;
      padding: 40px;
      width: 280px;
      transition: 0.3s;
    }

    .service:hover {
      background: rgba(0, 255, 255, 0.1);
      transform: translateY(-10px);
      box-shadow: 0 0 20px #0ff3;
    }

    .service h3 {
      color: #0ff;
      margin-bottom: 15px;
    }

    /* --- FOOTER --- */
    footer {
      text-align: center;
      padding: 30px;
      background: #050915;
      border-top: 1px solid rgba(0, 255, 255, 0.2);
      color: #aaa;
    }

    /* --- RESPONSIVE --- */
    @media (max-width: 768px) {
      header { padding: 15px 25px; }
      nav ul { gap: 15px; }
      h1 { font-size: 2.2rem; }
      p { font-size: 1rem; }
      .service { width: 100%; max-width: 350px; }
    }

  </style>
</head>
<body>

  <!-- NAVBAR -->
  <header>
    <div class="logo">SharkTech</div>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- HERO SECTION -->
  <section class="hero" id="hero">
    <div class="content floating">
      <h1>Empower Your Business with Smart Digital Solutions</h1>
      <p>At <strong>SharkTech</strong>, we build powerful websites, CRM systems, and POS platforms that help businesses automate, grow, and stay ahead in the digital era.</p>
      <div class="btn-group">
        <a href="#services" class="btn">Get Your Free Demo</a>
        <a href="#contact" class="btn">Start Your Project</a>
      </div>
    </div>
  </section>

  <!-- SERVICES SECTION -->
  <section id="services">
    <h2>Our Services</h2>
    <div class="service-boxes">
      <div class="service">
        <h3>Website Development</h3>
        <p>Responsive, fast, and professional websites for small businesses and startups.</p>
      </div>
      <div class="service">
        <h3>CRM Systems</h3>
        <p>Custom CRM solutions that streamline your workflow and boost productivity.</p>
      </div>
      <div class="service">
        <h3>POS Systems</h3>
        <p>Modern POS websites with inventory, billing, and analytics features.</p>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer id="contact">
    <p>Â© 2025 SharkTech â€” Smart Digital Solutions for Modern Businesses</p>
  </footer>

</body>
</html>
