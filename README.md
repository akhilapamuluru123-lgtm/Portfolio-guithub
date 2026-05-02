# Portfolio-guithub
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Akhila | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
      scroll-behavior: smooth;
    }

    body {
      background: #0f172a;
      color: #f8fafc;
      overflow-x: hidden;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: auto;
    }

    header {
      min-height: 100vh;
      display: flex;
      align-items: center;
      background: linear-gradient(135deg, #0f172a, #1e293b, #111827);
      position: relative;
    }

    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      padding: 18px 0;
      background: rgba(15, 23, 42, 0.9);
      backdrop-filter: blur(10px);
      z-index: 1000;
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }

    .nav-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.7rem;
      font-weight: 700;
      color: #38bdf8;
    }

    .nav-links {
      display: flex;
      gap: 28px;
    }

    .nav-links a {
      text-decoration: none;
      color: #e2e8f0;
      font-size: 0.95rem;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #38bdf8;
    }

    .hero {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      align-items: center;
      gap: 50px;
      width: 100%;
    }

    .hero-text h3 {
      color: #38bdf8;
      font-weight: 500;
      letter-spacing: 1px;
      margin-bottom: 10px;
    }

    .hero-text h1 {
      font-size: 4rem;
      line-height: 1.1;
      margin-bottom: 18px;
    }

    .hero-text p {
      color: #cbd5e1;
      line-height: 1.8;
      margin-bottom: 30px;
      max-width: 600px;
    }

    .btn-group {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 13px 28px;
      border-radius: 12px;
      text-decoration: none;
      font-weight: 600;
      transition: 0.3s ease;
    }

    .primary-btn {
      background: #38bdf8;
      color: #0f172a;
    }

    .primary-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(56, 189, 248, 0.4);
    }

    .secondary-btn {
      border: 1px solid #38bdf8;
      color: #38bdf8;
    }

    .secondary-btn:hover {
      background: #38bdf8;
      color: #0f172a;
    }

    .hero-card {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 35px;
      border-radius: 24px;
      backdrop-filter: blur(10px);
      box-shadow: 0 15px 40px rgba(0,0,0,0.3);
    }

    .hero-card h2 {
      color: #38bdf8;
      margin-bottom: 18px;
      font-size: 1.5rem;
    }

    .info-item {
      margin-bottom: 20px;
    }

    .info-item span {
      color: #94a3b8;
      font-size: 0.9rem;
    }

    .info-item p {
      margin-top: 5px;
      font-weight: 500;
    }

    section {
      padding: 100px 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-title h2 {
      font-size: 2.6rem;
      color: #38bdf8;
      margin-bottom: 10px;
    }

    .section-title p {
      color: #94a3b8;
    }

    .about-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
    }

    .card {
      background: #1e293b;
      border-radius: 20px;
      padding: 30px;
      border: 1px solid rgba(255,255,255,0.05);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 30px rgba(0,0,0,0.3);
    }

    .card h3 {
      margin-bottom: 18px;
      color: #38bdf8;
    }

    .card p, .card li {
      color: #cbd5e1;
      line-height: 1.8;
      font-size: 0.95rem;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
    }

    .skill-box {
      background: #1e293b;
      padding: 25px;
      border-radius: 18px;
      text-align: center;
      border: 1px solid rgba(255,255,255,0.05);
      transition: 0.3s;
    }

    .skill-box:hover {
      background: #38bdf8;
      color: #0f172a;
      transform: translateY(-5px);
    }

    .timeline {
      position: relative;
      max-width: 900px;
      margin: auto;
    }

    .timeline::before {
      content: '';
      position: absolute;
      left: 20px;
      top: 0;
      width: 2px;
      height: 100%;
      background: #38bdf8;
    }

    .timeline-item {
      position: relative;
      padding-left: 60px;
      margin-bottom: 45px;
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      left: 12px;
      top: 5px;
      width: 18px;
      height: 18px;
      border-radius: 50%;
      background: #38bdf8;
    }

    .timeline-item h3 {
      color: #38bdf8;
      margin-bottom: 8px;
    }

    .timeline-item span {
      color: #94a3b8;
      font-size: 0.9rem;
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
    }

    .project-card {
      background: linear-gradient(145deg, #1e293b, #111827);
      padding: 30px;
      border-radius: 24px;
      border: 1px solid rgba(255,255,255,0.05);
      transition: 0.3s;
    }

    .project-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 35px rgba(0,0,0,0.35);
    }

    .project-card h3 {
      color: #38bdf8;
      margin-bottom: 15px;
    }

    .project-card p {
      color: #cbd5e1;
      line-height: 1.8;
      font-size: 0.95rem;
    }

    .contact {
      text-align: center;
      background: linear-gradient(135deg, #0f172a, #111827);
      border-top: 1px solid rgba(255,255,255,0.05);
    }

    .contact h2 {
      color: #38bdf8;
      font-size: 2.5rem;
      margin-bottom: 20px;
    }

    .contact p {
      color: #cbd5e1;
      margin-bottom: 25px;
    }

    .contact-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .contact-links a {
      text-decoration: none;
      padding: 12px 24px;
      background: #1e293b;
      color: #f8fafc;
      border-radius: 12px;
      transition: 0.3s;
      border: 1px solid rgba(255,255,255,0.08);
    }

    .contact-links a:hover {
      background: #38bdf8;
      color: #0f172a;
    }

    footer {
      padding: 25px 0;
      text-align: center;
      background: #020617;
      color: #94a3b8;
      font-size: 0.9rem;
    }

    @media(max-width: 768px) {
      .hero-text h1 {
        font-size: 2.8rem;
      }

      .nav-links {
        gap: 15px;
      }

      .nav-links a {
        font-size: 0.85rem;
      }
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <div class="container nav-content">
      <div class="logo">Akhila Portfolio</div>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#education">Education</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <header>
    <div class="container hero">
      <div class="hero-text">
        <h3>Hello, I'm</h3>
        <h1>Pamuluru Akhila</h1>
        <p>
          Electronics and Communication Engineering graduate with strong foundations in programming, embedded systems, and communication technologies. Passionate about building innovative solutions and contributing to impactful technology-driven projects.
        </p>

        <div class="btn-group">
          <a href="#projects" class="btn primary-btn">View Projects</a>
          <a href="#contact" class="btn secondary-btn">Contact Me</a>
        </div>
      </div>

      <div class="hero-card">
        <h2>Professional Profile</h2>

        <div class="info-item">
          <span>Email</span>
          <p>akhilapamuluru123@gmail.com</p>
        </div>

        <div class="info-item">
          <span>Phone</span>
          <p>+91 9000854275</p>
        </div>

        <div class="info-item">
          <span>Languages</span>
          <p>English, Telugu</p>
        </div>
      </div>
    </div>
  </header>

  <section id="about">
    <div class="container">
      <div class="section-title">
        <h2>About Me</h2>
        <p>Driven by technology, innovation, and continuous learning.</p>
      </div>

      <div class="about-grid">
        <div class="card">
          <h3>Career Objective</h3>
          <p>
            Motivated Electronics and Communication Engineering graduate seeking an opportunity to apply technical skills, learn emerging technologies, and contribute effectively to organizational growth.
          </p>
        </div>


      </div>
    </div>
  </section>

  <section id="skills">
    <div class="container">
      <div class="section-title">
        <h2>Technical Skills</h2>
        <p>Core technologies and programming expertise.</p>
      </div>

      <div class="skills-grid">
        <div class="skill-box">
          <h3>C</h3>
        </div>

        <div class="skill-box">
          <h3>C++</h3>
        </div>

        <div class="skill-box">
          <h3>Python</h3>
        </div>

        <div class="skill-box">
          <h3>SQL</h3>
        </div>
      </div>
    </div>
  </section>

  <section id="education">
    <div class="container">
      <div class="section-title">
        <h2>Education Journey</h2>
        <p>Academic background with consistent performance and technical excellence.</p>
      </div>

      <div class="timeline">

        <div class="timeline-item">
          <h3>Bachelor of Technology - Electronics & Communication Engineering</h3>
          <span>Sathyabama Institute of Science and Technology | 2021 - 2025</span>
          <p>
            Graduated with a CGPA of 8.7 while building strong foundations in communication systems, embedded technologies, IoT, and programming concepts.
          </p>
        </div>

        <div class="timeline-item">
          <h3>Intermediate Education (MPC)</h3>
          <span>Narayana Junior College | 2019 - 2021</span>
          <p>
            Completed higher secondary education with 90.5%, focusing on Mathematics, Physics, and Chemistry.
          </p>
        </div>

        <div class="timeline-item">
          <h3>Secondary School Education</h3>
          <span>SSC Board | 2018 - 2019</span>
          <p>
            Successfully completed schooling with strong academic performance and active participation in academic activities.
          </p>
        </div>

      </div>
    </div>
  </section>

  <section id="projects">
    <div class="container">
      <div class="section-title">
        <h2>Featured Projects</h2>
        <p>Projects built using engineering and software concepts.</p>
      </div>

      <div class="project-grid">
        <div class="project-card">
          <h3>IoT-Based Smart Parking System</h3>
          <p>
            Developed an IoT-driven smart parking solution using real-time sensors to monitor parking availability. Enabled slot reservation and payment features to improve traffic flow and reduce parking congestion.
          </p>
        </div>

        <div class="project-card">
          <h3>MQAM & OFDMA Triple Hop Communication Analysis</h3>
          <p>
            Analysed system performance in mixed RF-FSO-UWOC communication environments by evaluating signal quality, throughput, and system efficiency using MQAM and OFDMA modulation techniques.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container">
      <div class="section-title">
        <h2>Certifications</h2>
        <p>Continuous learning and technical development.</p>
      </div>

      <div class="about-grid">
        <div class="card">
          <h3>Programming Certifications</h3>
          <p>
            Completed certification programs in C Programming and SQL with hands-on learning experience.
          </p>
        </div>

        <div class="card">
          <h3>Machine Learning Using Python</h3>
          <p>
            Participated in Machine Learning Using Python program focusing on practical implementation and data-driven concepts.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section class="contact" id="contact">
    <div class="container">
      <h2>Let's Connect</h2>
      <p>
        Open to opportunities, collaborations, and innovative projects.
      </p>

      <div class="contact-links">
        <a href="mailto:akhilapamuluru123@gmail.com">Email Me</a>
        <a href="tel:+919000854275">Call Me</a>
        <a href="#">LinkedIn</a>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2026 Pamuluru Akhila | Professional Portfolio</p>
  </footer>

</body>
</html>


