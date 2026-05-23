---
layout: default
title: "Muhammad Rizwan — Data Scientist & AI Researcher"
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" crossorigin="anonymous" />

<style>
  :root {
    --teal: #0f6e56;
    --teal-light: #e1f5ee;
    --teal-mid: #1d9e75;
    --ink: #1a1a1a;
    --ink-soft: #4a4a4a;
    --ink-muted: #7a7a7a;
    --cream: #faf9f6;
    --border: rgba(15,110,86,0.15);
    --serif: 'DM Serif Display', Georgia, serif;
    --sans: 'Plus Jakarta Sans', sans-serif;
    --mono: 'DM Mono', monospace;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body, .page-content, .wrapper {
    background: var(--cream) !important;
    font-family: var(--sans);
    color: var(--ink);
  }

  /* ── HERO ── */
  .hero {
    padding: 4rem 0 3rem;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(29,158,117,0.08) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-tag {
    display: inline-block;
    font-family: var(--mono);
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--teal);
    background: var(--teal-light);
    border: 1px solid rgba(15,110,86,0.2);
    padding: 4px 12px;
    border-radius: 100px;
    margin-bottom: 1.2rem;
  }

  .hero h1 {
    font-family: var(--serif);
    font-size: clamp(2.4rem, 6vw, 3.8rem);
    line-height: 1.1;
    color: var(--ink);
    margin-bottom: 0.5rem;
  }

  .hero h1 em {
    font-style: italic;
    color: var(--teal);
  }

  .hero-sub {
    font-size: 1.05rem;
    color: var(--ink-soft);
    max-width: 600px;
    line-height: 1.7;
    margin: 1rem 0 1.8rem;
  }

  .hero-keywords {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 2rem;
  }

  .kw {
    font-family: var(--mono);
    font-size: 0.78rem;
    color: var(--ink-soft);
    background: white;
    border: 1px solid var(--border);
    padding: 4px 12px;
    border-radius: 6px;
  }

  .hero-links {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    font-family: var(--sans);
    font-size: 0.88rem;
    font-weight: 500;
    padding: 9px 18px;
    border-radius: 8px;
    text-decoration: none;
    transition: all 0.18s ease;
  }

  .btn-primary {
    background: var(--teal);
    color: white;
    border: 1px solid var(--teal);
  }

  .btn-primary:hover { background: #0a5542; }

  .btn-outline {
    background: white;
    color: var(--ink-soft);
    border: 1px solid var(--border);
  }

  .btn-outline:hover { border-color: var(--teal); color: var(--teal); background: var(--teal-light); }

  /* ── SECTIONS ── */
  .section {
    padding: 3rem 0;
    border-bottom: 1px solid var(--border);
  }

  .section:last-child { border-bottom: none; }

  .sec-label {
    font-family: var(--mono);
    font-size: 0.68rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 0.4rem;
  }

  .sec-title {
    font-family: var(--serif);
    font-size: 1.9rem;
    color: var(--ink);
    margin-bottom: 1.8rem;
    line-height: 1.2;
  }

  /* ── NEXUS STATEMENT ── */
  .nexus-block {
    background: white;
    border: 1px solid var(--border);
    border-left: 4px solid var(--teal);
    border-radius: 0 12px 12px 0;
    padding: 1.8rem 2rem;
    font-size: 1.05rem;
    line-height: 1.85;
    color: var(--ink-soft);
  }

  .nexus-block strong { color: var(--ink); font-weight: 600; }

  /* ── NEWS ── */
  .news-list { display: flex; flex-direction: column; gap: 1rem; }

  .news-item {
    display: grid;
    grid-template-columns: 130px 1fr;
    gap: 1rem;
    align-items: start;
    padding: 1rem 1.25rem;
    background: white;
    border: 1px solid var(--border);
    border-radius: 10px;
    transition: border-color 0.15s;
  }

  .news-item:hover { border-color: var(--teal-mid); }

  .news-date {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--teal);
    padding-top: 2px;
  }

  .news-text {
    font-size: 0.93rem;
    line-height: 1.6;
    color: var(--ink-soft);
  }

  .news-text strong { color: var(--ink); }

  /* ── EXPERIENCE ── */
  .exp-list { display: flex; flex-direction: column; gap: 0; }

  .exp-item {
    display: grid;
    grid-template-columns: 8px 1fr;
    gap: 0 1.2rem;
    padding-bottom: 2rem;
    position: relative;
  }

  .exp-item::before {
    content: '';
    position: absolute;
    left: 3px; top: 10px; bottom: 0;
    width: 2px;
    background: var(--border);
  }

  .exp-item:last-child::before { display: none; }

  .exp-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--teal);
    margin-top: 6px;
    flex-shrink: 0;
    position: relative;
    z-index: 1;
  }

  .exp-role {
    font-weight: 600;
    font-size: 0.97rem;
    color: var(--ink);
  }

  .exp-org {
    font-size: 0.85rem;
    color: var(--teal);
    margin: 2px 0 4px;
  }

  .exp-period {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--ink-muted);
    margin-bottom: 8px;
  }

  .exp-bullets {
    font-size: 0.87rem;
    color: var(--ink-soft);
    line-height: 1.7;
    padding-left: 1rem;
  }

  .exp-bullets li { margin-bottom: 3px; }

  /* ── EDUCATION ── */
  .edu-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1rem;
  }

  .edu-card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.4rem 1.5rem;
    transition: border-color 0.15s, transform 0.15s;
  }

  .edu-card:hover { border-color: var(--teal-mid); transform: translateY(-2px); }

  .edu-degree {
    font-family: var(--serif);
    font-size: 1.15rem;
    color: var(--ink);
    margin-bottom: 4px;
  }

  .edu-inst {
    font-size: 0.82rem;
    color: var(--ink-muted);
    line-height: 1.5;
    margin-bottom: 8px;
  }

  .edu-meta {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--teal);
  }

  .edu-badge {
    display: inline-block;
    font-family: var(--mono);
    font-size: 0.7rem;
    background: var(--teal-light);
    color: var(--teal);
    border-radius: 6px;
    padding: 2px 8px;
    margin-top: 8px;
  }

  /* ── PUBLICATIONS ── */
  .pub-list { display: flex; flex-direction: column; gap: 1rem; }

  .pub-item {
    background: white;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.2rem 1.4rem;
    transition: border-color 0.15s;
  }

  .pub-item:hover { border-color: var(--teal-mid); }

  .pub-num {
    font-family: var(--mono);
    font-size: 0.68rem;
    color: var(--teal);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 5px;
  }

  .pub-title {
    font-weight: 600;
    font-size: 0.92rem;
    color: var(--ink);
    line-height: 1.5;
    margin-bottom: 4px;
  }

  .pub-venue {
    font-size: 0.82rem;
    color: var(--ink-muted);
    margin-bottom: 8px;
  }

  .pub-venue em { color: var(--teal); font-style: normal; font-weight: 500; }

  .pub-link {
    font-family: var(--mono);
    font-size: 0.75rem;
    color: var(--teal);
    text-decoration: none;
  }

  .pub-link:hover { text-decoration: underline; }

  /* ── PROJECTS ── */
  .proj-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1rem;
  }

  .proj-card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    transition: border-color 0.15s, transform 0.15s;
  }

  .proj-card:hover { border-color: var(--teal-mid); transform: translateY(-2px); }

  .proj-icon {
    width: 40px; height: 40px;
    background: var(--teal-light);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.2rem;
    margin-bottom: 1rem;
  }

  .proj-name {
    font-weight: 600;
    font-size: 0.95rem;
    color: var(--ink);
    margin-bottom: 6px;
  }

  .proj-desc {
    font-size: 0.85rem;
    color: var(--ink-soft);
    line-height: 1.6;
    margin-bottom: 12px;
  }

  .proj-tags { display: flex; flex-wrap: wrap; gap: 5px; }

  .tag {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--ink-muted);
    background: var(--cream);
    border: 1px solid var(--border);
    padding: 2px 8px;
    border-radius: 5px;
  }

  /* ── ACHIEVEMENTS ── */
  .ach-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1rem;
  }

  .ach-card {
    display: flex;
    gap: 12px;
    align-items: flex-start;
    background: white;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.1rem 1.2rem;
  }

  .ach-icon {
    font-size: 1.1rem;
    color: var(--teal);
    flex-shrink: 0;
    margin-top: 2px;
  }

  .ach-text {
    font-size: 0.87rem;
    color: var(--ink-soft);
    line-height: 1.55;
  }

  .ach-text strong { color: var(--ink); display: block; margin-bottom: 2px; }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
  }

  .skill-group {
    background: white;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.2rem;
  }

  .skill-group-title {
    font-family: var(--mono);
    font-size: 0.72rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--teal);
    margin-bottom: 10px;
  }

  .skill-tags { display: flex; flex-wrap: wrap; gap: 6px; }

  .skill-tag {
    font-size: 0.8rem;
    color: var(--ink-soft);
    background: var(--cream);
    border: 1px solid var(--border);
    padding: 3px 10px;
    border-radius: 6px;
  }

  /* ── CONTACT ── */
  .contact-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    padding: 1rem 0;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--ink-soft);
    background: white;
    border: 1px solid var(--border);
    padding: 10px 20px;
    border-radius: 10px;
    text-decoration: none;
    transition: all 0.15s;
  }

  .contact-link:hover { border-color: var(--teal); color: var(--teal); background: var(--teal-light); }

  .contact-link i { color: var(--teal); font-size: 1rem; }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .news-item { grid-template-columns: 1fr; }
    .news-date { margin-bottom: -6px; }
    .hero h1 { font-size: 2.2rem; }
  }
</style>

<!-- ═══════════════════════════════════════════ HERO -->
<div class="hero">
  <div class="hero-tag">Open to Research Collaborations</div>
  <h1>Muhammad<br><em>Rizwan</em></h1>
  <p class="hero-sub">
    Data Scientist · AI Researcher · Research Associate at PAF-IAST<br>
    Building transparent, interpretable machine learning systems for real-world healthcare challenges.
  </p>
  <div class="hero-keywords">
    <span class="kw">Explainable AI</span>
    <span class="kw">Chronic Kidney Disease</span>
    <span class="kw">Multimodal Data</span>
    <span class="kw">Transdisciplinary Research</span>
    <span class="kw">Scientific ML</span>
  </div>
  <div class="hero-links">
    <a class="btn btn-primary" href="mailto:rizwanawan612@gmail.com"><i class="fa-solid fa-envelope"></i> Get in Touch</a>
    <a class="btn btn-outline" href="https://orcid.org/0009-0004-9735-1743" target="_blank"><i class="fa-brands fa-orcid"></i> ORCID</a>
    <a class="btn btn-outline" href="https://github.com/rizwanawan612" target="_blank"><i class="fa-brands fa-github"></i> GitHub</a>
    <a class="btn btn-outline" href="https://www.linkedin.com/in/muhammad-rizwan-b08350202/" target="_blank"><i class="fa-brands fa-linkedin"></i> LinkedIn</a>
  </div>
</div>

<!-- ═══════════════════════════════════════════ ABOUT / NEXUS -->
<div class="section">
  <div class="sec-label">Research Vision</div>
  <div class="sec-title">Bridging AI & Medicine</div>
  <div class="nexus-block">
    My research interests are <strong>interdisciplinary</strong>, lying at the intersection of artificial intelligence, machine learning, and explainable AI. I approach my work as <strong>transdisciplinary</strong> — bridging academic theory, technological innovation, and industrial applications. My primary ambition is to develop <strong>transparent, robust, and interpretable</strong> model methods for multimodal data, building a <strong>NEXUS</strong> between researchers, engineers, and professionals to solve real-world healthcare challenges.
  </div>
</div>

<!-- ═══════════════════════════════════════════ NEWS -->
<div class="section">
  <div class="sec-label">Updates</div>
  <div class="sec-title">Latest News</div>
  <div class="news-list">
    <div class="news-item">
      <div class="news-date">July 2025</div>
      <div class="news-text"><strong>Research Associate role begins</strong> — Joined the funded project "Machine Learning Approach for Prophecy on Chronic Kidney Disease" (HEREF-3067) at PAF-IAST under Dr. Rashid Naseem.</div>
    </div>
    <div class="news-item">
      <div class="news-date">Apr 10, 2025</div>
      <div class="news-text"><strong>MS Thesis Successfully Defended</strong> — Completed MS in Data Science under the supervision of Dr. Rashid Naseem at PAF-IAST, Haripur.</div>
    </div>
    <div class="news-item">
      <div class="news-date">Mar 24, 2025</div>
      <div class="news-text"><strong>Conference Presentation</strong> — Paper on <em>Publications Landscape of Public Sector Medical Schools of Pakistan</em> presented at the First Conference on Uses of AI in Medical Sciences, Wah Medical College.</div>
    </div>
    <div class="news-item">
      <div class="news-date">Mar 14, 2025</div>
      <div class="news-text"><strong>PKR 2 Million Research Grant</strong> — MS research project awarded funding under the HED KPK Endowment Fund (HEREF-3067).</div>
    </div>
    <div class="news-item">
      <div class="news-date">2025</div>
      <div class="news-text"><strong>Startup Founded</strong> — Launched <em>"Kidney Vision"</em> through the Business Incubation Center at PAF-IAST, an AI-powered CKD early detection platform.</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ EXPERIENCE -->
<div class="section">
  <div class="sec-label">Career</div>
  <div class="sec-title">Professional Experience</div>
  <div class="exp-list">
    <div class="exp-item">
      <div class="exp-dot"></div>
      <div>
        <div class="exp-role">Research Associate <span style="font-weight:400;color:var(--ink-muted)">— Funded Project</span></div>
        <div class="exp-org">School of Computing Sciences, PAF-IAST · Haripur, Pakistan</div>
        <div class="exp-period">Jul 2025 – Present</div>
        <ul class="exp-bullets">
          <li>Leading ML model development for CKD prediction under project HEREF-3067 supervised by Dr. Rashid Naseem</li>
          <li>Data collection, cleaning, preprocessing, and feature engineering from biomarker datasets</li>
          <li>Applying Explainable AI (XAI) techniques (SHAP, LIME) for model transparency</li>
          <li>Authoring research papers, technical reports, and grant documentation</li>
          <li>Statistical analysis and visualization to interpret and communicate results</li>
        </ul>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-dot"></div>
      <div>
        <div class="exp-role">Assistant Supervisor HR</div>
        <div class="exp-org">Dept. of Chemical & Energy Engineering (C&EE), PAF-IAST</div>
        <div class="exp-period">Jul 2024 – Present</div>
        <ul class="exp-bullets">
          <li>Personal Assistant cum Department Coordinator, Faculty of Engineering Sciences & Technology</li>
        </ul>
      </div>
    </div>
    <div class="exp-item">
      <div class="exp-dot"></div>
      <div>
        <div class="exp-role">Secretarial Staff</div>
        <div class="exp-org">Sino-Pak Center for Artificial Intelligence / Dept. of Biological & Health Sciences, PAF-IAST</div>
        <div class="exp-period">Feb 2021 – Jun 2024</div>
        <ul class="exp-bullets">
          <li>Served as Personal Assistant cum Department Coordinator in the Faculty of Life Sciences (FLS)</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ EDUCATION -->
<div class="section">
  <div class="sec-label">Academic Background</div>
  <div class="sec-title">Education</div>
  <div class="edu-grid">
    <div class="edu-card">
      <div class="edu-degree">M.S. in Data Science</div>
      <div class="edu-inst">Pak-Austria Fachhochschule: Institute of Applied Sciences and Technology, Haripur, Pakistan</div>
      <div class="edu-meta">2021 – 2025</div>
      <div class="edu-badge">CGPA 3.24 / 4.00</div>
      <div style="margin-top:10px; font-size:0.8rem; color:var(--ink-muted); line-height:1.5;">
        Thesis: <em>Machine Learning Approach for Prophecy of Chronic Kidney Disease</em><br>
        Supervisor: Dr. Rashid Naseem
      </div>
    </div>
    <div class="edu-card">
      <div class="edu-degree">M.Sc. in Mathematics</div>
      <div class="edu-inst">University of Education, Jauharabad, Pakistan</div>
      <div class="edu-meta">2018 – 2021</div>
      <div class="edu-badge">GPA 3.00 / 4.00</div>
    </div>
    <div class="edu-card">
      <div class="edu-degree">B.Sc.</div>
      <div class="edu-inst">Government National College, University of Karachi, Pakistan</div>
      <div class="edu-meta">2014 – 2016</div>
      <div class="edu-badge">1st Division</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ PUBLICATIONS -->
<div class="section">
  <div class="sec-label">Scholarly Work</div>
  <div class="sec-title">Research Publications</div>
  <div class="pub-list">

    <div class="pub-item">
      <div class="pub-num">Publication · 01 · 2025</div>
      <div class="pub-title">Comparative Analysis of Supervised Machine Learning Algorithms for Predicting Chronic Kidney Diseases</div>
      <div class="pub-venue">Muhammad Rizwan, Maqbool Khan, Maria Gul, Muhammad Ahmad Khan, Rashid Naseem, Momina Shaheen — <em>International Conference on Data Processing and Networking, 2025</em></div>
      <a class="pub-link" href="https://doi.org/10.1007/978-981-96-3102-534" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> doi.org/10.1007/978-981-96-3102-534</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Publication · 02 · 2025</div>
      <div class="pub-title">Intelligent Delignification: Leveraging Explainable AI for Ozone Transport Modeling and Optimization</div>
      <div class="pub-venue">Muhammad Rizwan, Muhammad Ahmad Khan, Sharifullah Khan et al. — <em>Nature Scientific Reports, 2025</em></div>
      <a class="pub-link" href="https://doi.org/10.1038/s41598-025-28638-7" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> doi.org/10.1038/s41598-025-28638-7</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Publication · 03 · 2025</div>
      <div class="pub-title">Explainable AI-Driven Chronic Kidney Disease Prediction System</div>
      <div class="pub-venue">Muhammad Ahmad Khan, Muhammad Rizwan, Saira Bhatti, Maqbool Khan — <em>IEEE ETECOM 2025</em></div>
      <a class="pub-link" href="https://doi.org/10.1109/ETECOM66111.2025.11319132" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> doi.org/10.1109/ETECOM66111.2025.11319132</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Dataset · 04 · 2025</div>
      <div class="pub-title">Saraiki Handwritten Characters (0–9) Dataset</div>
      <div class="pub-venue">Muhammad Ahmad Khan, Muhammad Rizwan — <em>Mendeley Data, 2025</em></div>
      <a class="pub-link" href="https://data.mendeley.com/datasets/wcnzkw9n2f/1" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> data.mendeley.com/datasets/wcnzkw9n2f/1</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Dataset · 05 · 2025</div>
      <div class="pub-title">Optimizing Ozone Delignification of Lignocellulose Dataset</div>
      <div class="pub-venue">Muhammad Rizwan, Muhammad Ahmad Khan, Khurram Shahzad Baig — <em>Figshare, 2025</em></div>
      <a class="pub-link" href="https://doi.org/10.6084/m9.figshare.29289128" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> doi.org/10.6084/m9.figshare.29289128</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Dataset · 06 · 2025</div>
      <div class="pub-title">A Benchmark Biomarker Dataset for Classification of Chronic Kidney Disease Patients in Pakistan</div>
      <div class="pub-venue">Muhammad Rizwan, Rashid Naseem — <em>Figshare, 2025</em></div>
      <a class="pub-link" href="https://doi.org/10.6084/m9.figshare.29603663" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> doi.org/10.6084/m9.figshare.29603663</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Conference · 07 · 2025</div>
      <div class="pub-title">Publications Landscape of Public Sector Medical Schools of Pakistan</div>
      <div class="pub-venue">Muhammad Rizwan, Muhammad Fozan, Waqar Khalid Saeed — <em>1st Conference on AI in Medical Sciences, Wah Medical College, 2025</em></div>
      <a class="pub-link" href="https://wahmedicalcollege.edu.pk/2024/12/03/1st-conference-on-uses-of-artificial-intelligence-in-medical-sciences-by-wah-medical-college/" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square" style="font-size:0.7rem"></i> Conference page</a>
    </div>

    <div class="pub-item">
      <div class="pub-num">Competition · 08 · 2025</div>
      <div class="pub-title">Data Science for Resilience: Transforming WASH and Learning Environments in Climate-Vulnerable Regions</div>
      <div class="pub-venue">Muhammad Rizwan, Muzammil Irshad, Rashid Naseem — <em>Inter-University Climate Change Competition, NIUIP, UET Peshawar / UNICEF, 2025</em></div>
    </div>

    <div class="pub-item">
      <div class="pub-num">Competition · 09 · 2025</div>
      <div class="pub-title">AI-Driven Hybrid MBR-RO Membrane Technology for Sustainable Industrial Wastewater Treatment</div>
      <div class="pub-venue">Asma Iqbal, Engr. Muhammad Shahzaib, Muhammad Rizwan, Dr. Khurram Shahzad Baig — <em>Inter-University Climate Change Competition, NIUIP, UET Peshawar / UNICEF, 2025</em></div>
    </div>

  </div>
</div>

<!-- ═══════════════════════════════════════════ RESEARCH PROJECTS -->
<div class="section">
  <div class="sec-label">Applied Work</div>
  <div class="sec-title">Research Projects</div>
  <div class="proj-grid">
    <div class="proj-card">
      <div class="proj-icon">🫘</div>
      <div class="proj-name">CKD Prediction System</div>
      <div class="proj-desc">ML-based system for early detection of Chronic Kidney Disease using biomarker data from Pakistani patients. Incorporates XAI techniques for clinical interpretability.</div>
      <div class="proj-tags">
        <span class="tag">Python</span><span class="tag">XAI / SHAP</span><span class="tag">SMOTE</span><span class="tag">Healthcare ML</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-icon">🫀</div>
      <div class="proj-name">Heart Disease Prediction</div>
      <div class="proj-desc">Semester project developing a machine learning model to predict likelihood of heart disease from clinical risk factors, aimed at supporting medical professionals.</div>
      <div class="proj-tags">
        <span class="tag">Python</span><span class="tag">Classification</span><span class="tag">2021–2022</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-icon">🫁</div>
      <div class="proj-name">Lung Cancer Prediction</div>
      <div class="proj-desc">Team-led semester project building a predictive model for lung cancer risk through systematic analysis of patient risk factors.</div>
      <div class="proj-tags">
        <span class="tag">Python</span><span class="tag">Risk Modeling</span><span class="tag">2022–2023</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-icon">💧</div>
      <div class="proj-name">Ozone Delignification Optimization</div>
      <div class="proj-desc">Applied explainable AI to model and optimize ozone transport in lignocellulosic biomass delignification — published in Nature Scientific Reports.</div>
      <div class="proj-tags">
        <span class="tag">XAI</span><span class="tag">Regression</span><span class="tag">Industrial ML</span>
      </div>
    </div>
    <div class="proj-card">
      <div class="proj-icon">👁️</div>
      <div class="proj-name">Kidney Vision — Startup</div>
      <div class="proj-desc">AI-powered CKD screening platform founded through PAF-IAST's Business Incubation Center. Aims to make early kidney disease detection accessible in Pakistan.</div>
      <div class="proj-tags">
        <span class="tag">Startup</span><span class="tag">Healthtech</span><span class="tag">BIC PAF-IAST</span>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ ACHIEVEMENTS -->
<div class="section">
  <div class="sec-label">Recognition</div>
  <div class="sec-title">Achievements</div>
  <div class="ach-grid">
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-trophy"></i></div>
      <div class="ach-text"><strong>PKR 2M Research Grant</strong> HED KPK Endowment Fund (HEREF-3067) · 2025</div>
    </div>
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-rocket"></i></div>
      <div class="ach-text"><strong>Startup Founder — Kidney Vision</strong> Business Incubation Center, PAF-IAST · 2024</div>
    </div>
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-calendar-check"></i></div>
      <div class="ach-text"><strong>Three-Day Conference & Expo Organizer</strong> PAF-IAST · 2024</div>
    </div>
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-stethoscope"></i></div>
      <div class="ach-text"><strong>Workshop Conductor — AI in Medicine</strong> Pakistan Kidney Center, Abbottabad · 2024</div>
    </div>
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-flask"></i></div>
      <div class="ach-text"><strong>Technical Workshop Organizer</strong> Lab Calibration & ISO Standards, PAF-IAST · 2022</div>
    </div>
    <div class="ach-card">
      <div class="ach-icon"><i class="fa-solid fa-lightbulb"></i></div>
      <div class="ach-text"><strong>PML Hacks 1K Innovation Challenge Winner</strong> Cash prize Rs. 1,000 · 2022</div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ SKILLS -->
<div class="section">
  <div class="sec-label">Toolkit</div>
  <div class="sec-title">Skills & Software</div>
  <div class="skills-grid">
    <div class="skill-group">
      <div class="skill-group-title">Machine Learning & AI</div>
      <div class="skill-tags">
        <span class="skill-tag">Scikit-learn</span>
        <span class="skill-tag">XAI / SHAP</span>
        <span class="skill-tag">LIME</span>
        <span class="skill-tag">Classification</span>
        <span class="skill-tag">Regression</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Programming & Data</div>
      <div class="skill-tags">
        <span class="skill-tag">Python</span>
        <span class="skill-tag">SPSS</span>
        <span class="skill-tag">Power BI</span>
        <span class="skill-tag">Origin</span>
        <span class="skill-tag">GraphPad Prism</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Research & Writing</div>
      <div class="skill-tags">
        <span class="skill-tag">Scientific Writing</span>
        <span class="skill-tag">Grant Writing</span>
        <span class="skill-tag">Literature Review</span>
        <span class="skill-tag">Statistical Analysis</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Productivity</div>
      <div class="skill-tags">
        <span class="skill-tag">MS Office</span>
        <span class="skill-tag">Critical Thinking</span>
        <span class="skill-tag">Project Management</span>
        <span class="skill-tag">Collaboration</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Languages</div>
      <div class="skill-tags">
        <span class="skill-tag">English</span>
        <span class="skill-tag">Urdu</span>
        <span class="skill-tag">Punjabi</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Community</div>
      <div class="skill-tags">
        <span class="skill-tag">Green Youth Movement</span>
        <span class="skill-tag">Welfare Society</span>
        <span class="skill-tag">PAF-IAST Clubs</span>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════ CONTACT -->
<div class="section" style="border-bottom:none; text-align:center;">
  <div class="sec-label">Connect</div>
  <div class="sec-title" style="margin-bottom:0.5rem;">Get In Touch</div>
  <p style="color:var(--ink-muted); font-size:0.9rem; margin-bottom:1.5rem;">Open to research collaborations, speaking invitations, and interdisciplinary projects.</p>
  <div class="contact-row">
    <a class="contact-link" href="mailto:rizwanawan612@gmail.com"><i class="fa-solid fa-envelope"></i> rizwanawan612@gmail.com</a>
    <a class="contact-link" href="tel:+923142008778"><i class="fa-solid fa-phone"></i> +92 314 200 8778</a>
    <a class="contact-link" href="https://www.linkedin.com/in/muhammad-rizwan-b08350202/" target="_blank"><i class="fa-brands fa-linkedin"></i> LinkedIn</a>
    <a class="contact-link" href="https://github.com/rizwanawan612" target="_blank"><i class="fa-brands fa-github"></i> GitHub</a>
    <a class="contact-link" href="https://orcid.org/0009-0004-9735-1743" target="_blank"><i class="fa-brands fa-orcid"></i> ORCID</a>
  </div>
</div>
