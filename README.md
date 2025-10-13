<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ftalew Dagnaw | Professional Portfolio</title>

  <!-- ===== Embedded CSS ===== -->
  <style>
    /* ===== Global Styles ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    body {
      background: #f9f9f9;
      color: #333;
      line-height: 1.6;
    }

    /* ===== Navbar ===== */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background: #004aad;
      color: white;
    }
    .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }
    .nav-links {
      display: flex;
      list-style: none;
    }
    .nav-links li {
      margin-left: 1.5rem;
    }
    .nav-links a {
      color: white;
      text-decoration: none;
      transition: color 0.3s;
    }
    .nav-links a:hover {
      color: #ffcc00;
    }
    .menu-toggle {
      display: none;
      font-size: 1.8rem;
      cursor: pointer;
    }

    /* ===== Hero Section ===== */
    .hero {
      text-align: center;
      padding: 3rem 1rem;
      background: linear-gradient(120deg, #004aad, #0099cc);
      color: white;
    }
    .profile-pic {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      margin-bottom: 1rem;
      object-fit: cover;
    }
    .hero h1 {
      font-size: 2rem;
      margin-bottom: 0.5rem;
    }
    .hero p {
      font-size: 1.2rem;
    }

    /* ===== Section ===== */
    .section {
      padding: 3rem 2rem;
      max-width: 1000px;
      margin: auto;
    }
    .section h2 {
      margin-bottom: 1rem;
      font-size: 1.8rem;
      color: #004aad;
    }
    .skills-list {
      list-style: disc;
      padding-left: 2rem;
    }

    /* ===== Course Progress ===== */
    .course-progress .lesson {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 0.5rem 0;
    }
    progress {
      width: 50%;
      height: 15px;
    }

    /* ===== Contact Section ===== */
    .contact-section p {
      margin: 0.5rem 0;
    }
    .contact-section a {
      color: #004aad;
    }

    /* ===== Footer ===== */
    footer {
      background: #004aad;
      color: white;
      text-align: center;
      padding: 1rem;
    }

    /* ===== Responsive Design ===== */
    @media (max-width: 768px) {
      .nav-links {
        position: absolute;
        top: 60px;
        right: 0;
        background: #004aad;
        flex-direction: column;
        width: 200px;
        display: none;
      }
      .nav-links.active {
        display: flex;
      }
      .nav-links li {
        margin: 1rem 0;
      }
      .menu-toggle {
        display: block;
      }
      progress {
        width: 100%;
      }
    }
  </style>
</head>

<body>
  <!-- ===== Navigation Bar ===== -->
  <header>
    <nav class="navbar">
      <div class="logo">Ftalew Dagnaw</div>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#course">AI Course</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="menu-toggle" id="menu-toggle">☰</div>
    </nav>
  </header>

  <!-- ===== Hero Section ===== -->
  <section class="hero">
    <img src="Me.jpeg" alt="Ftalew Dagnaw" class="profile-pic" />
    <h1>Welcome to My Professional Portfolio</h1>
    <p>Senior Monitoring & Evaluation Advisor | Data & Health Systems Expert</p>
  </section>

  <!-- ===== About Section ===== -->
  <section id="about" class="section">
    <h2>About Me</h2>
    <p>
      I am a results-driven Monitoring and Evaluation (M&E) professional with over 15 years of experience in designing, implementing, and managing M&E frameworks and systems in Ethiopia's healthcare sector. I specialize in data systems strengthening, strategic planning, and stakeholder engagement to enhance national health program outcomes.
    </p>
  </section>

  <!-- ===== Skills Section ===== -->
  <section id="skills" class="section">
    <h2>Core Competencies</h2>
    <ul class="skills-list">
      <li>Monitoring & Evaluation Frameworks (M&E)</li>
      <li>Data Analysis & Visualization (Power BI, DHIS2)</li>
      <li>Health Information System Strengthening</li>
      <li>Strategic Planning & Reporting</li>
      <li>Stakeholder Engagement & Collaboration</li>
    </ul>
  </section>

  <!-- ===== AI Course Section ===== -->
  <section id="course" class="section">
    <h2>Generative AI Course Module</h2>
    <p>
      I am currently enrolled in the <a href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank">Generative AI Course (Q4 2025)</a>.
    </p>
    <div class="course-progress">
      <div class="lesson">
        <span>Lesson 1: Introduction to Generative AI</span>
        <progress value="100" max="100"></progress>
      </div>
      <div class="lesson">
        <span>Lesson 2: Model Architectures</span>
        <progress value="60" max="100"></progress>
      </div>
      <div class="lesson">
        <span>Lesson 3: Applications and Ethics</span>
        <progress value="30" max="100"></progress>
      </div>
    </div>
  </section>

  <!-- ===== Contact Section ===== -->
  <section id="contact" class="section contact-section">
    <h2>Contact Information</h2>
    <p><strong>Organization:</strong> Ministry of Health, Ethiopia</p>
    <p><strong>Address:</strong> Addis Ababa, Ethiopia</p>
    <p><strong>Phone:</strong> +251-911061646</p>
    <p><strong>Email:</strong> 
      <a href="mailto:ftalewd211@gmail.com">ftalewd211@gmail.com</a> | 
      <a href="mailto:ftalew.dagnaw@moh.gov.et">ftalew.dagnaw@moh.gov.et</a>
    </p>
  </section>

  <!-- ===== Footer ===== -->
  <footer>
    <p>© 2025 Ftalew Dagnaw. All Rights Reserved.</p>
  </footer>

  <!-- ===== Embedded JavaScript ===== -->
  <script>
    // ===== Mobile Menu Toggle =====
    const toggle = document.getElementById('menu-toggle');
    const navLinks = document.querySelector('.nav-links');

    toggle.addEventListener('click', () => {
      navLinks.classList.toggle('active');
    });

    // ===== Smooth Scroll =====
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
        navLinks.classList.remove('active');
      });
    });
  </script>
</body>
</html>
