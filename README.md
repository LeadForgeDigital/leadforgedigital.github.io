
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SmileCare | modern dental clinic</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    }

    body {
      background: #ffffff;
      color: #1e2b3a;
      line-height: 1.5;
    }

    /* helper colours */
    :root {
      --primary: #0b7b7a;
      --primary-light: #e1f0f0;
      --primary-soft: #2fa9a8;
      --accent: #f4b942;
      --accent-light: #fff2db;
      --neutral-bg: #f9fbfd;
      --text-dark: #152b3a;
      --text-soft: #3e5a6b;
      --white: #ffffff;
      --shadow: 0 20px 30px -10px rgba(0, 50, 50, 0.1);
      --radius: 28px;
      --radius-sm: 16px;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 32px;
    }

    /* header / nav */
    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px 0;
      flex-wrap: wrap;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 1.8rem;
      font-weight: 600;
      color: var(--primary);
    }

    .logo i {
      font-size: 2.4rem;
      background: var(--primary-light);
      padding: 10px;
      border-radius: 20px;
    }

    .nav-links {
      display: flex;
      gap: 32px;
      font-weight: 500;
      color: var(--text-soft);
    }

    .nav-links a {
      text-decoration: none;
      color: inherit;
      transition: 0.2s;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    .btn {
      background: var(--primary);
      color: white;
      padding: 12px 28px;
      border-radius: 50px;
      font-weight: 600;
      border: none;
      cursor: pointer;
      font-size: 1rem;
      transition: 0.2s;
      box-shadow: 0 6px 14px rgba(11, 123, 122, 0.3);
      display: inline-block;
      text-decoration: none;
    }

    .btn-outline {
      background: transparent;
      color: var(--primary);
      border: 2px solid var(--primary);
      box-shadow: none;
    }

    .btn-outline:hover {
      background: var(--primary-light);
    }

    /* hero */
    .hero {
      display: flex;
      align-items: center;
      gap: 40px;
      padding: 40px 0 60px;
      flex-wrap: wrap;
    }

    .hero-content {
      flex: 1 1 380px;
    }

    .hero-badge {
      background: var(--accent-light);
      color: #a3550f;
      font-weight: 600;
      font-size: 0.9rem;
      padding: 6px 16px;
      border-radius: 40px;
      display: inline-block;
      margin-bottom: 20px;
      border: 1px solid #ffdcb0;
    }

    .hero-content h1 {
      font-size: 3.4rem;
      font-weight: 700;
      line-height: 1.2;
      letter-spacing: -0.02em;
      color: var(--text-dark);
      margin-bottom: 20px;
    }

    .hero-highlight {
      color: var(--primary);
      border-bottom: 4px solid var(--accent);
    }

    .hero-description {
      font-size: 1.2rem;
      color: var(--text-soft);
      max-width: 520px;
      margin-bottom: 30px;
    }

    .hero-actions {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .hero-image {
      flex: 1 1 380px;
      background: linear-gradient(145deg, #d3f0f0, #b7e2e1);
      border-radius: 50px;
      padding: 20px 20px 0 20px;
      box-shadow: var(--shadow);
      min-height: 320px;
      display: flex;
      align-items: flex-end;
      justify-content: center;
      position: relative;
    }

    .hero-image svg {
      width: 100%;
      max-height: 340px;
      object-fit: contain;
      filter: drop-shadow(0 6px 10px rgba(0,60,60,0.2));
    }

    /* features / services */
    .section-header {
      text-align: center;
      margin: 70px 0 40px;
    }

    .section-header h2 {
      font-size: 2.5rem;
      color: var(--text-dark);
    }

    .section-header p {
      color: var(--text-soft);
      font-size: 1.2rem;
      max-width: 600px;
      margin: 12px auto 0;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 28px;
    }

    .service-card {
      background: white;
      border-radius: var(--radius);
      padding: 32px 22px;
      box-shadow: 0 10px 25px -8px rgba(0,70,70,0.08);
      transition: 0.15s ease;
      border: 1px solid rgba(11, 123, 122, 0.1);
      text-align: center;
    }

    .service-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 30px 35px -14px rgba(11,123,122,0.2);
      border-color: var(--primary-soft);
    }

    .service-icon {
      background: var(--primary-light);
      width: 74px;
      height: 74px;
      border-radius: 30px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 22px;
      font-size: 2.2rem;
      color: var(--primary);
    }

    .service-card h3 {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    .service-card p {
      color: var(--text-soft);
    }

    /* why choose us / stats */
    .stats-row {
      display: flex;
      align-items: center;
      gap: 40px;
      background: var(--primary-light);
      border-radius: 50px;
      padding: 40px 48px;
      margin: 70px 0;
      flex-wrap: wrap;
    }

    .stats-left {
      flex: 1 1 240px;
    }

    .stats-left h3 {
      font-size: 2.2rem;
      font-weight: 700;
      color: var(--text-dark);
    }

    .stats-grid {
      flex: 3 1 400px;
      display: flex;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .stat-item {
      text-align: center;
    }

    .stat-number {
      font-size: 2.8rem;
      font-weight: 700;
      color: var(--primary);
      line-height: 1.2;
    }

    .stat-label {
      color: var(--text-soft);
      font-weight: 500;
    }

    /* team preview / dentists */
    .team-grid {
      display: flex;
      gap: 30px;
      flex-wrap: wrap;
      justify-content: center;
      margin: 50px 0;
    }

    .team-card {
      background: white;
      border-radius: 40px;
      padding: 32px 20px 24px;
      flex: 1 1 200px;
      box-shadow: 0 12px 24px -12px rgba(0,80,80,0.1);
      border: 1px solid #ebf5f5;
      text-align: center;
      transition: 0.2s;
    }

    .team-card:hover {
      background: var(--neutral-bg);
    }

    .team-avatar {
      width: 120px;
      height: 120px;
      background: linear-gradient(145deg, #c2e6e5, #a3d6d5);
      border-radius: 50%;
      margin: 0 auto 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3.4rem;
      color: #08605f;
      border: 4px solid white;
      box-shadow: 0 4px 12px rgba(0,0,0,0.04);
    }

    .team-card h4 {
      font-size: 1.5rem;
      margin-bottom: 6px;
    }

    .team-role {
      color: var(--primary);
      font-weight: 600;
      margin-bottom: 14px;
    }

    /* appointment CTA */
    .cta-banner {
      background: var(--primary);
      color: white;
      border-radius: 60px;
      padding: 54px 48px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 32px;
      margin: 70px 0;
    }

    .cta-text h2 {
      font-size: 2.2rem;
      font-weight: 700;
      margin-bottom: 12px;
    }

    .cta-text p {
      font-size: 1.2rem;
      opacity: 0.85;
      max-width: 500px;
    }

    .cta-btn {
      background: white;
      color: var(--primary);
      font-size: 1.2rem;
      padding: 16px 48px;
      border-radius: 60px;
      font-weight: 700;
      box-shadow: 0 12px 20px -8px rgba(0,30,30,0.4);
      transition: 0.2s;
      border: none;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
    }

    .cta-btn:hover {
      background: var(--accent-light);
      transform: scale(1.02);
    }

    /* footer */
    .footer {
      border-top: 2px solid #e3f0f0;
      padding: 40px 0;
      margin-top: 40px;
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      justify-content: space-between;
      color: var(--text-soft);
    }

    .footer-col p {
      max-width: 260px;
      margin-top: 16px;
    }

    .footer-links {
      display: flex;
      gap: 70px;
      flex-wrap: wrap;
    }

    .footer-links a {
      display: block;
      color: var(--text-soft);
      text-decoration: none;
      margin-bottom: 8px;
    }

    .footer-links a:hover {
      color: var(--primary);
    }

    .social-icons {
      display: flex;
      gap: 20px;
      font-size: 1.5rem;
      margin-top: 16px;
    }

    .social-icons a {
      color: var(--primary);
    }

    .copyright {
      text-align: center;
      padding: 30px 0 10px;
      color: #7b9aa8;
      font-size: 0.9rem;
    }

    /* responsiveness */
    @media (max-width: 700px) {
      .navbar {
        flex-direction: column;
        gap: 20px;
      }
      .hero-content h1 {
        font-size: 2.5rem;
      }
      .stats-row {
        flex-direction: column;
        text-align: center;
      }
      .cta-banner {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- navigation -->
    <nav class="navbar">
      <div class="logo">
        <i class="fas fa-tooth"></i>
        <span>Smile<span style="color:var(--accent);">Care</span></span>
      </div>
      <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">Services</a>
        <a href="#">Team</a>
        <a href="#">Contact</a>
      </div>
      <a href="#" class="btn btn-outline" style="padding: 10px 28px;"> <i class="far fa-calendar-alt" style="margin-right: 8px;"></i>Book now</a>
    </nav>

    <!-- hero section -->
    <div class="hero">
      <div class="hero-content">
        <span class="hero-badge"><i class="fas fa-shield-alt" style="margin-right: 6px;"></i>Safe & gentle dentistry</span>
        <h1>Where <span class="hero-highlight">healthy smiles</span> begin</h1>
        <p class="hero-description">Experience compassionate care with modern technology. Your comfort and healthy smile are our top priorities.</p>
        <div class="hero-actions">
          <a href="#" class="btn"><i class="fas fa-phone-alt" style="margin-right: 8px;"></i> (212) 555 0149</a>
          <a href="#" class="btn btn-outline">See services →</a>
        </div>
        <div style="margin-top: 30px; display: flex; gap: 18px; align-items: center;">
          <span style="display: flex; align-items: center; gap: 6px;"><i class="fas fa-check-circle" style="color:var(--primary);"></i> 24/7 support</span>
          <span style="display: flex; align-items; gap: 6px;"><i class="fas fa-star" style="color:var(--accent);"></i> 5-star reviews</span>
        </div>
      </div>
      <div class="hero-image">
        <!-- friendly vector illustration / tooth character -->
        <svg viewBox="0 0 280 240" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="140" cy="120" r="90" fill="#FEFEFE" stroke="#0B7B7A" stroke-width="2" />
          <path d="M100 110 Q120 85 140 110 Q160 85 180 110" stroke="#0B7B7A" stroke-width="5" fill="none" stroke-linecap="round"/>
          <circle cx="110" cy="90" r="8" fill="#0B7B7A" />
          <circle cx="170" cy="90" r="8" fill="#0B7B7A" />
          <rect x="130" y="130" width="20" height="40" rx="10" fill="#F4B942" />
          <path d="M120 150 L160 150" stroke="#fff" stroke-width="4" stroke-linecap="round"/>
          <circle cx="100" cy="160" r="8" fill="#fff" stroke="#0B7B7A" stroke-width="2" />
          <circle cx="180" cy="160" r="8" fill="#fff" stroke="#0B7B7A" stroke-width="2" />
        </svg>
      </div>
    </div>

    <!-- services -->
    <div class="section-header">
      <h2>Our gentle services</h2>
      <p>Comprehensive dental care for the whole family in a relaxing environment</p>
    </div>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon"><i class="fas fa-tooth"></i></div>
        <h3>Preventive care</h3>
        <p>Cleanings, exams & fluoride treatments to keep your smile bright.</p>
      </div>
      <div class="service-card">
        <div class="service-icon"><i class="fas fa-brush"></i></div>
        <h3>Cosmetic dentistry</h3>
        <p>Whitening, veneers & smile makeovers for confidence.</p>
      </div>
      <div class="service-card">
        <div class="service-icon"><i class="fas fa-robot"></i></div>
        <h3>Digital dentistry</h3>
        <p>Laser, intraoral scanners & painless procedures.</p>
      </div>
      <div class="service-card">
        <div class="service-icon"><i class="fas fa-baby"></i></div>
        <h3>Pediatric care</h3>
        <p>Fun, friendly visits that kids love.</p>
      </div>
    </div>

    <!-- stats / experience -->
    <div class="stats-row">
      <div class="stats-left">
        <h3>Trusted by thousands of families</h3>
      </div>
      <div class="stats-grid">
        <div class="stat-item">
          <div class="stat-number">15+</div>
          <div class="stat-label">years experience</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">12k</div>
          <div class="stat-label">happy patients</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">4.9</div>
          <div class="stat-label">Google rating</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">24/7</div>
          <div class="stat-label">emergency care</div>
        </div>
      </div>
    </div>

    <!-- meet the team -->
    <div class="section-header">
      <h2>Meet your smile specialists</h2>
      <p>Experienced, caring and dedicated to your comfort</p>
    </div>
    <div class="team-grid">
      <div class="team-card">
        <div class="team-avatar"><i class="fas fa-user-md"></i></div>
        <h4>Dr. Emily Chen</h4>
        <div class="team-role">orthodontist</div>
        <p style="font-size:0.95rem;">10+ years creating beautiful smiles</p>
      </div>
      <div class="team-card">
        <div class="team-avatar"><i class="fas fa-user-nurse"></i></div>
        <h4>Dr. Marcus Velez</h4>
        <div class="team-role">implantologist</div>
        <p style="font-size:0.95rem;">pain-free surgery specialist</p>
      </div>
      <div class="team-card">
        <div class="team-avatar"><i class="fas fa-child"></i></div>
        <h4>Dr. Sarah Njoroge</h4>
        <div class="team-role">pediatric dentist</div>
        <p style="font-size:0.95rem;">making kids smile since 2012</p>
      </div>
      <div class="team-card">
        <div class="team-avatar"><i class="fas fa-teeth"></i></div>
        <h4>Dr. James Park</h4>
        <div class="team-role">prosthodontist</div>
        <p style="font-size:0.95rem;">crowns & bridges expert</p>
      </div>
    </div>

    <!-- appointment CTA -->
    <div class="cta-banner">
      <div class="cta-text">
        <h2>Ready for a healthier smile?</h2>
        <p>Book your visit online – it takes only 2 minutes. New patients welcome!</p>
      </div>
      <a href="#" class="cta-btn"><i class="fas fa-calendar-check" style="margin-right: 10px;"></i>Request appointment</a>
    </div>

    <!-- footer -->
    <div class="footer">
      <div class="footer-col">
        <div class="logo" style="margin-bottom: 10px;">
          <i class="fas fa-tooth"></i>
          <span>SmileCare</span>
        </div>
        <p>123 Wellness Avenue, New York, NY 10001<br>contact@smilecare.demo</p>
        <div class="social-icons">
          <a href="#"><i class="fab fa-facebook"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-x-twitter"></i></a>
        </div>
      </div>
      <div class="footer-links">
        <div>
          <strong style="color:var(--text-dark);">quick links</strong><br><br>
          <a href="#">About us</a>
          <a href="#">services</a>
          <a href="#">patient reviews</a>
          <a href="#">insurance</a>
        </div>
        <div>
          <strong style="color:var(--text-dark);">support</strong><br><br>
          <a href="#">FAQ</a>
          <a href="#">emergency</a>
          <a href="#">contact</a>
          <a href="#">privacy</a>
        </div>
      </div>
    </div>
    <div class="copyright">
      © 2025 SmileCare Dental Clinic – demo landing page. All rights reserved.
    </div>
  </div>
  <!-- optional small interaction: smooth hover is already there -->
</body>
</html>
