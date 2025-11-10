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
      line-height: 1.6;
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
      text-decoration: underline;
    }

    img {
      display: block;
      max-width: 100%;
      height: auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 20;
      background: var(--nav-bg);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(140, 197, 255, 0.12);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
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
      color: var(--accent-cyan);
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
      transition: background-color var(--transition), color var(--transition), transform var(--transition);
      font-weight: 500;
    }

    .nav__links a:hover,
    .nav__links a:focus-visible {
      background-color: rgba(255, 255, 255, 0.16);
      color: #fff;
      transform: translateY(-2px);
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
      background: linear-gradient(135deg, var(--accent-cyan) 0%, #ffffff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
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
      position: relative;
      overflow: hidden;
    }

    .hero__cta::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      transition: left var(--transition);
    }

    .hero__cta:hover::before,
    .hero__cta:focus-visible::before {
      left: 100%;
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
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
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
      transition: transform var(--transition), box-shadow var(--transition);
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-lift);
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
      color: var(--accent-cyan);
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
      transition: background-color var(--transition);
    }

    .tag:hover {
      background: rgba(180, 213, 255, 0.25);
    }

    .experience__item + .experience__item {
      margin-top: 1.75rem;
      padding-top: 1.75rem;
      border-top: 1px solid rgba(160, 205, 255, 0.18);
    }

    .experience__role {
      font-weight: 600;
      font-size: 1.05rem;
      color: var(--accent-gold);
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
      color: var(--accent-cyan);
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
      box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.2);
    }

    .progress-bar span {
      position: absolute;
      inset: 0;
      width: 0%;
      border-radius: inherit;
      background: linear-gradient(90deg, #6bdcff 0%, #c0e7ff 100%);
      transition: width 0.45s ease-in-out;
      box-shadow: 0 0 10px rgba(107, 220, 255, 0.5);
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
      backdrop-filter: blur(10px);
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
      transition: background-color var(--transition);
    }

    .contact-list li:hover {
      background: rgba(255, 255, 255, 0.2);
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
      background: rgba(0, 0, 0, 0.2);
      backdrop-filter: blur(10px);
    }

    footer a {
      color: var(--accent-cyan);
      font-weight: 600;
    }

    .project-card {
      background: rgba(5, 28, 96, 0.62);
      border: 1px solid rgba(112, 181, 254, 0.28);
      border-radius: 18px;
      padding: 1.35rem;
      display: grid;
      gap: 0.95rem;
      transition: transform var(--transition), box-shadow var(--transition), border-color var(--transition);
    }

    .project-card:hover,
    .project-card:focus-within {
      transform: translateY(-4px);
      box-shadow: 0 26px 45px rgba(5, 55, 135, 0.42);
      border-color: rgba(171, 219, 255, 0.45);
    }

    .project-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 1.5rem;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .project-content {
      display: grid;
      grid-template-columns: 200px 1fr;
      gap: 2rem;
      margin-bottom: 1.5rem;
    }

    .project-image {
      display: flex;
      justify-content: center;
    }

    .project-portrait {
      width: 180px;
      height: 240px;
      object-fit: cover;
      border-radius: 16px;
      border: 2px solid var(--card-border);
      box-shadow: var(--shadow-soft);
    }

    .project-description h4 {
      margin-top: 1.5rem;
      margin-bottom: 0.8rem;
      color: var(--accent-gold);
    }

    .project-cta {
      margin-top: 1.5rem;
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .project-footer {
      display: flex;
      justify-content: space-between;
      color: var(--text-muted);
      font-size: 0.9rem;
      padding-top: 1rem;
      border-top: 1px solid var(--card-border);
    }

    .report-container {
      width: 100%;
      margin-top: 1.5rem;
      border-radius: 12px;
      overflow: hidden;
      background: rgba(0, 0, 0, 0.2);
      border: 1px solid var(--card-border);
    }

    .report-tabs {
      display: flex;
      background: rgba(0, 0, 0, 0.3);
      border-bottom: 1px solid var(--card-border);
    }

    .report-tab {
      flex: 1;
      padding: 0.8rem 1rem;
      background: none;
      border: none;
      color: var(--text-muted);
      cursor: pointer;
      transition: all var(--transition);
      font-weight: 500;
      font-size: 0.9rem;
    }

    .report-tab.active {
      background: rgba(107, 220, 255, 0.1);
      color: var(--accent-cyan);
      border-bottom: 2px solid var(--accent-cyan);
    }

    .report-tab:hover {
      background: rgba(107, 220, 255, 0.05);
    }

    .report-content {
      padding: 1.5rem;
      min-height: 400px;
      max-height: 600px;
      overflow-y: auto;
    }

    .report-text {
      line-height: 1.8;
      color: var(--text-light);
    }

    .report-text h3 {
      color: var(--accent-gold);
      margin-top: 1.5rem;
      margin-bottom: 0.8rem;
    }

    .report-text p {
      margin-bottom: 1rem;
    }

    .report-text ul {
      margin: 1rem 0;
    }

    .report-text li {
      margin-bottom: 0.5rem;
    }

    .access-badge {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.4rem 0.8rem;
      border-radius: 20px;
      background: rgba(76, 175, 80, 0.2);
      color: #4caf50;
      font-size: 0.85rem;
      font-weight: 500;
      margin-left: 0.5rem;
    }

    .pdf-button {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.75rem 1.5rem;
      border-radius: 8px;
      font-weight: 500;
      transition: all var(--transition);
      cursor: pointer;
      border: none;
      font-size: 0.9rem;
      text-decoration: none;
    }

    .pdf-button-primary {
      background: linear-gradient(135deg, #6bdcff 0%, #4aa8ff 100%);
      color: #01203f;
    }

    .pdf-button-secondary {
      background: rgba(255, 255, 255, 0.1);
      color: var(--text-light);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    .pdf-button:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }

    .error-message {
      background: rgba(244, 67, 54, 0.1);
      border: 1px solid rgba(244, 67, 54, 0.3);
      border-radius: 8px;
      padding: 1rem;
      color: #ff9800;
      margin-top: 1rem;
      font-size: 0.9rem;
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

      .project-content {
        grid-template-columns: 1fr;
        text-align: center;
      }
      
      .project-portrait {
        margin: 0 auto;
      }
      
      .project-footer {
        flex-direction: column;
        gap: 0.5rem;
        text-align: center;
      }

      .report-content {
        min-height: 300px;
        max-height: 400px;
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

      .hero {
        text-align: center;
      }

      .hero__text h1 {
        font-size: clamp(1.8rem, 6vw, 2.5rem);
      }

      .report-tabs {
        flex-direction: column;
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
        <li><a href="#contact">Contact</a></li>
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
            I am Ftalew Dagnaw Gebreyesus, a Senior Monitoring & Evaluation Advisor at Ethiopia's Ministry of Health. With over 15 years of experience leading national health information systems, program evaluations, and quality improvement initiatives, I align data ecosystems with strategic priorities to elevate public health outcomes.
          </p>
          <a class="hero__cta" href="#course">
            Explore My AI Bootcamp Progress
            <svg width="16" height="16" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
            </svg>
          </a>
        </div>

        <div class="hero__image">
          <div class="portrait-frame">
            <img
              class="hero__portrait"
              src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzEwIiBoZWlnaHQ9IjQxMyIgdmlld0JveD0iMCAwIDMxMCA0MTMiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIzMTAiIGhlaWdodD0iNDEzIiByeD0iMjAiIGZpbGw9IiMwQzJENjQiLz4KPHRleHQgeD0iMTU1IiB5PSIyMDYiIGZvbnQtZmFtaWx5PSJBcmlhbCwgc2Fucy1zZXJpZiIgZm9udC1zaXplPSIxOCIgZmlsbD0id2hpdGUiIHRleHQtYW5jaG9yPSJtaWRkbGUiPkZ0YWxldyBEYWduYXc8L3RleHQ+Cjx0ZXh0IHg9IjE1NSIgeT0iMjMwIiBmb250LWZhbWlseT0iQXJpYWwsIHNhbnMtc2VyaWYiIGZvbnQtc2l6ZT0iMTQiIGZpbGw9IndoaXRlIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5NUEggJiBNJkUgU3BlY2lhbGlzdDwvdGV4dD4KPC9zdmc+"
              alt="Portrait of Ftalew Dagnaw Gebreyesus"
              loading="lazy"
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
            Results-driven Monitoring & Evaluation professional with a Master of Public Health and a B.Sc. in Statistics. I specialize in designing, implementing, and optimizing M&E frameworks across national health programs, leveraging platforms like DHIS2 and Power BI to strengthen data quality, equity, and decision-making.
          </p>
          <div>
            <span class="tag">Monitoring & Evaluation Frameworks</span>
            <span class="tag">Health Information Systems</span>
            <span class="tag">Data Analytics & Visualization</span>
            <span class="tag">Strategic Planning</span>
            <span class="tag">Stakeholder Engagement</span>
          </div>
        </article>

        <article class="card">
          <h2>Core Competencies</h2>
          <ul>
            <li>Architecting national M&E systems, dashboards, and reporting pipelines.</li>
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
          <div class="experience__role">Senior Monitoring & Evaluation Advisor · Ministry of Health, Ethiopia</div>
          <div class="experience__meta">
            <span>July 2019 – Present</span>
            <span>Addis Ababa, Ethiopia</span>
          </div>
          <ul>
            <li>Lead design and execution of M&E plans for national healthcare quality, innovation, and equity initiatives.</li>
            <li>Modernized national HMIS indicators, reporting forms, and DHIS2 implementations to match sector priorities.</li>
            <li>Advanced integration of ICD-11, effective coverage metrics, and responsive dashboards to improve data use.</li>
            <li>Guided sub-national mentorship, learning forums, and publications to scale quality improvement practices.</li>
          </ul>
        </div>

        <div class="experience__item">
          <div class="experience__role">Data Manager & Analyst · World Health Organization Ethiopia</div>
          <div class="experience__meta">
            <span>Sept 2014 – July 2019</span>
            <span>Addis Ababa, Ethiopia</span>
          </div>
          <ul>
            <li>Co-developed the national Maternal & Perinatal Death Surveillance & Response (MPDSR) framework and database.</li>
            <li>Integrated MPDSR with Public Health Emergency Management systems, ensuring actionable intelligence flow.</li>
            <li>Built national capacity through trainings, supportive supervision, and knowledge dissemination.</li>
          </ul>
        </div>

        <div class="experience__item">
          <div class="experience__role">Monitoring & Evaluation Roles · CHAI, USAID Programs, Save the Children, I-TECH</div>
          <div class="experience__meta">
            <span>2006 – 2014</span>
            <span>Ethiopia</span>
          </div>
          <ul>
            <li>Strengthened vaccine program M&E systems, led PMP compliance, and coordinated project evaluations.</li>
            <li>Executed routine data quality assessments, surveys, and evidence-based reporting for USAID-funded programs.</li>
            <li>Managed HIV/AIDS data ecosystems, training, and performance analytics across regional facilities.</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section" id="course">
      <div class="container card">
        <h2>Generative AI for Work & Research Productivity Bootcamp · 2025 Q4</h2>
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
                <li>Duration: 8 weeks · Live & applied learning</li>
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
                  <h4>02 · AI-Assisted Documents & Presentations</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Building professional websites, reports, and decks rapidly with co-creative AI tools.
                </p>
                <div class="project-card" style="margin-top: 1rem;">
                  <div class="project-header">
                    <h4 style="color: var(--accent-gold); margin: 0;">GDP per Capita & Life Expectancy Analysis</h4>
                    <div style="display: flex; gap: 0.5rem; align-items: center;">
                      <span class="tag">Data Analysis</span>
                      <span class="tag">Public Health</span>
                      <span class="access-badge">
                        <svg width="12" height="12" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                        </svg>
                        Public Access
                      </span>
                    </div>
                  </div>
                  
                  <div class="project-content">
                    <div class="project-image">
                      <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTgwIiBoZWlnaHQ9IjI0MCIgdmlld0JveD0iMCAwIDE4MCAyNDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIxODAiIGhlaWdodD0iMjQwIiByeD0iMTYiIGZpbGw9IiMwQzJENjQiLz4KPHRleHQgeD0iOTAiIHk9IjEyMCIgZm9udC1mYW1pbHk9IkFyaWFsLCBzYW5zLXNlcmlmIiBmb250LXNpemU9IjE0IiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+RnRhbGV3IERhZ25hdzwvdGV4dD4KPHRleHQgeD0iOTAiIHk9IjE0MCIgZm9udC1mYW1pbHk9IkFyaWFsLCBzYW5zLXNlcmlmIiBmb250LXNpemU9IjEyIiBmaWxsPSJ3aGl0ZSIgdGV4dC1hbmNob3I9Im1pZGRsZSI+TVBIIE0mRSBTcGVjaWFsaXN0PC90ZXh0Pgo8L3N2Zz4=" alt="Ftalew Dagnaw" class="project-portrait">
                    </div>
                    
                    <div class="project-description">
                      <p>This analysis explores the relationship between GDP per capita and life expectancy using Gapminder's data repository, examining how economic prosperity correlates with population health outcomes across countries in 2020.</p>
                      
                      <h4>Key Findings:</h4>
                      <ul>
                        <li>Strong positive relationship between GDP per capita and life expectancy</li>
                        <li>Logarithmic relationship strongest at lower GDP levels</li>
                        <li>Diminishing returns at higher GDP levels (above ~$20,000)</li>
                        <li>Life expectancy ranges from approximately 55 to 85 years globally</li>
                      </ul>
                      
                      <div class="report-container">
                        <div class="report-tabs">
                          <button class="report-tab active" data-tab="gdp-summary">Executive Summary</button>
                          <button class="report-tab" data-tab="gdp-methods">Methods</button>
                          <button class="report-tab" data-tab="gdp-findings">Key Findings</button>
                          <button class="report-tab" data-tab="gdp-reflection">Reflection</button>
                        </div>
                        <div class="report-content">
                          <div id="gdp-summary" class="report-text">
                            <h3>Executive Summary</h3>
                            <p>This analysis examines the relationship between GDP per capita and life expectancy across 193 countries using 2020 data from Gapminder. The study reveals a strong positive correlation between economic prosperity and population health outcomes, with particularly pronounced effects at lower income levels.</p>
                            <p>The logarithmic relationship demonstrates that small increases in GDP per capita at lower income levels yield substantial improvements in life expectancy, while the benefits diminish at higher income levels, suggesting a plateau effect. This pattern underscores the critical importance of economic development for basic health improvements while highlighting the need for targeted health interventions even in wealthier nations.</p>
                          </div>
                          <div id="gdp-methods" class="report-text" style="display: none;">
                            <h3>Methodology</h3>
                            <p>Data was sourced from Gapminder's open data repository, which provides country-level statistics on GDP per capita and life expectancy. The year 2020 was selected to reflect the most recent available global data. The analysis involved:</p>
                            <ul>
                              <li>Data retrieval and preparation: GDP per capita (in USD) and life expectancy data for 2020 were extracted</li>
                              <li>Exploratory data analysis: A scatter plot was created to visualize the relationship between GDP per capita and life expectancy, using a logarithmic scale for GDP to better capture variation at lower income levels</li>
                              <li>Visualization of spatial distribution: A world map was produced to illustrate life expectancy and GDP per capita across countries</li>
                              <li>Statistical assistance: The AI platform Julius AI was used to support data analysis and visualization, including generation of scatter plots and model fitting</li>
                            </ul>
                          </div>
                          <div id="gdp-findings" class="report-text" style="display: none;">
                            <h3>Detailed Findings</h3>
                            <p>The scatterplot reveals a strong positive relationship between GDP per capita and life expectancy in 2020. Key observations:</p>
                            <ul>
                              <li>Logarithmic relationship: The relationship is strongest at lower GDP levels, where small increases in GDP per capita are associated with substantial gains in life expectancy</li>
                              <li>Diminishing returns: At higher GDP levels (above ~$20,000), additional wealth produces smaller improvements in life expectancy, suggesting a plateau effect</li>
                              <li>Strong correlation: Countries with higher economic output consistently show higher life expectancy, indicating that economic development is closely tied to health outcomes</li>
                              <li>Range: Life expectancy ranges from approximately 55 to 85 years, while GDP per capita spans from under $1,000 to over $100,000</li>
                            </ul>
                            <p>This pattern suggests that economic resources enable better healthcare, nutrition, sanitation, and living conditions that directly impact longevity, though the benefits level off once basic needs are met.</p>
                          </div>
                          <div id="gdp-reflection" class="report-text" style="display: none;">
                            <h3>Personal Reflection</h3>
                            <p>As a statistician and Public Health specialist with extensive experience of M&E, such use of Generative with no code data analysis has huge implications in maximizing the utilization of data in short time to facilitate the timely decision making in the Health sector. In our context, there are huge data set from multiple data sources that such platforms motivate me to apply it in my current role at Ministry of Health. Very helpful and feel encouraged.! I will also go further exercise to deepen my knowledge.</p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  
                  <div class="project-footer">
                    <span>Project from Lesson 02</span>
                    <span>Date: Oct 20, 2025</span>
                  </div>
                  
                  <div class="project-cta">
                    <button class="pdf-button pdf-button-primary" onclick="downloadPDF('GDP Analysis Report', 'relationship between GDP per capita and life expectancy_by_Ftalew_Dagnaw.pdf')">Download Report (PDF)</button>
                  </div>
                </div>
              </label>

              <label class="lesson">
                <div class="lesson__header">
                  <h4>03 · AI for Literature Review & Data Analysis</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Leveraging AI to synthesize research, clean data, and generate insights from datasets.
                </p>
                
                <div class="project-card" style="margin-top: 1.5rem; background: rgba(5, 28, 96, 0.85);">
                  <div class="project-header" style="margin-bottom: 0.5rem;">
                    <h4 style="color: var(--accent-gold); margin: 0;">Workshop 3: Job Market Analysis</h4>
                    <div style="display: flex; gap: 0.5rem; align-items: center;">
                      <span class="tag">Data Analysis</span>
                      <span class="tag">LLM APIs</span>
                      <span class="access-badge">
                        <svg width="12" height="12" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                        </svg>
                        Completed
                      </span>
                    </div>
                  </div>
                  <p style="color: var(--text-muted); margin: 0.5rem 0 1rem; line-height: 1.6;">
                    Analysis of 400 data analyst job postings to see how experience and programming language (R, Python) affect salary.
                  </p>
                  <div class="project-footer" style="padding-top: 0.5rem; margin-top: 0.5rem; border-color: rgba(140, 197, 255, 0.15);">
                    <span>Project from Lesson 03</span>
                    <span>Date: Oct 30, 2025</span>
                  </div>
                  <div class="project-cta" style="margin-top: 1rem; gap: 0.95rem;">
                    <button class="pdf-button pdf-button-primary" onclick="downloadPDF('Job Market Analysis Report', 'Job market analysis report.pdf')">
                      <svg width="16" height="16" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M3 17a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm3.293-7.707a1 1 0 011.414 0L9 10.586V3a1 1 0 112 0v7.586l1.293-1.293a1 1 0 111.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z" clip-rule="evenodd"></path>
                      </svg>
                      Download Week 3 Report (PDF)
                    </button>
                  </div>
                </div>
                                
              </label>

              <label class="lesson">
                <div class="lesson__header">
                  <h4>04 · Building Interactive Chatbots</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Designing and deploying custom AI chatbots (like this portfolio helper) without code.
                </p>
              </label>

              <label class="lesson">
                <div class="lesson__header">
                  <h4>05 · AI-Powered Workflow Automation</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Connecting AI with tools like Zapier or Make to automate M&E reporting and other tasks.
                </p>
              </label>

              <label class="lesson">
                <div class="lesson__header">
                  <h4>06 · Creative Media & Design with AI</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Generating images, logos, videos, and audio for reports, campaigns, and presentations.
                </p>
              </label>

              <label class="lesson">
                <div class="lesson__header">
                  <h4>07 · Capstone & Final Quiz</h4>
                  <input type="checkbox" class="lesson-checkbox" />
                </div>
                <p style="color: var(--text-muted); margin: 0;">
                  Integrating all learned skills into a final project and knowledge assessment.
                </p>
              </label>
            </div>
          </div>

          <div class="course-footer">
            <p style="margin: 0;"><strong>Enrolled:</strong> Ftalew Dagnaw Gebreyesus</p>
            <p style="margin: 0;"><strong>Course ID:</strong> GRPH-AI-Q42025</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="contact">
      <div class="container card contact-card">
        <h2>Get in Touch</h2>
        <p>
          I am passionate about leveraging data to solve complex public health challenges and am always open to discussing new ideas, collaborations, or opportunities. Please feel free to connect with me.
        </p>
        <ul class="contact-list">
          <li>
            <span>Email:</span>
            <a href="mailto:f.dagnaw.gebreyesus@gmail.com">f.dagnaw.gebreyesus@gmail.com</a>
          </li>
          <li>
            <span>LinkedIn:</span>
            <a href="https://www.linkedin.com/in/ftalew-dagnaw-gebreyesus-mph-b95b8535/" target="_blank" rel="noopener noreferrer">
              /in/ftalew-dagnaw-gebreyesus-mph
            </a>
          </li>
          <li>
            <span>Location:</span>
            Addis Ababa, Ethiopia
          </li>
        </ul>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <p>
        &copy; 2025 Ftalew Dagnaw Gebreyesus ·
        <a href="https://www.thegraph.courses" target="_blank" rel="noopener noreferrer">
          AI Bootcamp Portfolio Project
        </a>
      </p>
    </div>
  </footer>

  <script>
    // --- Navigation Toggle ---
    const navToggle = document.querySelector('.nav__toggle');
    const navLinks = document.querySelector('.nav__links');

    if (navToggle && navLinks) {
      navToggle.addEventListener('click', () => {
        const isExpanded = navToggle.getAttribute('aria-expanded') === 'true';
        navToggle.setAttribute('aria-expanded', !isExpanded);
        navLinks.classList.toggle('is-open');
      });
    }

    // --- Progress Tracker ---
    const checkboxes = document.querySelectorAll('.lesson-checkbox');
    const overallProgress = document.getElementById('overall-progress');
    const overallPercentage = document.getElementById('overall-percentage');
    const totalLessons = checkboxes.length;

    function updateProgress() {
      const completedLessons = document.querySelectorAll('.lesson-checkbox:checked').length;
      const percentage = totalLessons > 0 ? Math.round((completedLessons / totalLessons) * 100) : 0;
      
      if (overallProgress) {
        overallProgress.style.width = percentage + '%';
      }
      if (overallPercentage) {
        overallPercentage.textContent = percentage;
      }
    }

    checkboxes.forEach(checkbox => {
      checkbox.addEventListener('change', updateProgress);
    });

    // --- Tab Switching for Reports ---
    const reportTabs = document.querySelectorAll('.report-tab');
    
    reportTabs.forEach(tab => {
      tab.addEventListener('click', () => {
        const tabId = tab.getAttribute('data-tab');
        const container = tab.closest('.report-container');
        
        // Hide all content tabs
        const contentTabs = container.querySelectorAll('.report-text');
        contentTabs.forEach(content => {
          content.style.display = 'none';
        });
        
        // Remove active class from all tabs
        const allTabs = container.querySelectorAll('.report-tab');
        allTabs.forEach(t => {
          t.classList.remove('active');
        });
        
        // Show selected content and mark tab as active
        const selectedContent = container.querySelector(`#${tabId}`);
        if (selectedContent) {
          selectedContent.style.display = 'block';
          tab.classList.add('active');
        }
      });
    });

    // --- Close mobile nav on link click ---
    if (navLinks) {
      navLinks.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
          if (navLinks.classList.contains('is-open')) {
            navToggle.setAttribute('aria-expanded', 'false');
            navLinks.classList.remove('is-open');
          }
        });
      });
    }

    // --- Download PDF Function ---
    function downloadPDF(title, filename) {
      // In a real implementation, this would link to actual PDF files
      // For demonstration, we'll create a simple alert
      alert(`In a real implementation, this would download: ${filename}\n\nFor now, this is a placeholder function.`);
      
      // To implement actual download, you would need:
      // 1. Actual PDF files hosted on your server
      // 2. Replace this function with: window.location.href = '/path/to/' + filename;
    }

    // --- Initialize progress on load ---
    updateProgress();
  </script>
</body>
</html>
