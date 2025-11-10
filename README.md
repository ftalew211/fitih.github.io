import { useMemo, useState } from "react";
import portraitImage from "./assets/ftalew-picture.png";

const navLinks = [
  { label: "Profile", href: "#profile" },
  { label: "Experience", href: "#experience" },
  { label: "AI Bootcamp", href: "#course" },
  { label: "Contact", href: "#contact" },
];

type ReportTabKey = "gdp-summary" | "gdp-methods" | "gdp-findings" | "gdp-reflection";

const reportTabs: { key: ReportTabKey; label: string }[] = [
  { key: "gdp-summary", label: "Executive Summary" },
  { key: "gdp-methods", label: "Methods" },
  { key: "gdp-findings", label: "Key Findings" },
  { key: "gdp-reflection", label: "Reflection" },
];

const reportContent: Record<ReportTabKey, JSX.Element> = {
  "gdp-summary": (
    <div>
      <h3>Executive Summary</h3>
      <p>
        This analysis examines the relationship between GDP per capita and life expectancy across 193 countries using
        2020 data from Gapminder. The study reveals a strong positive correlation between economic prosperity and
        population health outcomes, with particularly pronounced effects at lower income levels.
      </p>
      <p>
        The logarithmic relationship demonstrates that small increases in GDP per capita at lower income levels yield
        substantial improvements in life expectancy, while the benefits diminish at higher income levels, suggesting a
        plateau effect. This pattern underscores the critical importance of economic development for basic health
        improvements while highlighting the need for targeted health interventions even in wealthier nations.
      </p>
    </div>
  ),
  "gdp-methods": (
    <div>
      <h3>Methodology</h3>
      <p>
        Data was sourced from Gapminder&apos;s open data repository, which provides country-level statistics on GDP per
        capita and life expectancy. The year 2020 was selected to reflect the most recent available global data. The
        analysis involved:
      </p>
      <ul>
        <li>Data retrieval and preparation: GDP per capita (in USD) and life expectancy data for 2020 were extracted</li>
        <li>
          Exploratory data analysis: A scatter plot was created to visualize the relationship between GDP per capita and
          life expectancy, using a logarithmic scale for GDP to better capture variation at lower income levels
        </li>
        <li>
          Visualization of spatial distribution: A world map was produced to illustrate life expectancy and GDP per
          capita across countries
        </li>
        <li>
          Statistical assistance: The AI platform Julius AI was used to support data analysis and visualization,
          including generation of scatter plots and model fitting
        </li>
      </ul>
    </div>
  ),
  "gdp-findings": (
    <div>
      <h3>Detailed Findings</h3>
      <p>The scatterplot reveals a strong positive relationship between GDP per capita and life expectancy in 2020.</p>
      <ul>
        <li>
          Logarithmic relationship: The relationship is strongest at lower GDP levels, where small increases in GDP per
          capita are associated with substantial gains in life expectancy
        </li>
        <li>
          Diminishing returns: At higher GDP levels (above ~$20,000), additional wealth produces smaller improvements in
          life expectancy, suggesting a plateau effect
        </li>
        <li>
          Strong correlation: Countries with higher economic output consistently show higher life expectancy, indicating
          that economic development is closely tied to health outcomes
        </li>
        <li>
          Range: Life expectancy ranges from approximately 55 to 85 years, while GDP per capita spans from under $1,000
          to over $100,000
        </li>
      </ul>
      <p>
        This pattern suggests that economic resources enable better healthcare, nutrition, sanitation, and living
        conditions that directly impact longevity, though the benefits level off once basic needs are met.
      </p>
    </div>
  ),
  "gdp-reflection": (
    <div>
      <h3>Personal Reflection</h3>
      <p>
        As a statistician and Public Health specialist with extensive experience of M&amp;E, such use of Generative with no
        code data analysis has huge implications in maximizing the utilization of data in short time to facilitate the
        timely decision making in the Health sector. In our context, there are huge data set from multiple data sources
        that such platforms motivate me to apply it in my current role at Ministry of Health. Very helpful and feel
        encouraged.! I will also go further exercise to deepen my knowledge.
      </p>
    </div>
  ),
};

const downloadLinks: Record<string, string> = {
  "relationship between GDP per capita and life expectancy_by_Ftalew_Dagnaw.pdf": "/relationship-between-gdp-life-expectancy.pdf",
  "Job market analysis report.pdf": "/job-market-analysis-report.pdf",
};

function App() {
  const [isNavOpen, setIsNavOpen] = useState(false);
  const [activeTab, setActiveTab] = useState<ReportTabKey>("gdp-summary");
  const [lessonProgress, setLessonProgress] = useState<boolean[]>(() => new Array(7).fill(false));

  const totalLessons = lessonProgress.length;
  const completedLessons = useMemo(
    () => lessonProgress.filter(Boolean).length,
    [lessonProgress]
  );
  const overallPercentage = totalLessons > 0 ? Math.round((completedLessons / totalLessons) * 100) : 0;

  const handleToggleNavigation = () => {
    setIsNavOpen((prev) => !prev);
  };

  const handleNavLinkClick = () => {
    setIsNavOpen(false);
  };

  const handleCheckboxToggle = (index: number) => {
    setLessonProgress((prev) => prev.map((value, idx) => (idx === index ? !value : value)));
  };

  const handleDownload = (title: string, filename: string) => {
    const link = document.createElement("a");
    link.href = downloadLinks[filename] ?? "#";
    link.download = filename;
    link.rel = "noopener noreferrer";
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
  };

  return (
    <div>
      <header>
        <div className="nav">
          <div className="nav__brand">Ftalew Dagnaw · MPH · M&amp;E Specialist</div>
          <button
            className="nav__toggle"
            aria-expanded={isNavOpen}
            aria-controls="primary-navigation"
            aria-label="Toggle primary navigation"
            type="button"
            onClick={handleToggleNavigation}
          >
            Menu
          </button>
          <ul className={`nav__links${isNavOpen ? " is-open" : ""}`} id="primary-navigation">
            {navLinks.map((link) => (
              <li key={link.href}>
                <a href={link.href} onClick={handleNavLinkClick}>
                  {link.label}
                </a>
              </li>
            ))}
          </ul>
        </div>
      </header>

      <main>
        <section className="section">
          <div className="container hero">
            <div className="hero__text">
              <span className="hero__eyebrow">Health Systems · Insights · Equity</span>
              <h1>Transforming Health Systems with Data-Driven Insight</h1>
              <p>
                I am Ftalew Dagnaw Gebreyesus, a Senior Monitoring &amp; Evaluation Advisor at Ethiopia&apos;s Ministry of
                Health. With over 15 years of experience leading national health information systems, program
                evaluations, and quality improvement initiatives, I align data ecosystems with strategic priorities to
                elevate public health outcomes.
              </p>
              <a className="hero__cta" href="#course">
                Explore My AI Bootcamp Progress
                <svg width="16" height="16" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                  <path
                    fillRule="evenodd"
                    d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                    clipRule="evenodd"
                  ></path>
                </svg>
              </a>
            </div>

            <div className="hero__image">
              <div className="portrait-frame">
                <img
                  className="hero__portrait"
                  src={portraitImage}
                  alt="Portrait of Ftalew Dagnaw Gebreyesus"
                  loading="lazy"
                />
              </div>
            </div>
          </div>
        </section>

        <section className="section" id="profile">
          <div className="container grid grid--two">
            <article className="card">
              <h2>Professional Snapshot</h2>
              <p>
                Results-driven Monitoring &amp; Evaluation professional with a Master of Public Health and a B.Sc. in
                Statistics. I specialize in designing, implementing, and optimizing M&amp;E frameworks across national health
                programs, leveraging platforms like DHIS2 and Power BI to strengthen data quality, equity, and
                decision-making.
              </p>
              <div>
                <span className="tag">Monitoring &amp; Evaluation Frameworks</span>
                <span className="tag">Health Information Systems</span>
                <span className="tag">Data Analytics &amp; Visualization</span>
                <span className="tag">Strategic Planning</span>
                <span className="tag">Stakeholder Engagement</span>
              </div>
            </article>

            <article className="card">
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

        <section className="section" id="experience">
          <div className="container card">
            <h2>Experience Highlights</h2>

            <div className="experience__item">
              <div className="experience__role">Senior Monitoring &amp; Evaluation Advisor · Ministry of Health, Ethiopia</div>
              <div className="experience__meta">
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

            <div className="experience__item">
              <div className="experience__role">Data Manager &amp; Analyst · World Health Organization Ethiopia</div>
              <div className="experience__meta">
                <span>Sept 2014 – July 2019</span>
                <span>Addis Ababa, Ethiopia</span>
              </div>
              <ul>
                <li>Co-developed the national Maternal &amp; Perinatal Death Surveillance &amp; Response (MPDSR) framework and database.</li>
                <li>Integrated MPDSR with Public Health Emergency Management systems, ensuring actionable intelligence flow.</li>
                <li>Built national capacity through trainings, supportive supervision, and knowledge dissemination.</li>
              </ul>
            </div>

            <div className="experience__item">
              <div className="experience__role">Monitoring &amp; Evaluation Roles · CHAI, USAID Programs, Save the Children, I-TECH</div>
              <div className="experience__meta">
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

        <section className="section" id="course">
          <div className="container card">
            <h2>Generative AI for Work &amp; Research Productivity Bootcamp · 2025 Q4</h2>
            <p>
              Hands-on 8-week program from <strong>The GRAPH Courses</strong> focused on leveraging AI for productivity,
              literature reviews, data analysis, chatbot design, workflow automation, and creative media—without requiring
              coding expertise.
            </p>

            <div className="course-overview">
              <div className="course-summary grid grid--two">
                <div className="lesson" role="group" aria-labelledby="program-snapshot">
                  <div className="lesson__header">
                    <h4 id="program-snapshot">Program Snapshot</h4>
                  </div>
                  <ul>
                    <li>Duration: 8 weeks · Live &amp; applied learning</li>
                    <li>Includes: 7 Lessons · 1 Topic · 1 Quiz</li>
                    <li>Status: Enrollment confirmed (Course currently closed to new participants)</li>
                  </ul>
                </div>

                <div className="lesson" role="group" aria-labelledby="key-outcomes">
                  <div className="lesson__header">
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

              <div className="course-progress">
                <div className="lesson" role="group" aria-labelledby="progress-tracker">
                  <div className="lesson__header">
                    <h4 id="progress-tracker">Lesson Progress Tracker</h4>
                    <div className="lesson__status" id="overall-status">
                      Overall Progress: <strong><span id="overall-percentage">{overallPercentage}</span>%</strong>
                    </div>
                  </div>
                  <div className="progress-bar" aria-hidden="true">
                    <span id="overall-progress" style={{ width: `${overallPercentage}%` }}></span>
                  </div>
                  <p style={{ color: "var(--text-muted)", margin: 0 }}>
                    Mark each lesson as you complete it to visualize advancement through the bootcamp modules.
                  </p>
                </div>

                <div className="grid grid--two" aria-live="polite">
                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>01 · Getting Started with AI Productivity Tools</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[0]}
                        onChange={() => handleCheckboxToggle(0)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Orientation to generative AI platforms, capabilities, and practical workflows for daily tasks.
                    </p>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>02 · AI-Assisted Documents &amp; Presentations</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[1]}
                        onChange={() => handleCheckboxToggle(1)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Building professional websites, reports, and decks rapidly with co-creative AI tools.
                    </p>
                    <div className="project-card" style={{ marginTop: "1rem" }}>
                      <div className="project-header">
                        <h4 style={{ color: "var(--accent-gold)", margin: 0 }}>GDP per Capita &amp; Life Expectancy Analysis</h4>
                        <div style={{ display: "flex", gap: "0.5rem", alignItems: "center" }}>
                          <span className="tag">Data Analysis</span>
                          <span className="tag">Public Health</span>
                          <span className="access-badge">
                            <svg width="12" height="12" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                              <path
                                fillRule="evenodd"
                                d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                                clipRule="evenodd"
                              ></path>
                            </svg>
                            Public Access
                          </span>
                        </div>
                      </div>

                      <div className="project-content">
                        <div className="project-image">
                          <img
                            src={portraitImage}
                            alt="Ftalew Dagnaw Gebreyesus"
                            className="project-portrait"
                          />
                        </div>

                        <div className="project-description">
                          <p>
                            This analysis explores the relationship between GDP per capita and life expectancy using
                            Gapminder&apos;s data repository, examining how economic prosperity correlates with population
                            health outcomes across countries in 2020.
                          </p>

                          <h4>Key Findings:</h4>
                          <ul>
                            <li>Strong positive relationship between GDP per capita and life expectancy</li>
                            <li>Logarithmic relationship strongest at lower GDP levels</li>
                            <li>Diminishing returns at higher GDP levels (above ~$20,000)</li>
                            <li>Life expectancy ranges from approximately 55 to 85 years globally</li>
                          </ul>

                          <div className="report-container">
                            <div className="report-tabs">
                              {reportTabs.map((tab) => (
                                <button
                                  key={tab.key}
                                  className={`report-tab${activeTab === tab.key ? " active" : ""}`}
                                  type="button"
                                  data-tab={tab.key}
                                  onClick={() => setActiveTab(tab.key)}
                                >
                                  {tab.label}
                                </button>
                              ))}
                            </div>
                            <div className="report-content">
                              <div className="report-text">{reportContent[activeTab]}</div>
                            </div>
                          </div>
                        </div>
                      </div>

                      <div className="project-footer">
                        <span>Project from Lesson 02</span>
                        <span>Date: Oct 20, 2025</span>
                      </div>

                      <div className="project-cta">
                        <button
                          className="pdf-button pdf-button-primary"
                          type="button"
                          onClick={() =>
                            handleDownload(
                              "GDP Analysis Report",
                              "relationship between GDP per capita and life expectancy_by_Ftalew_Dagnaw.pdf"
                            )
                          }
                        >
                          Download Report (PDF)
                        </button>
                      </div>
                    </div>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>03 · AI for Literature Review &amp; Data Analysis</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[2]}
                        onChange={() => handleCheckboxToggle(2)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Leveraging AI to synthesize research, clean data, and generate insights from datasets.
                    </p>

                    <div className="project-card" style={{ marginTop: "1.5rem", background: "rgba(5, 28, 96, 0.85)" }}>
                      <div className="project-header" style={{ marginBottom: "0.5rem" }}>
                        <h4 style={{ color: "var(--accent-gold)", margin: 0 }}>Workshop 3: Job Market Analysis</h4>
                        <div style={{ display: "flex", gap: "0.5rem", alignItems: "center" }}>
                          <span className="tag">Data Analysis</span>
                          <span className="tag">LLM APIs</span>
                          <span className="access-badge">
                            <svg width="12" height="12" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                              <path
                                fillRule="evenodd"
                                d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                                clipRule="evenodd"
                              ></path>
                            </svg>
                            Completed
                          </span>
                        </div>
                      </div>
                      <p style={{ color: "var(--text-muted)", margin: "0.5rem 0 1rem", lineHeight: 1.6 }}>
                        Analysis of 400 data analyst job postings to see how experience and programming language (R, Python)
                        affect salary.
                      </p>
                      <div className="project-footer" style={{ paddingTop: "0.5rem", marginTop: "0.5rem", borderColor: "rgba(140, 197, 255, 0.15)" }}>
                        <span>Project from Lesson 03</span>
                        <span>Date: Oct 30, 2025</span>
                      </div>
                      <div className="project-cta" style={{ marginTop: "1rem", gap: "0.95rem" }}>
                        <button
                          className="pdf-button pdf-button-primary"
                          type="button"
                          onClick={() => handleDownload("Job Market Analysis Report", "Job market analysis report.pdf")}
                        >
                          <svg width="16" height="16" fill="currentColor" viewBox="0 0 20 20" aria-hidden="true">
                            <path
                              fillRule="evenodd"
                              d="M3 17a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm3.293-7.707a1 1 0 011.414 0L9 10.586V3a1 1 0 112 0v7.586l1.293-1.293a1 1 0 111.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z"
                              clipRule="evenodd"
                            ></path>
                          </svg>
                          Download Week 3 Report (PDF)
                        </button>
                      </div>
                    </div>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>04 · Building Interactive Chatbots</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[3]}
                        onChange={() => handleCheckboxToggle(3)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Designing and deploying custom AI chatbots (like this portfolio helper) without code.
                    </p>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>05 · AI-Powered Workflow Automation</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[4]}
                        onChange={() => handleCheckboxToggle(4)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Connecting AI with tools like Zapier or Make to automate M&amp;E reporting and other tasks.
                    </p>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>06 · Creative Media &amp; Design with AI</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[5]}
                        onChange={() => handleCheckboxToggle(5)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Generating images, logos, videos, and audio for reports, campaigns, and presentations.
                    </p>
                  </label>

                  <label className="lesson">
                    <div className="lesson__header">
                      <h4>07 · Capstone &amp; Final Quiz</h4>
                      <input
                        type="checkbox"
                        className="lesson-checkbox"
                        checked={lessonProgress[6]}
                        onChange={() => handleCheckboxToggle(6)}
                      />
                    </div>
                    <p style={{ color: "var(--text-muted)", margin: 0 }}>
                      Integrating all learned skills into a final project and knowledge assessment.
                    </p>
                  </label>
                </div>
              </div>

              <div className="course-footer">
                <p style={{ margin: 0 }}>
                  <strong>Enrolled:</strong> Ftalew Dagnaw Gebreyesus
                </p>
                <p style={{ margin: 0 }}>
                  <strong>Course ID:</strong> GRPH-AI-Q42025
                </p>
              </div>
            </div>
          </div>
        </section>

        <section className="section" id="contact">
          <div className="container card contact-card">
            <h2>Get in Touch</h2>
            <p>
              I am passionate about leveraging data to solve complex public health challenges and am always open to
              discussing new ideas, collaborations, or opportunities. Please feel free to connect with me.
            </p>
            <ul className="contact-list">
              <li>
                <span>Email:</span>
                <a href="mailto:f.dagnaw.gebreyesus@gmail.com">f.dagnaw.gebreyesus@gmail.com</a>
              </li>
              <li>
                <span>LinkedIn:</span>
                <a
                  href="https://www.linkedin.com/in/ftalew-dagnaw-gebreyesus-mph-b95b8535/"
                  target="_blank"
                  rel="noopener noreferrer"
                >
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
        <div className="container">
          <p>
            &copy; 2025 Ftalew Dagnaw Gebreyesus ·
            <a href="https://www.thegraph.courses" target="_blank" rel="noopener noreferrer">
              AI Bootcamp Portfolio Project
            </a>
          </p>
        </div>
      </footer>
    </div>
  );
}

export default App;
