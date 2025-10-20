<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Ftalew Dagnaw | Professional Portfolio</title>
  <meta name="description" content="Portfolio of Ftalew Dagnaw Gebreyesus, Senior Monitoring & Evaluation Advisor specializing in health information systems and data-driven public health outcomes." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

    :root {
      --primary-blue: #0c2d64;
      --secondary-blue: #1e4fb8;
      --accent-cyan: #6bdcff;
      --accent-gold: #ffcb66;
      --text-light: #f5f9ff;
      --text-muted: #d0e2ff;
      --bg-deep: #00102a;
      --card-bg: rgba(11, 39, 93, 0.55);
      --card-border: rgba(140, 197, 255, 0.28);
      --nav-bg: rgba(4, 23, 63, 0.85);
      --shadow-soft: 0 22px 45px rgba(2, 15, 51, 0.38);
      --shadow-lift: 0 28px 60px rgba(10, 43, 122, 0.42);
      --transition: 0.3s ease;
      --max-width: 1100px;
    }

    *, *::before, *::after {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: 'Inter', 'Helvetica Neue', Arial, sans-serif;
      color: var(--text-light);
      background-color: var(--bg-deep);
      background-image:
        radial-gradient(circle at 10% 15%, rgba(86, 140, 255, 0.6) 0%, transparent 55%),
        radial-gradient(circle at 80% 0%, rgba(0, 193, 255, 0.38) 0%, transparent 60%),
        linear-gradient(140deg, #02123a 0%, #052f7d 55%, #0a4bac 100%);
      background-attachment: fixed;
      scroll-behavior: smooth;
    }

    ::selection {
      background: rgba(100, 181, 246, 0.38);
      color: #fff;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    a:hover,
    a:focus-visible {
      color: var(--accent-cyan);
    }

    img {
      display: block;
      max-width: 100%;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 20;
      background: var(--nav-bg);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(140, 197, 255, 0.12);
    }

    .nav {
      width: min(92%, var(--max-width));
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1.5rem;
      padding: 0.85rem 0;
    }

    .nav__brand {
      font-weight: 700;
      font-size: clamp(1.05rem, 1.8vw, 1.3rem);
      letter-spacing: 0.06em;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
    }

    .nav__links {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.25rem;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    .nav__links a {
      padding: 0.55rem 0.9rem;
      border-radius: 999px;
      transition: background-color var(--transition), color var(--transition);
    }

    .nav__links a:hover,
    .nav__links a:focus-visible {
      background-color: rgba(255, 255, 255, 0.16);
      color: #fff;
    }

    .nav__toggle {
      display: none;
      border: 1px solid rgba(140, 197, 255, 0.45);
      background: rgba(21, 61, 146, 0.35);
      color: var(--text-light);
      padding: 0.45rem 0.75rem;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color var(--transition), border-color var(--transition);
    }

    .nav__toggle:hover,
    .nav__toggle:focus-visible {
      background: rgba(33, 94, 198, 0.45);
      border-color: rgba(140, 197, 255, 0.75);
    }

    main {
      display: block;
    }

    .section {
      padding: clamp(3.5rem, 5vw, 5.5rem) 0;
    }

    .container {
      width: min(92%, var(--max-width));
      margin: 0 auto;
    }

    .hero {
      display: grid;
      align-items: center;
      gap: clamp(1.75rem, 5vw, 4rem);
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    }

    .hero__eyebrow {
      text-transform: uppercase;
      font-size: 0.85rem;
      letter-spacing: 0.4em;
      color: rgba(237, 245, 255, 0.65);
      margin-bottom: 1.1rem;
      display: inline-block;
    }

    .hero__text h1 {
      font-size: clamp(2.25rem, 5vw, 3.35rem);
      line-height: 1.15;
      margin: 0 0 1.1rem;
      text-shadow: 0 12px 40px rgba(0, 0, 0, 0.45);
    }

    .hero__text p {
      margin: 0 0 1.8rem;
      line-height: 1.75;
      color: var(--text-muted);
      max-width: 38rem;
    }

    .hero__cta {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      padding: 0.95rem 1.8rem;
      border-radius: 999px;
      background: linear-gradient(135deg, #6bdcff 0%, #4aa8ff 100%);
      color: #01203f;
      font-weight: 600;
      box-shadow: var(--shadow-lift);
      transition: transform var(--transition), box-shadow var(--transition);
    }

    .hero__cta:hover,
    .hero__cta:focus-visible {
      transform: translateY(-4px);
      box-shadow: 0 32px 60px rgba(18, 74, 158, 0.45);
      color: #001a32;
    }

    .hero__image {
      position: relative;
      display: grid;
      place-items: center;
    }

    .portrait-frame {
      position: relative;
      isolation: isolate;
      padding: clamp(0.55rem, 2vw, 0.9rem);
      border-radius: 26px;
      background: linear-gradient(145deg, rgba(100, 181, 246, 0.45) 0%, rgba(8, 34, 96, 0.85) 100%);
      box-shadow: var(--shadow-lift);
      overflow: hidden;
    }

    .portrait-frame::before {
      content: "";
      position: absolute;
      inset: 14%;
      border-radius: 20px;
      background: rgba(106, 190, 255, 0.18);
      filter: blur(34px);
      z-index: -2;
    }

    .hero__portrait {
      width: min(310px, 82vw);
      aspect-ratio: 3 / 4;
      border-radius: 20px;
      border: 2px solid rgba(245, 249, 255, 0.35);
      box-shadow: 0 22px 44px rgba(2, 18, 62, 0.55);
      object-fit: cover;
      object-position: center;
      background:
        radial-gradient(circle at 28% 22%, rgba(255, 255, 255, 0.26) 0%, transparent 54%),
        linear-gradient(135deg, rgba(9, 35, 96, 0.9), rgba(4, 21, 61, 0.92));
      filter: saturate(1.05) contrast(1.05);
      transition: transform var(--transition), filter var(--transition);
    }

    .portrait-frame:hover .hero__portrait,
    .portrait-frame:focus-within .hero__portrait {
      transform: translateY(-6px);
      filter: saturate(1.12) contrast(1.08);
    }

    .card {
      background: var(--card-bg);
      border: 1px solid var(--card-border);
      border-radius: 24px;
      padding: clamp(1.8rem, 3vw, 2.25rem);
      backdrop-filter: blur(18px);
      box-shadow: var(--shadow-soft);
    }

    .grid {
      display: grid;
      gap: clamp(1.5rem, 3vw, 2.5rem);
    }

    .grid--two {
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    }

    h2 {
      font-size: clamp(1.7rem, 3vw, 2.25rem);
      margin: 0 0 1.6rem;
    }

    h3 {
      margin: 0 0 1rem;
      font-size: clamp(1.1rem, 2vw, 1.35rem);
    }

    p {
      margin: 0 0 1rem;
      line-height: 1.7;
    }

    ul {
      margin: 0;
      padding-left: 1.4rem;
    }

    ul li {
      margin-bottom: 0.65rem;
      line-height: 1.65;
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 0.35rem;
      padding: 0.45rem 0.85rem;
      margin: 0 0.55rem 0.6rem 0;
      border-radius: 999px;
      background: rgba(180, 213, 255, 0.14);
      color: rgba(237, 245, 255, 0.92);
      font-size: 0.88rem;
      font-weight: 500;
      letter-spacing: 0.01em;
    }

    .experience__item + .experience__item {
      margin-top: 1.75rem;
      padding-top: 1.75rem;
      border-top: 1px solid rgba(160, 205, 255, 0.18);
    }

    .experience__role {
      font-weight: 600;
      font-size: 1.05rem;
    }

    .experience__meta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin: 0.6rem 0 1rem;
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    .course-overview {
      display: grid;
      gap: clamp(2rem, 4.5vw, 3rem);
    }

    .lesson {
      background: rgba(5, 28, 96, 0.62);
      border: 1px solid rgba(112, 181, 254, 0.28);
      border-radius: 18px;
      padding: 1.35rem;
      display: grid;
      gap: 0.95rem;
      transition: transform var(--transition), box-shadow var(--transition), border-color var(--transition);
    }

    .lesson:hover,
    .lesson:focus-within {
      transform: translateY(-4px);
      box-shadow: 0 26px 45px rgba(5, 55, 135, 0.42);
      border-color: rgba(171, 219, 255, 0.45);
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
      line-height: 1.35;
    }

    .lesson__status {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      font-size: 0.92rem;
      color: var(--accent-cyan);
      font-weight: 600;
    }

    .lesson-checkbox {
      width: 1.05rem;
      height: 1.05rem;
      accent-color: var(--accent-cyan);
    }

    .progress-bar {
      position: relative;
      width: 100%;
      height: 10px;
      border-radius: 999px;
      overflow: hidden;
      background: rgba(255, 255, 255, 0.16);
    }

    .progress-bar span {
      position: absolute;
      inset: 0;
      width: 0%;
      border-radius: inherit;
      background: linear-gradient(90deg, #6bdcff 0%, #c0e7ff 100%);
      transition: width 0.45s ease-in-out;
    }

    .course-footer {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      justify-content: space-between;
      background: rgba(9, 46, 110, 0.7);
      border: 1px solid rgba(134, 197, 255, 0.24);
      border-radius: 18px;
      padding: 1.5rem;
      color: var(--text-muted);
    }

    .contact-card {
      display: grid;
      gap: 1.2rem;
    }

    .contact-list {
      list-style: none;
      margin: 0;
      padding: 0;
      display: grid;
      gap: 0.9rem;
    }

    .contact-list li {
      display: flex;
      flex-wrap: wrap;
      gap: 0.65rem;
      align-items: center;
      padding: 0.95rem 1.1rem;
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.14);
      color: rgba(237, 245, 255, 0.9);
    }

    .contact-list span {
      font-weight: 600;
      color: #ffffff;
    }

    footer {
      padding: 2.5rem 0 3rem;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.92rem;
    }

    footer a {
      color: var(--accent-cyan);
    }

    @media (max-width: 760px) {
      .nav__toggle {
        display: inline-flex;
      }

      .nav__links {
        position: absolute;
        right: 4%;
        top: calc(100% + 0.75rem);
        flex-direction: column;
        align-items: flex-start;
        width: min(280px, 92vw);
        padding: 1.2rem;
        background: rgba(5, 24, 70, 0.94);
        border-radius: 18px;
        border: 1px solid rgba(150, 205, 255, 0.18);
        box-shadow: 0 24px 48px rgba(3, 11, 34, 0.65);
        opacity: 0;
        visibility: hidden;
        transform: translateY(-10px);
        transition: opacity var(--transition), transform var(--transition), visibility var(--transition);
      }

      .nav__links.is-open {
        opacity: 1;
        visibility: visible;
        transform: translateY(0);
      }

      .nav__links a {
        width: 100%;
      }
    }

    @media (max-width: 580px) {
      .hero__cta {
        width: 100%;
        justify-content: center;
      }

      .experience__meta {
        flex-direction: column;
        align-items: flex-start;
      }

      .course-footer {
        flex-direction: column;
        align-items: flex-start;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="nav__brand">Ftalew Dagnaw · MPH · M&E Specialist</div>
      <button class="nav__toggle" aria-expanded="false" aria-controls="primary-navigation" aria-label="Toggle primary navigation">
        Menu
      </button>
      <ul class="nav__links" id="primary-navigation">
        <li><a href="#profile">Profile</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#course">AI Bootcamp</a></li>
        <li><a href="#contact">Organization Contact</a></li>
      </ul>
    </div>
  </header>

  <main>
    <section class="section">
      <div class="container hero">
        <div class="hero__text">
          <span class="hero__eyebrow">Health Systems · Insights · Equity</span>
          <h1>Transforming Health Systems with Data-Driven Insight</h1>
          <p>
            I am Ftalew Dagnaw Gebreyesus, a Senior Monitoring &amp; Evaluation Advisor at Ethiopia’s Ministry of Health. With over 15 years of experience leading national health information systems, program evaluations, and quality improvement initiatives, I align data ecosystems with strategic priorities to elevate public health outcomes.
          </p>
          <a class="hero__cta" href="#course">
            Explore My AI Bootcamp Progress
          </a>
        </div>

        <div class="hero__image">
          <div class="portrait-frame">
            <img
              class="hero__portrait"
              src="assets/ftalew-portrait.jpg"
              alt="Portrait of Ftalew Dagnaw Gebreyesus"
              loading="lazy"
              onerror="this.onerror=null;this.src='data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI2NDAiIGhlaWdodD0iNzIwIiB2aWV3Qm94PSIwIDAgNjQwIDcyMCI+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJncmFkIiB4MT0iMCUiIHkxPSIwJSIgeDI9IjEwMCUiIHkyPSIxMDAlIj48c3RvcCBvZmZzZXQ9IjAlIiBzdG9wLWNvbG9yPSIjMmE2ZGY0Ii8+PHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjMDIxYjc5Ii8+PC9saW5lYXJHcmFkaWVudD48L2RlZnM+PHJlY3Qgd2lkdGg9IjY0MCIgaGVpZ2h0PSI3MjAiIGZpbGw9InVybCgjZ3JhZCkiIHJ4PSI0OCIvPjx0ZXh0IHg9IjUwJSIgeT0iNTUlIiBmb250LXNpemU9IjIyMCIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZmlsbD0iI2UyZWRmZiIgZm9udC1mYW1pbHk9IkludGVyLCBIZWx2ZXRpY2EsIEFyaWFsIiBmb250LXdlaWdodD0iNzAwIj5GRCZuYnNwOzwvdGV4dD48L3N2Zz4=';"
            />
          </div>
        </div>
      </div>
    </section>

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

    <section class="section" id="course">
      <div class="container card">
        <h2>Generative AI for Work &amp; Research Productivity Bootcamp · 2025 Q4</h2>
        <p>
          Hands-on 8-week program from <strong>The GRAPH Courses</strong> focused on leveraging AI for productivity, literature reviews, data analysis, chatbot design, workflow automation, and creative media—without requiring coding expertise.
        </p>

        <div class="course-overview">
          <div class="course-summary grid grid--two">
            <div class="lesson" role="group" aria-labelledby="program-snapshot">
              <div class="lesson__header">
                <h4 id="program-snapshot">Program Snapshot</h4>
              </div>
              <ul>
                <li>Duration: 8 weeks · Live &amp; applied learning</li>
                <li>Includes: 7 Lessons · 1 Topic · 1 Quiz</li>
                <li>Status: Enrollment confirmed (Course currently closed to new participants)</li>
              </ul>
            </div>

            <div class="lesson" role="group" aria-labelledby="key-outcomes">
              <div class="lesson__header">
                <h4 id="key-outcomes">Key Outcomes</h4>
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
            <div class="lesson" role="group" aria-labelledby="progress-tracker">
              <div class="lesson__header">
                <h4 id="progress-tracker">Lesson Progress Tracker</h4>
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
                  <h4>Workshop 2 · Automated Data Analysis</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Analyzed Gapminder data to explore relationships between two global indicators using AI tools.
                  <br />
                  <a href="https://github.com/ftalew211/fitih.github.io/commit/624d5b476f144f9017ac8dfa98db054778a35fc1#diff-e67cc0f5f787f4d567c186394afbf337af2b40b050f71326780e2bc668b09664" target="_blank" rel="noopener" style="color: var(--accent-cyan); font-weight: 600;">
                    View Report
                  </a>
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
                <p style="color: var(--text-muted); margin: 0%;">
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
                <p style="color: var(--text-muted); margin: 0%;">
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
              <strong>Course Access:</strong> Login required (
              <a href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank" rel="noopener">Visit course page</a>
              )
            </div>
            <div>
              Cohort: Q4 2025 · Provider: The GRAPH Network
            </div>
          </div>
        </div>
      </div>
    </section>

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
  </main>

  <footer>
    © 2025 Ftalew Dagnaw Gebreyesus · Elevating public health through data, equity, and innovation.
  </footer>

  <script>
    const navToggle = document.querySelector('.nav__toggle');
    const navLinks = document.querySelector('.nav__links');
    const navAnchors = navLinks.querySelectorAll('a');

    navToggle?.addEventListener('click', () => {
      const isOpen = navLinks.classList.toggle('is-open');
      navToggle.setAttribute('aria-expanded', String(isOpen));
    });

    navAnchors.forEach((anchor) => {
      anchor.addEventListener('click', () => {
        if (navLinks.classList.contains('is-open')) {
          navLinks.classList.remove('is-open');
          navToggle.setAttribute('aria-expanded', 'false');
        }
      });
    });

    document.addEventListener('click', (event) => {
      if (!navLinks.contains(event.target) && !navToggle.contains(event.target)) {
        navLinks.classList.remove('is-open');
        navToggle.setAttribute('aria-expanded', 'false');
      }
    });

    const checkboxes = document.querySelectorAll('.lesson-checkbox');
    const overallProgress = document.getElementById('overall-progress');
    const overallPercentage = document.getElementById('overall-percentage');

    function updateProgress() {
      const total = checkboxes.length;
      const completed = Array.from(checkboxes).filter((box) => box.checked).length;
      const percent = total > 0 ? Math.round((completed / total) * 100) : 0;

      overallProgress.style.width = `${percent}%`;
      overallPercentage.textContent = percent;
    }

    checkboxes.forEach((box) => {
      box.addEventListener('change', updateProgress);
    });

    updateProgress();
  </script>
</body>
</html>
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
