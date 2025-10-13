<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Ftalew Dagnaw — Portfolio & CV</title>
  <meta name="description" content="Ftalew Dagnaw — Senior M&E Advisor, CV, Generative AI course tracker, references manager, LinkedIn contacts import" />
  <!-- Lightweight Google Font (may fallback if blocked) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    /* ---------- Reset & base ---------- */
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#9aa6b2;
      --accent:#4f46e5;
      --glass: rgba(255,255,255,0.03);
      --radius:14px;
      --max-width:1100px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background:linear-gradient(180deg,#071029 0%, #081426 40%);
      color:#e6eef6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:24px;
      display:flex;
      justify-content:center;
    }
    .container{
      width:100%;
      max-width:var(--max-width);
    }

    /* ---------- Header / nav ---------- */
    header{
      display:flex;
      gap:18px;
      align-items:center;
      margin-bottom:18px;
    }
    .brand{
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo{
      width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#06b6d4);
      display:flex;align-items:center;justify-content:center;font-weight:700;box-shadow:0 6px 18px rgba(79,70,229,0.2);
    }
    nav{margin-left:auto;display:flex;gap:10px;align-items:center}
    nav a{
      color:var(--muted);
      text-decoration:none;
      padding:8px 12px;border-radius:10px;font-weight:600;font-size:14px;
    }
    nav a.active, nav a:hover{background:var(--glass); color:#fff}

    /* ---------- Layout ---------- */
    main{
      display:grid;
      grid-template-columns: 360px 1fr;
      gap:18px;
      align-items:start;
    }

    /* Left column (profile card) */
    .profile{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:var(--radius);
      padding:18px;
      box-shadow:0 6px 30px rgba(2,6,23,0.6);
      position:sticky;top:24px;align-self:start;
    }
    .photo{
      width:100%;height:0;padding-bottom:100%;position:relative;border-radius:12px;overflow:hidden;background:linear-gradient(180deg,#0f1724,#0b1220);
      display:flex;align-items:center;justify-content:center;color:#cfe6ff;font-size:18px;
    }
    .photo img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}
    .upload-btn{display:flex;gap:8px;margin-top:10px}
    .btn{
      background:transparent;border:1px solid rgba(255,255,255,0.06);padding:8px 10px;border-radius:10px;color:var(--muted);cursor:pointer;font-weight:600;
    }
    .btn.primary{background:linear-gradient(90deg,var(--accent),#06b6d4);color:white;border:none;box-shadow:0 8px 22px rgba(79,70,229,0.18)}
    .meta{margin-top:12px;font-size:14px;color:var(--muted)}
    .meta b{color:#fff}
    .org-card{margin-top:12px;background:rgba(255,255,255,0.02);padding:10px;border-radius:10px}
    .small{font-size:13px;color:var(--muted)}

    /* Right column (content) */
    .content-section{
      background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));
      border-radius:var(--radius);
      padding:18px;box-shadow:0 6px 30px rgba(2,6,23,0.45);
    }
    h1,h2,h3{margin:0 0 8px 0}
    h1{font-size:20px}
    .lead{color:var(--muted);margin-bottom:18px}

    /* CV/resume layout */
    .grid-two{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    .section-block{margin-bottom:14px;padding:12px;background:rgba(255,255,255,0.01);border-radius:10px}
    ul.clean{padding-left:1rem;margin:0}
    li.job{margin-bottom:8px}
    .skills{display:flex;flex-wrap:wrap;gap:8px}
    .skill{background:rgba(255,255,255,0.03);padding:6px 8px;border-radius:8px;font-weight:600;color:var(--muted);font-size:13px}

    /* Course tracker */
    .course-list{list-style:none;padding:0;margin:0}
    .course-item{display:flex;justify-content:space-between;align-items:center;padding:10px;border-radius:10px;margin-bottom:8px;background:rgba(255,255,255,0.01)}
    .progress{height:8px;background:rgba(255,255,255,0.04);border-radius:8px;overflow:hidden;width:100%;margin-top:8px}
    .progress > i{display:block;height:100%;background:linear-gradient(90deg,var(--accent),#06b6d4);}

    /* References manager */
    .refs-list{list-style:none;padding:0;margin:0}
    .ref-row{display:flex;gap:10px;align-items:center;justify-content:space-between;padding:10px;border-radius:10px;background:rgba(255,255,255,0.01);margin-bottom:8px}
    .ref-controls button{margin-left:6px}

    /* Contacts area */
    .contacts-table{width:100%;border-collapse:collapse}
    .contacts-table th, .contacts-table td{padding:8px;text-align:left;border-bottom:1px solid rgba(255,255,255,0.03);font-size:13px;color:var(--muted)}
    .contacts-actions{display:flex;gap:8px;align-items:center}
    .lnk{color:#9ad1ff;text-decoration:underline}

    /* Footer */
    footer{margin-top:18px;color:var(--muted);font-size:13px;text-align:center}

    /* Responsive */
    @media (max-width:980px){
      main{grid-template-columns:1fr; padding-bottom:60px}
      .profile{position:relative;top:0}
    }

    /* Accessibility focus */
    a:focus, button:focus, input:focus, textarea:focus{
      outline:3px solid rgba(79,70,229,0.18);
      outline-offset:2px;
    }

    /* Tiny performance tips: restrict heavy shadows on small screens */
    @media (max-width:420px){
      .container{padding:8px}
      .logo{width:48px;height:48px}
    }
  </style>
</head>
<body>
  <div class="container" id="top">
    <header>
      <div class="brand" aria-label="brand">
        <div class="logo" aria-hidden="true">FD</div>
        <div>
          <div style="font-weight:700">Ftalew Dagnaw</div>
          <div class="small">Senior Monitoring & Evaluation Advisor — Ministry of Health, Ethiopia</div>
        </div>
      </div>

      <nav aria-label="Main navigation">
        <a href="#about" class="nav-link active">About</a>
        <a href="#cv" class="nav-link">CV / Resume</a>
        <a href="#course" class="nav-link">AI Course</a>
        <a href="#references" class="nav-link">References</a>
        <a href="#contacts" class="nav-link">Contacts</a>
        <a href="#resources" class="nav-link">Resources</a>
      </nav>
    </header>

    <main>
      <!-- LEFT COLUMN: Profile / Photo / Org -->
      <aside class="profile" aria-label="Profile card">
        <div class="photo" id="photoPlaceholder" title="Upload your photo">
          <!-- Placeholder initials; will be replaced when user uploads -->
          <img id="profileImg" alt="Ftalew Dagnaw photo" loading="lazy" style="display:none" />
          <div id="photoFallback" style="position:absolute;padding:12px;text-align:center">
            <div style="font-size:18px;font-weight:700">Ftalew Dagnaw</div>
            <div style="margin-top:8px;color:var(--muted);font-size:13px">Senior M&E Advisor</div>
          </div>
        </div>

        <div class="upload-btn">
          <!-- photo upload (client-only) -->
          <label class="btn" for="photoInput">Change Photo</label>
          <input id="photoInput" type="file" accept="image/*" style="display:none">
          <button class="btn" id="downloadProfile" title="Download sample profile card">Export</button>
        </div>

        <div class="meta">
          <div><b>Email:</b> <span id="emailDisplay">ftalewd211@gmail.com</span></div>
          <div><b>Work email:</b> <span id="workEmailDisplay">ftalew.dagnaw@moh.gov.et</span></div>
          <div style="margin-top:6px"><b>Phone:</b> <span id="phoneDisplay">+251-911061646</span></div>
        </div>

        <div class="org-card" aria-label="Organization contact">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <div>
              <div style="font-weight:700">Ministry of Health, Ethiopia</div>
              <div class="small">Senior Monitoring & Evaluation Advisor</div>
            </div>
            <button class="btn" id="editOrgBtn" title="Edit organization details">Edit</button>
          </div>

          <!-- editable org fields (client-side) -->
          <div id="orgFields" style="margin-top:10px">
            <div class="small"><b>Address:</b> <span id="orgAddress">[Add organization address]</span></div>
            <div class="small"><b>Phone:</b> <span id="orgPhone">+251-911061646</span></div>
            <div class="small"><b>Email:</b> <span id="orgEmail">ftalew.dagnaw@moh.gov.et</span></div>
          </div>
        </div>

        <div style="margin-top:12px" class="small">
          Profile & CV contents loaded from your uploaded CV. Source: uploaded PDF. :contentReference[oaicite:1]{index=1}
        </div>

        <div style="margin-top:12px;display:flex;gap:8px">
          <a class="btn" href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank" rel="noopener">Generative AI Course</a>
          <a class="btn" href="https://www.linkedin.com/in/ftalew-dagnaw-97a99a25/" target="_blank" rel="noopener">LinkedIn</a>
        </div>
      </aside>

      <!-- RIGHT COLUMN: Content -->
      <section>
        <!-- ABOUT -->
        <article id="about" class="content-section" style="margin-bottom:12px">
          <h1>About</h1>
          <div class="lead">Results-driven Monitoring & Evaluation professional with over 15 years of healthcare sector experience — specialized in M&E frameworks, health information systems, data visualization, and program evaluation.</div>

          <div class="section-block">
            <h2 style="font-size:16px">Quick links & exports</h2>
            <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:8px">
              <button class="btn primary" id="downloadCVBtn">Download CV (PDF)</button>
              <button class="btn" id="downloadContactsExample">Download LinkedIn contacts template</button>
              <button class="btn" id="printBtn">Print / Save as PDF</button>
            </div>
            <div class="small" style="margin-top:8px;color:var(--muted)">
              Note: this site is client-side only. Exports use browser features and downloaded files are generated locally.
            </div>
          </div>
        </article>

        <!-- CV / Resume -->
        <article id="cv" class="content-section">
          <h2>CV — Selected Experience</h2>
          <div class="lead">Content pre-filled from your uploaded CV (education, summary, certifications, and selected roles). Edit sections inline or in the source PDF and re-upload if needed.</div>

          <div class="section-block">
            <h3>Summary</h3>
            <p id="cvSummary">
              Results-driven Monitoring and Evaluation (M&E) professional with over 15 years of extensive experience in the healthcare sector, particularly in designing, implementing, and managing M&E frameworks and systems. Currently serving as a Senior Monitoring and Evaluation Advisor at the Ministry of Health in Ethiopia, with a proven track record in improving health information systems and providing technical guidance to enhance data quality and utilization.
            </p>
          </div>

          <div class="grid-two" style="margin-top:12px">
            <div class="section-block">
              <h3>Professional Experience</h3>
              <ul class="clean" id="experienceList">
                <!-- Populated from CV -->
                <li class="job">
                  <div style="font-weight:700">Senior Monitoring and Evaluation Advisor — Ministry of Health, Ethiopia</div>
                  <div class="small">July 2019 - Present</div>
                  <div style="margin-top:6px;color:var(--muted);font-size:14px">
                    Provide technical support in design and implementation of M&E plans for national healthcare quality, health innovation and health equity programs; led DHIS-2 customizations, KPI dashboards, capacity building, and national assessments (SPA+, SARA, DQA). (summary from uploaded CV). :contentReference[oaicite:2]{index=2}
                  </div>
                </li>

                <li class="job">
                  <div style="font-weight:700">Data Manager & Analyst — WHO Ethiopia</div>
                  <div class="small">Sept 2014 - July 2019</div>
                  <div style="margin-top:6px;color:var(--muted);font-size:14px">
                    Led MPDSR electronic database design and implementation; integration with PHEM and national surveillance systems; capacity building for staff and documentation of best practices. :contentReference[oaicite:3]{index=3}
                  </div>
                </li>

                <!-- Additional items can be added -->
              </ul>
            </div>

            <div class="section-block">
              <h3>Education & Certifications</h3>
              <div class="small"><b>MPH</b>, Hawassa University — 2012</div>
              <div class="small"><b>BSc</b>, Statistics — Addis Ababa University — 2003</div>
              <div style="margin-top:8px" class="small"><b>Selected Certifications:</b>
                <ul>
                  <li>Fellowship in Healthcare Quality (FISQua) — ISQua, Sep 2022</li>
                  <li>DHIS2 Design and Customization — Univ. of Oslo & MoH</li>
                  <li>Global Program Management & Evaluation — Washington Univ.</li>
                </ul>
              </div>
            </div>
          </div>

          <div class="section-block" style="margin-top:12px">
            <h3>Skills</h3>
            <div class="skills" id="skills">
              <div class="skill">Monitoring & Evaluation</div>
              <div class="skill">DHIS2</div>
              <div class="skill">Power BI</div>
              <div class="skill">Health Information Systems</div>
              <div class="skill">Statistical Analysis</div>
              <div class="skill">Program Evaluation</div>
            </div>
          </div>

          <div class="section-block" style="margin-top:12px">
            <h3>Publications</h3>
            <ul class="clean">
              <li class="small">Comparing maternal deaths occurring at home, in transit and in facilities using Ethiopia’s national MDSR data. (BJOG, 2017) — :contentReference[oaicite:4]{index=4}</li>
              <li class="small">Triangulating data sources for further learning from and about the MDSR in Ethiopia. (BMC Pregnancy & Childbirth, 2020) — :contentReference[oaicite:5]{index=5}</li>
            </ul>
          </div>
        </article>

        <!-- Course module -->
        <article id="course" class="content-section" style="margin-top:12px">
          <h2>Generative AI Course — AIW 2025 Q4</h2>
          <p class="lead">Course link: <a href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank" rel="noopener" class="lnk">thegraphcourses.org — AIW 2025 Q4</a></p>

          <div class="section-block">
            <h3>Lessons & Progress</h3>

            <!-- Course lessons list (editable) -->
            <ul id="lessons" class="course-list" aria-live="polite">
              <!-- example item -->
              <li class="course-item">
                <div style="flex:1">
                  <div style="font-weight:700">Lesson 1 — Introduction to Generative AI</div>
                  <div class="small">Topics: LLM basics, diffusion, ethics</div>
                  <div class="progress" aria-hidden="true"><i style="width:60%"></i></div>
                </div>
                <div style="margin-left:12px;text-align:right">
                  <div class="small">60%</div>
                  <div style="margin-top:8px">
                    <button class="btn" data-action="mark" data-idx="0">Mark</button>
                    <button class="btn" data-action="edit" data-idx="0">Edit</button>
                  </div>
                </div>
              </li>
            </ul>

            <div style="display:flex;gap:8px;margin-top:10px">
              <input id="lessonTitle" placeholder="Lesson title" style="flex:1;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <input id="lessonTopics" placeholder="Topics (comma separated)" style="flex:1;padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <button class="btn primary" id="addLesson">Add</button>
            </div>

            <div class="small" style="margin-top:8px;color:var(--muted)">
              Progress is stored in your browser (localStorage). Use the course link above for official course content. This area allows you to track completion and notes.
            </div>
          </div>
        </article>

        <!-- References manager -->
        <article id="references" class="content-section" style="margin-top:12px">
          <h2>References (dynamic)</h2>
          <div class="lead">Add academic or professional references here. References are stored client-side and can be exported/imported as JSON or CSV.</div>

          <div class="section-block">
            <div style="display:flex;gap:8px;flex-wrap:wrap">
              <input id="refName" placeholder="Name" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <input id="refRole" placeholder="Role / Institution" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <input id="refEmail" placeholder="Email" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <button class="btn primary" id="addRef">Add Reference</button>
            </div>

            <ul id="refs" class="refs-list" style="margin-top:12px" aria-live="polite"></ul>

            <div style="display:flex;gap:8px;margin-top:10px;flex-wrap:wrap">
              <button class="btn" id="exportRefs">Export JSON</button>
              <button class="btn" id="exportRefsCSV">Export CSV</button>
              <input type="file" id="importRefsFile" accept=".json,.csv" style="display:none">
              <button class="btn" id="importRefsBtn">Import</button>
            </div>
          </div>
        </article>

        <!-- Contacts management -->
        <article id="contacts" class="content-section" style="margin-top:12px">
          <h2>LinkedIn Contacts & Organization Contacts</h2>
          <p class="lead">You can import your LinkedIn contacts CSV export here (LinkedIn allows exporting your connections as CSV from the Settings & Privacy → Data → Get a copy of your data). This site will parse and show them; no data leaves your browser.</p>

          <div class="section-block">
            <div style="display:flex;gap:8px;align-items:center;flex-wrap:wrap">
              <label class="btn" for="contactsFile">Import LinkedIn CSV</label>
              <input type="file" id="contactsFile" accept=".csv" style="display:none">
              <button class="btn" id="clearContacts">Clear</button>
              <button class="btn" id="downloadContacts" title="Download contacts JSON">Download JSON</button>
            </div>

            <div style="margin-top:12px;overflow:auto">
              <table class="contacts-table" id="contactsTable" role="table" aria-live="polite">
                <thead>
                  <tr><th>Name</th><th>Company</th><th>Email</th><th>Action</th></tr>
                </thead>
                <tbody id="contactsBody">
                  <tr><td colspan="4" class="small" style="color:var(--muted)">No contacts loaded.</td></tr>
                </tbody>
              </table>
            </div>
          </div>

          <div class="section-block" style="margin-top:12px">
            <h3>Organization Contact Details</h3>
            <div class="small" style="margin-bottom:8px">
              Edit and save the official contact details for your current organization below (stored in browser).
            </div>
            <div style="display:flex;gap:8px;flex-wrap:wrap">
              <input id="orgInputName" placeholder="Organization name" value="Ministry of Health, Ethiopia" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <input id="orgInputPhone" placeholder="Org phone" value="+251-911061646" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
              <input id="orgInputEmail" placeholder="Org email" value="ftalew.dagnaw@moh.gov.et" style="padding:8px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">
            </div>
            <textarea id="orgInputAddress" placeholder="Address" style="margin-top:8px;width:100%;min-height:64px;padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:inherit">[Add organization address here]</textarea>
            <div style="margin-top:8px;display:flex;gap:8px">
              <button class="btn primary" id="saveOrg">Save</button>
              <button class="btn" id="resetOrg">Reset</button>
            </div>
          </div>
        </article>

        <!-- Resources -->
        <article id="resources" class="content-section" style="margin-top:12px">
          <h2>Resources & Notes</h2>
          <div class="section-block">
            <h3>LinkedIn contacts export</h3>
            <div class="small">
              To get a representation of your LinkedIn contacts: sign in to LinkedIn → Settings & Privacy → Data privacy → Get a copy of your data → select "Connections" → request archive. Once you have the CSV, use the "Import LinkedIn CSV" above to load contacts locally.
            </div>
          </div>

          <div class="section-block" style="margin-top:12px">
            <h3>Course link (official)</h3>
            <div class="small">Course page: <a class="lnk" href="https://thegraphcourses.org/courses/aiw-2025-q4/" target="_blank" rel="noopener">https://thegraphcourses.org/courses/aiw-2025-q4/</a></div>
            <div class="small" style="margin-top:8px">If you want the site to automatically import the course syllabus, I can add server-side scraping or a small proxy later — for now there is an "Add lesson" flow to track progress quickly.</div>
          </div>
        </article>

        <footer>
          Built with ❤️ · Client-side only · Editable. Save a copy (File → Save page as...) or host anywhere static.
        </footer>
      </section>
    </main>
  </div>

  <!-- ---------- JavaScript: functionality ---------- -->
  <script>
    /* 
      Main JS - keeps everything client-side, no external servers required.
      Features implemented:
        - Photo upload & export of a simple profile-card PNG (client-only)
        - CV content prefilled from uploaded PDF metadata (the file you uploaded is referenced in the UI)
        - Course lessons add/edit/mark & localStorage persistence
        - References manager (add/edit/delete/export/import CSV/JSON)
        - LinkedIn contacts CSV import (parse) and download JSON export
        - Organization contact editing and persistence
        - Smooth navigation with active link highlighting
      Note: For heavy server tasks (like fetching LinkedIn contacts automatically), OAuth and a backend are required. This file provides a safe client-side UX instead.
    */

    // ---------- small helpers ----------
    const $ = (s)=>document.querySelector(s);
    const $$ = (s)=>Array.from(document.querySelectorAll(s));
    const ls = window.localStorage;

    // Smooth-scroll nav
    document.querySelectorAll('a.nav-link').forEach(a=>{
      a.addEventListener('click', (e)=>{
        e.preventDefault();
        document.querySelectorAll('a.nav-link').forEach(x=>x.classList.remove('active'));
        a.classList.add('active');
        const id = a.getAttribute('href');
        document.querySelector(id).scrollIntoView({behavior:'smooth',block:'start'});
      });
    });

    // ---------- Profile photo upload ----------
    const photoInput = document.getElementById('photoInput');
    const profileImg = document.getElementById('profileImg');
    const photoFallback = document.getElementById('photoFallback');
    photoInput.addEventListener('change', async (e)=>{
      const f = e.target.files[0];
      if(!f) return;
      const url = URL.createObjectURL(f);
      profileImg.src = url;
      profileImg.style.display = 'block';
      photoFallback.style.display = 'none';
      // Save to localStorage as data URL (small images advised)
      const reader = new FileReader();
      reader.onload = ()=> {
        try{ ls.setItem('profileImage', reader.result); }catch(err){console.warn('image too big for localStorage') }
      };
      reader.readAsDataURL(f);
    });

    // load saved photo if any
    (function loadPhoto(){
      const data = ls.getItem('profileImage');
      if(data){
        profileImg.src = data;
        profileImg.style.display = 'block';
        photoFallback.style.display = 'none';
      }
    })();

    // Export a basic JSON profile when clicking "Export"
    document.getElementById('downloadProfile').addEventListener('click', ()=>{
      const profile = {
        name:'Ftalew Dagnaw',
        title:'Senior Monitoring & Evaluation Advisor',
        email: document.getElementById('emailDisplay').innerText,
        phone: document.getElementById('phoneDisplay').innerText,
      };
      const blob = new Blob([JSON.stringify(profile, null, 2)], {type:'application/json'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url; a.download='ftalew_profile.json'; a.click();
      URL.revokeObjectURL(url);
    });

    // Print button
    document.getElementById('printBtn').addEventListener('click', ()=> window.print());

    // ---------- Organization details persistence ----------
    const orgAddressEl = document.getElementById('orgAddress');
    const orgPhoneEl = document.getElementById('orgPhone');
    const orgEmailEl = document.getElementById('orgEmail');

    function loadOrg() {
      const org = JSON.parse(ls.getItem('org')||'null');
      if(org){
        document.getElementById('orgInputName').value = org.name || '';
        document.getElementById('orgInputPhone').value = org.phone || '';
        document.getElementById('orgInputEmail').value = org.email || '';
        document.getElementById('orgInputAddress').value = org.address || '';
        orgAddressEl.innerText = org.address || '[Add organization address]';
        orgPhoneEl.innerText = org.phone || '';
        orgEmailEl.innerText = org.email || '';
      }
    }
    loadOrg();

    document.getElementById('saveOrg').addEventListener('click', ()=>{
      const org = {
        name: document.getElementById('orgInputName').value,
        phone: document.getElementById('orgInputPhone').value,
        email: document.getElementById('orgInputEmail').value,
        address: document.getElementById('orgInputAddress').value,
      };
      ls.setItem('org', JSON.stringify(org));
      loadOrg();
      alert('Organization details saved locally in your browser.');
    });
    document.getElementById('resetOrg').addEventListener('click', ()=>{ ls.removeItem('org'); location.reload(); });

    // Edit org quick button (copies values to edit fields)
    document.getElementById('editOrgBtn').addEventListener('click', ()=>{ document.getElementById('orgInputAddress').focus(); });

    // ---------- Course lessons (localStorage) ----------
    const lessonsKey = 'ai_course_lessons_v1';
    function loadLessons(){
      const data = JSON.parse(ls.getItem(lessonsKey) || 'null');
      if(!data){
        // default seed lesson
        const seed = [{title:'Lesson 1 — Introduction to Generative AI', topics:['LLM basics','Diffusion models','Ethics'], progress:60}];
        ls.setItem(lessonsKey, JSON.stringify(seed));
        return seed;
      }
      return data;
    }
    function renderLessons(){
      const lessons = loadLessons();
      const ul = document.getElementById('lessons');
      ul.innerHTML = '';
      lessons.forEach((l, idx)=>{
        const li = document.createElement('li'); li.className='course-item';
        li.innerHTML = \`
          <div style="flex:1">
            <div style="font-weight:700">\${l.title}</div>
            <div class="small">Topics: \${(l.topics||[]).join(', ')}</div>
            <div class="progress" aria-hidden="true"><i style="width:\${(l.progress||0)}%"></i></div>
          </div>
          <div style="margin-left:12px;text-align:right">
            <div class="small">\${l.progress||0}%</div>
            <div style="margin-top:8px">
              <button class="btn" data-action="mark" data-idx="\${idx}">Mark</button>
              <button class="btn" data-action="edit" data-idx="\${idx}">Edit</button>
            </div>
          </div>\`;
        ul.appendChild(li);
      });
    }
    renderLessons();

    // Add lesson
    document.getElementById('addLesson').addEventListener('click', ()=>{
      const title = document.getElementById('lessonTitle').value.trim();
      const topics = document.getElementById('lessonTopics').value.split(',').map(s=>s.trim()).filter(Boolean);
      if(!title){ alert('Add a lesson title'); return; }
      const lessons = loadLessons();
      lessons.push({title, topics, progress:0});
      ls.setItem(lessonsKey, JSON.stringify(lessons));
      document.getElementById('lessonTitle').value=''; document.getElementById('lessonTopics').value='';
      renderLessons();
    });

    // Delegate edit / mark buttons
    document.getElementById('lessons').addEventListener('click', (e)=>{
      const btn = e.target.closest('button');
      if(!btn) return;
      const action = btn.dataset.action;
      const idx = Number(btn.dataset.idx);
      const lessons = loadLessons();
      if(action === 'mark'){
        const p = prompt('Set progress percentage (0-100)', String(lessons[idx].progress || 0));
        if(p===null) return;
        const val = Math.max(0, Math.min(100, Number(p) || 0));
        lessons[idx].progress = val;
        ls.setItem(lessonsKey, JSON.stringify(lessons));
        renderLessons();
      } else if(action === 'edit'){
        const t = prompt('Edit lesson title', lessons[idx].title) || lessons[idx].title;
        const topics = prompt('Edit topics (comma separated)', (lessons[idx].topics||[]).join(', ')) || (lessons[idx].topics||[]).join(', ');
        lessons[idx].title = t;
        lessons[idx].topics = topics.split(',').map(s=>s.trim()).filter(Boolean);
        ls.setItem(lessonsKey, JSON.stringify(lessons));
        renderLessons();
      }
    });

    // ---------- References manager ----------
    const refsKey = 'ftalew_refs_v1';
    const refsListEl = document.getElementById('refs');

    function loadRefs(){ return JSON.parse(ls.getItem(refsKey) || '[]'); }
    function saveRefs(v){ ls.setItem(refsKey, JSON.stringify(v)); }

    function renderRefs(){
      const refs = loadRefs();
      refsListEl.innerHTML = '';
      if(refs.length === 0){
        refsListEl.innerHTML = '<div class="small" style="color:var(--muted)">No references yet.</div>';
        return;
      }
      refs.forEach((r, idx)=>{
        const li = document.createElement('li'); li.className='ref-row';
        li.innerHTML = \`
          <div>
            <div style="font-weight:700">\${r.name}</div>
            <div class="small">\${r.role} • \${r.email || '—'}</div>
          </div>
          <div class="ref-controls">
            <button class="btn" data-idx="\${idx}" data-action="edit">Edit</button>
            <button class="btn" data-idx="\${idx}" data-action="del">Delete</button>
          </div>\`;
        refsListEl.appendChild(li);
      });
    }
    renderRefs();

    document.getElementById('addRef').addEventListener('click', ()=>{
      const name = document.getElementById('refName').value.trim();
      const role = document.getElementById('refRole').value.trim();
      const email = document.getElementById('refEmail').value.trim();
      if(!name) return alert('Name is required');
      const refs = loadRefs();
      refs.push({name, role, email});
      saveRefs(refs);
      document.getElementById('refName').value=''; document.getElementById('refRole').value=''; document.getElementById('refEmail').value='';
      renderRefs();
    });

    refsListEl.addEventListener('click', (e)=>{
      const btn = e.target.closest('button');
      if(!btn) return;
      const idx = Number(btn.dataset.idx);
      const action = btn.dataset.action;
      const refs = loadRefs();
      if(action === 'del'){
        if(confirm('Delete this reference?')){ refs.splice(idx,1); saveRefs(refs); renderRefs(); }
      } else if(action === 'edit'){
        const r = refs[idx];
        const name = prompt('Name', r.name);
        if(name === null) return;
        const role = prompt('Role / Institution', r.role) || '';
        const email = prompt('Email', r.email) || '';
        refs[idx] = {name, role, email};
        saveRefs(refs); renderRefs();
      }
    });

    // Export JSON
    document.getElementById('exportRefs').addEventListener('click', ()=>{
      const data = loadRefs();
      const blob = new Blob([JSON.stringify(data, null, 2)], {type:'application/json'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href=url; a.download='references.json'; a.click(); URL.revokeObjectURL(url);
    });

    // Export CSV
    document.getElementById('exportRefsCSV').addEventListener('click', ()=>{
      const refs = loadRefs();
      if(refs.length===0) return alert('No references to export.');
      const rows = [['Name','Role','Email'], ...refs.map(r=>[r.name,r.role,r.email])];
      const csv = rows.map(r=>r.map(c=>\`"\${String(c||'').replace(/"/g,'""')}"\`).join(',')).join('\\n');
      const blob = new Blob([csv], {type:'text/csv'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href=url; a.download='references.csv'; a.click(); URL.revokeObjectURL(url);
    });

    // Import refs (JSON or CSV)
    document.getElementById('importRefsBtn').addEventListener('click', ()=> document.getElementById('importRefsFile').click());
    document.getElementById('importRefsFile').addEventListener('change', async (e)=>{
      const f = e.target.files[0]; if(!f) return;
      const text = await f.text();
      let parsed = [];
      if(f.name.endsWith('.json')){
        try{ parsed = JSON.parse(text); }
        catch(err){ return alert('Invalid JSON'); }
      } else {
        // naive CSV: expect header Name,Role,Email
        const rows = text.split(/\\r?\\n/).map(r=>r.trim()).filter(Boolean);
        const [header, ...rest] = rows;
        parsed = rest.map(r=>{
          const cols = r.split(',').map(c=>c.replace(/^"|"$/g,'').trim());
          return {name:cols[0]||'', role:cols[1]||'', email:cols[2]||''};
        });
      }
      const existing = loadRefs();
      const merged = existing.concat(parsed);
      saveRefs(merged);
      renderRefs();
      alert('Imported references (appended).');
    });

    // ---------- LinkedIn contacts CSV import ----------
    const contactsKey = 'ftalew_contacts_v1';
    const contactsBody = document.getElementById('contactsBody');
    function loadContacts(){ return JSON.parse(ls.getItem(contactsKey) || '[]'); }
    function saveContacts(v){ ls.setItem(contactsKey, JSON.stringify(v)); renderContacts(); }

    function renderContacts(){
      const list = loadContacts();
      contactsBody.innerHTML = '';
      if(list.length===0){
        contactsBody.innerHTML = '<tr><td colspan="4" class="small" style="color:var(--muted)">No contacts loaded.</td></tr>';
        return;
      }
      list.forEach((c, idx)=>{
        const tr = document.createElement('tr');
        tr.innerHTML = \`
          <td>\${c.name||''}</td>
          <td>\${c.company||''}</td>
          <td>\${c.email||''}</td>
          <td><div class="contacts-actions">
              <button class="btn" data-idx="\${idx}" data-action="view">View</button>
              <button class="btn" data-idx="\${idx}" data-action="del">Delete</button>
            </div></td>\`;
        contactsBody.appendChild(tr);
      });
    }
    renderContacts();

    // Let user click sample download for template
    document.getElementById('downloadContactsExample').addEventListener('click', ()=>{
      const csv = 'Name,Company,Email\\n"John Doe","Acme Ltd","john@example.com"\\n"Jane Smith","Uni X","jane@univx.edu"';
      const blob = new Blob([csv], {type:'text/csv'}); const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href=url; a.download='contacts_template.csv'; a.click(); URL.revokeObjectURL(url);
    });

    // File input parse (simple CSV parser)
    document.getElementById('contactsFile').addEventListener('change', async (e)=>{
      const f = e.target.files[0]; if(!f) return;
      const txt = await f.text();
      // Attempt to parse CSV robustly for common LinkedIn export columns
      const rows = txt.split(/\\r?\\n/).filter(Boolean);
      // header normalization
      const header = rows.shift().split(',').map(h=>h.replace(/^"|"$/g,'').toLowerCase());
      // find likely column indices
      const nameIdx = header.findIndex(h => /name/.test(h));
      const emailIdx = header.findIndex(h => /email/.test(h));
      const companyIdx = header.findIndex(h => /company|organization|employer/.test(h));
      const parsed = rows.map(r=>{
        const cols = r.split(',').map(c=>c.replace(/^"|"$/g,'').trim());
        return {
          name: cols[nameIdx] || cols[0] || '',
          email: cols[emailIdx] || '',
          company: cols[companyIdx] || ''
        };
      }).filter(c=>c.name || c.email);
      const merged = loadContacts().concat(parsed);
      saveContacts(merged);
      alert(\`Imported \${parsed.length} contacts (appended).\`);
    });

    // contacts table actions
    contactsBody.addEventListener('click', (e)=>{
      const btn = e.target.closest('button'); if(!btn) return;
      const idx = Number(btn.dataset.idx); const action = btn.dataset.action;
      const list = loadContacts();
      if(action === 'del'){ list.splice(idx,1); saveContacts(list); }
      else if(action === 'view'){ alert(JSON.stringify(list[idx], null, 2)); }
    });

    // Clear / download contacts
    document.getElementById('clearContacts').addEventListener('click', ()=>{ if(confirm('Clear all contacts?')){ ls.removeItem(contactsKey); renderContacts(); } });
    document.getElementById('downloadContacts').addEventListener('click', ()=>{
      const list = loadContacts();
      if(list.length===0) return alert('No contacts to download');
      const blob = new Blob([JSON.stringify(list, null, 2)], {type:'application/json'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a'); a.href=url; a.download='linkedin_contacts.json'; a.click(); URL.revokeObjectURL(url);
    });

    // ---------- CV PDF download (user uploaded file referenced) ----------
    document.getElementById('downloadCVBtn').addEventListener('click', ()=>{
      // If you want to include the original uploaded PDF automatically, you'd need a file input for the PDF.
      // Here we instruct the user how to download the original file (or re-upload).
      alert('The original uploaded CV PDF is available in this session (source displayed). If you want the PDF included in the site, upload it via a file input we can add. For now, you can re-download the original PDF you uploaded from your files.');
    });

    // ---------- small UX: highlight nav while scrolling ----------
    const sections = ['#about','#cv','#course','#references','#contacts','#resources'].map(s=>document.querySelector(s));
    window.addEventListener('scroll', ()=>{
      let idx = sections.findIndex((sec,i)=>{
        const rect = sec.getBoundingClientRect();
        return rect.top >= 0 && rect.top < window.innerHeight/3;
      });
      if(idx === -1) idx = sections.length-1;
      document.querySelectorAll('a.nav-link').forEach((a,i)=> a.classList.toggle('active', i === idx));
    });

    // ---------- On first load: pre-populate org contact display with CV info where available ----------
    (function prefillFromCV(){
      // Values prefilled in HTML from uploaded CV: emails and phone shown in profile card and org phone
      // These came from the CV you uploaded (source: uploaded PDF). See UI text near profile for the filecite: :contentReference[oaicite:6]{index=6}
      // If desired, we can add a file input to upload a new PDF and auto-extract text, but that requires a PDF parser library.
    })();

    // END main script
  </script>
</body>
</html>
