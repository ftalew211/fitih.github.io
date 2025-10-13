<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Ftalew Dagnaw | Professional Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    /* Root variables for consistent theming */
    :root {
      --primary-blue: #0d47a1;
      --secondary-blue: #1976d2;
      --accent-cyan: #64b5f6;
      --light-bg: rgba(255, 255, 255, 0.1);
      --card-bg: rgba(255, 255, 255, 0.18);
      --text-light: #f5f9ff;
      --text-muted: #d0e2ff;
      --max-width: 1100px;
      --transition: 0.3s ease;
      --shadow: 0 20px 40px rgba(0, 0, 0, 0.25);
    }

    /* Global resets */
    *, *::before, *::after {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: "Inter", "Helvetica Neue", Arial, sans-serif;
      color: var(--text-light);
      background: linear-gradient(140deg, #021b79 0%, #0575e6 100%);
      min-height: 100vh;
      scroll-behavior: smooth;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* Layout utility classes */
    .container {
      width: min(92%, var(--max-width));
      margin: 0 auto;
    }

    .section {
      padding: clamp(3rem, 5vw, 5rem) 0;
    }

    /* Navigation */
    header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(2, 27, 121, 0.9);
      backdrop-filter: blur(16px);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1rem 0;
    }

    .nav__brand {
      font-weight: 700;
      font-size: 1.15rem;
      letter-spacing: 0.05em;
    }

    .nav__links {
      display: flex;
      gap: 1.25rem;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    .nav__links a {
      padding: 0.5rem 0.75rem;
      border-radius: 999px;
      transition: background-color var(--transition);
    }

    .nav__links a:hover, .nav__links a:focus {
      background-color: rgba(255, 255, 255, 0.14);
    }

    .nav__toggle {
      display: none;
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.4);
      color: var(--text-light);
      padding: 0.4rem 0.65rem;
      border-radius: 6px;
      cursor: pointer;
    }

    /* Hero */
    .hero {
      display: grid;
      gap: clamp(1.5rem, 4vw, 3rem);
      align-items: center;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    }

    .hero__text h1 {
      font-size: clamp(2rem, 5vw, 3.1rem);
      margin: 0 0 1rem;
    }

    .hero__text p {
      margin: 0 0 1.5rem;
      line-height: 1.7;
      color: var(--text-muted);
    }

    .hero__cta {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: var(--accent-cyan);
      color: #01274a;
      padding: 0.85rem 1.6rem;
      border-radius: 999px;
      font-weight: 600;
      box-shadow: var(--shadow);
      transition: transform var(--transition), box-shadow var(--transition);
    }

    .hero__cta:hover {
      transform: translateY(-3px);
      box-shadow: 0 24px 48px rgba(6, 72, 140, 0.35);
    }

    .hero__image {
      position: relative;
      justify-self: center;
    }

    .hero__image::after {
      content: "";
      position: absolute;
      inset: 10%;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(25, 118, 210, 0.4), rgba(100, 181, 246, 0.3));
      filter: blur(40px);
      z-index: -1;
    }

    .hero__portrait {
      border-radius: 20px;
      border: 3px solid rgba(255, 255, 255, 0.35);
      box-shadow: var(--shadow);
      object-fit: cover;
      width: min(320px, 90%);
      aspect-ratio: 3 / 4;
    }

    /* Cards & sections */
    .card {
      background: var(--card-bg);
      border: 1px solid rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      padding: clamp(1.5rem, 2vw, 2rem);
      box-shadow: 0 16px 32px rgba(0, 0, 0, 0.18);
      backdrop-filter: blur(18px);
    }

    .grid {
      display: grid;
      gap: clamp(1.5rem, 3vw, 2.5rem);
    }

    .grid--two {
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.4rem 0.8rem;
      background: rgba(255, 255, 255, 0.12);
      border-radius: 999px;
      font-size: 0.85rem;
      margin: 0 0.5rem 0.5rem 0;
    }

    ul {
      padding-left: 1.25rem;
      margin: 0;
    }

    ul li {
      margin-bottom: 0.6rem;
      line-height: 1.6;
    }

    h2 {
      font-size: clamp(1.6rem, 3.2vw, 2.15rem);
      margin: 0 0 1.5rem;
    }

    h3 {
      margin: 0 0 1rem;
      font-size: 1.25rem;
    }

    .experience__item + .experience__item {
      padding-top: 1.5rem;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }

    .experience__role {
      font-weight: 600;
    }

    .experience__meta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin: 0.6rem 0 1rem;
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    /* Course progress section */
    .course-overview {
      display: grid;
      gap: 2.5rem;
    }

    .course-summary {
      display: grid;
      gap: 1.5rem;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    }

    .course-progress {
      display: grid;
      gap: 1.5rem;
    }

    .lesson {
      background: rgba(2, 27, 121, 0.6);
      border: 1px solid rgba(100, 181, 246, 0.25);
      border-radius: 16px;
      padding: 1.25rem;
      display: grid;
      gap: 0.85rem;
      transition: transform var(--transition), box-shadow var(--transition);
    }

    .lesson:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 30px rgba(5, 60, 120, 0.35);
    }

    .lesson__header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
    }

    .lesson__header h4 {
      margin: 0;
      font-size: 1.05rem;
    }

    .lesson__status {
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      font-size: 0.9rem;
      color: var(--accent-cyan);
    }

    .progress-bar {
      position: relative;
      width: 100%;
      height: 8px;
      background: rgba(255, 255, 255, 0.16);
      border-radius: 999px;
      overflow: hidden;
    }

    .progress-bar span {
      display: block;
      height: 100%;
      width: 0%;
      background: linear-gradient(90deg, #64b5f6 0%, #bbdefb 100%);
      transition: width 0.4s ease;
    }

    .course-footer {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      justify-content: space-between;
      background: rgba(9, 46, 110, 0.7);
      border-radius: 16px;
      padding: 1.5rem;
    }

    /* Contact section */
    .contact-card {
      display: grid;
      gap: 1rem;
    }

    .contact-list {
      list-style: none;
      padding: 0;
      margin: 0;
      display: grid;
      gap: 0.75rem;
    }

    .contact-list li {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      padding: 0.85rem 1rem;
      background: rgba(255, 255, 255, 0.12);
      border-radius: 12px;
    }

    .contact-list span {
      font-weight: 600;
    }

    /* Footer */
    footer {
      padding: 2rem 0 3rem;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    /* Responsive navigation */
    @media (max-width: 760px) {
      .nav__links {
        position: absolute;
        inset: 60px 1rem auto;
        background: rgba(1, 19, 70, 0.95);
        border-radius: 16px;
        padding: 1.2rem;
        flex-direction: column;
        gap: 1rem;
        opacity: 0;
        visibility: hidden;
        transform: translateY(-10px);
        transition: opacity var(--transition), transform var(--transition);
      }

      .nav__links.is-open {
        opacity: 1;
        visibility: visible;
        transform: translateY(0);
      }

      .nav__toggle {
        display: inline-flex;
      }
    }
  </style>
</head>
<body>
  <!-- Navigation -->
  <header>
    <div class="container nav">
      <div class="nav__brand">Ftalew Dagnaw | MPH, M&E Specialist</div>
      <button class="nav__toggle" aria-expanded="false" aria-controls="primary-navigation">
        Menu
      </button>
      <ul class="nav__links" id="primary-navigation">
        <li><a href="#profile">Profile</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#course">Generative AI Bootcamp</a></li>
        <li><a href="#contact">Organization Contact</a></li>
      </ul>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="section">
    <div class="container hero">
      <div class="hero__text">
        <h1>Transforming Health Systems with Data-Driven Insight</h1>
        <p>
          I am Ftalew Dagnaw Gebreyesus, a Senior Monitoring &amp; Evaluation Advisor at Ethiopia’s Ministry of Health. With over 15 years of experience leading national health information systems, program evaluations, and quality improvement initiatives, I align data ecosystems with strategic priorities to elevate public health outcomes.
        </p>
        <a class="hero__cta" href="#course">
          Explore My AI Bootcamp Progress
        </a>
      </div>
      <div class="hero__image">
        <!-- Replace the src value with the correct path or data URI of your portrait -->
        <img class="hero__portrait" src="assets/ftalew-portrait.jpg" alt="Portrait of Ftalew Dagnaw Gebreyesus" />
      </div>
    </div>
  </section>

  <!-- Professional Profile -->
  <section class="section" id="profile">
    <div class="container grid grid--two">
      <article class="card">
        <h2>Professional Snapshot</h2>
        <p>
          Results-driven Monitoring &amp; Evaluation professional with a Master of Public Health and a B.Sc. in Statistics. I specialize in designing, implementing, and optimizing M&amp;E frameworks across national health programs, leveraging platforms like DHIS2 and Power BI to strengthen data quality, equity, and decision-making.
        </p>
        <div>
          <span class="tag">Monitoring &amp; Evaluation Frameworks</span>
          <span class="tag">Health Information Systems</span>
          <span class="tag">Data Analytics &amp; Visualization</span>
          <span class="tag">Strategic Planning</span>
          <span class="tag">Stakeholder Engagement</span>
        </div>
      </article>

      <article class="card">
        <h2>Core Competencies</h2>
        <ul>
          <li>Architecting national M&amp;E systems, dashboards, and reporting pipelines.</li>
          <li>Customizing DHIS2, HMIS indicators, and data tools aligned with health priorities.</li>
          <li>Leading capacity building, onsite mentorship, and quality assurance programs.</li>
          <li>Integrating maternal, perinatal, and quality metrics into national surveillance systems.</li>
          <li>Publishing insights and best practices that drive policy and programmatic improvement.</li>
        </ul>
      </article>
    </div>
  </section>

  <!-- Experience Highlights -->
  <section class="section" id="experience">
    <div class="container card">
      <h2>Experience Highlights</h2>
      <div class="experience__item">
        <div class="experience__role">Senior Monitoring &amp; Evaluation Advisor · Ministry of Health, Ethiopia</div>
        <div class="experience__meta">
          <span>July 2019 – Present</span>
          <span>Addis Ababa, Ethiopia</span>
        </div>
        <ul>
          <li>Lead design and execution of M&amp;E plans for national healthcare quality, innovation, and equity initiatives.</li>
          <li>Modernized national HMIS indicators, reporting forms, and DHIS2 implementations to match sector priorities.</li>
          <li>Advanced integration of ICD-11, effective coverage metrics, and responsive dashboards to improve data use.</li>
          <li>Guided sub-national mentorship, learning forums, and publications to scale quality improvement practices.</li>
        </ul>
      </div>

      <div class="experience__item">
        <div class="experience__role">Data Manager &amp; Analyst · World Health Organization Ethiopia</div>
        <div class="experience__meta">
          <span>Sept 2014 – July 2019</span>
          <span>Addis Ababa, Ethiopia</span>
        </div>
        <ul>
          <li>Co-developed the national Maternal &amp; Perinatal Death Surveillance &amp; Response (MPDSR) framework and database.</li>
          <li>Integrated MPDSR with Public Health Emergency Management systems, ensuring actionable intelligence flow.</li>
          <li>Built national capacity through trainings, supportive supervision, and knowledge dissemination.</li>
        </ul>
      </div>

      <div class="experience__item">
        <div class="experience__role">Monitoring &amp; Evaluation Roles · CHAI, USAID Programs, Save the Children, I-TECH</div>
        <div class="experience__meta">
          <span>2006 – 2014</span>
          <span>Ethiopia</span>
        </div>
        <ul>
          <li>Strengthened vaccine program M&amp;E systems, led PMP compliance, and coordinated project evaluations.</li>
          <li>Executed routine data quality assessments, surveys, and evidence-based reporting for USAID-funded programs.</li>
          <li>Managed HIV/AIDS data ecosystems, training, and performance analytics across regional facilities.</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Generative AI Course Progress -->
  <section class="section" id="course">
    <div class="container card">
      <h2>Generative AI for Work &amp; Research Productivity Bootcamp 2025 Q4</h2>
      <p>
        Hands-on 8-week program from <strong>The GRAPH Courses</strong> focused on leveraging AI for productivity, literature reviews, data analysis, chatbot design, workflow automation, and creative media—without requiring coding expertise.
      </p>

      <div class="course-overview">
        <div class="course-summary">
          <div class="lesson">
            <div class="lesson__header">
              <h4>Program Snapshot</h4>
            </div>
            <ul>
              <li>Duration: 8 weeks · Live &amp; applied learning</li>
              <li>Includes: 7 Lessons · 1 Topic · 1 Quiz</li>
              <li>Status: Enrollment confirmed (Course currently closed to new participants)</li>
            </ul>
          </div>

          <div class="lesson">
            <div class="lesson__header">
              <h4>Key Outcomes</h4>
            </div>
            <ul>
              <li>Create professional websites, documents, and presentations with AI assistance.</li>
              <li>Conduct literature reviews, analyze data, and build dashboards using intuitive AI tools.</li>
              <li>Design custom chatbots and automate workflows aligned with health-sector use cases.</li>
              <li>Produce and edit images, videos, and design materials powered by AI.</li>
            </ul>
          </div>
        </div>

        <div class="course-progress">
          <div class="lesson">
            <div class="lesson__header">
              <h4>Lesson Progress Tracker</h4>
              <div class="lesson__status" id="overall-status">
                Overall Progress: <strong><span id="overall-percentage">0</span>%</strong>
              </div>
            </div>
            <div class="progress-bar" aria-hidden="true">
              <span id="overall-progress"></span>
            </div>
            <p style="color: var(--text-muted); margin: 0;">
              Mark each lesson as you complete it to visualize advancement through the bootcamp modules.
            </p>
          </div>

          <div class="grid grid--two" aria-live="polite">
            <!-- Individual lesson cards with checkboxes -->
            <label class="lesson">
              <div class="lesson__header">
                <h4>01 · Getting Started with AI Productivity Tools</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Orientation to generative AI platforms, capabilities, and practical workflows for daily tasks.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>02 · AI-Assisted Documents &amp; Presentations</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Building professional websites, reports, and decks rapidly with co-creative AI tools.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>03 · Literature Reviews &amp; Data Exploration</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Conducting evidence scans and exploratory analysis without coding, using AI agents.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>04 · No-Code Dashboards &amp; Insights</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Designing KPIs and visual dashboards powered by intuitive AI data interfaces.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>05 · Domain-Specific Chatbots</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Crafting responsive chatbots capable of answering health program and policy queries.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>06 · Automated Workflows</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Configuring end-to-end automations that operate around the clock to streamline operations.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>07 · AI for Creative Media Production</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Producing and editing images, videos, and design assets tailored to stakeholder communication.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>Capstone Topic · Real-World Implementation Lab</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Applying bootcamp learnings to a live project that aligns with Ministry of Health priorities.
              </p>
            </label>

            <label class="lesson">
              <div class="lesson__header">
                <h4>Quiz · AI Productivity Foundations</h4>
                <input type="checkbox" class="lesson-checkbox" />
              </div>
              <p style="color: var(--text-muted); margin: 0;">
                Demonstrating mastery of core concepts, tools, and responsible use considerations.
              </p>
            </label>
          </div>
        </div>

        <div class="course-footer">
          <div>
            <strong>Course Access:</strong> Login required (<a href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank" rel="noopener">Visit course page</a>)
          </div>
          <div>
            Cohort: Q4 2025 · Provider: The GRAPH Network
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="section" id="contact">
    <div class="container card contact-card">
      <h2>Current Organization Contact</h2>
      <p>
        Ministry of Health, Federal Democratic Republic of Ethiopia – primary liaison for Monitoring &amp; Evaluation initiatives, health information system strengthening, and national quality programs.
      </p>
      <ul class="contact-list">
        <li>
          <span>Address:</span>
          Swaziland Street, Gulele Sub-City, Addis Ababa, Ethiopia
        </li>
        <li>
          <span>Phone:</span>
          +251-11-551-8080
        </li>
        <li>
          <span>Email:</span>
          moh@ethionet.et
        </li>
      </ul>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    © 2025 Ftalew Dagnaw Gebreyesus · Elevating public health through data, equity, and innovation.
  </footer>

  <script>
    // Mobile navigation toggle logic
    const navToggle = document.querySelector('.nav__toggle');
    const navLinks = document.querySelector('.nav__links');

    navToggle.addEventListener('click', () => {
      const isOpen = navLinks.classList.toggle('is-open');
      navToggle.setAttribute('aria-expanded', isOpen);
    });

    // Course progress tracking
    const checkboxes = document.querySelectorAll('.lesson-checkbox');
    const overallProgress = document.getElementById('overall-progress');
    const overallPercentage = document.getElementById('overall-percentage');

    function updateProgress() {
      const completed = Array.from(checkboxes).filter(box => box.checked).length;
      const total = checkboxes.length;
      const percent = Math.round((completed / total) * 100);

      overallProgress.style.width = `${percent}%`;
      overallPercentage.textContent = percent;
    }

    // Initialize progress and bind events
    checkboxes.forEach(box => {
      box.addEventListener('change', updateProgress);
    });

    updateProgress();
  </script>
</body>
</html>
