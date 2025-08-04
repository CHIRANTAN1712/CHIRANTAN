<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Chirantan Maity | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="Portfolio of Chirantan Maity - Technical Assistant, Virologist, Molecular Biologist">
  <link href="https://fonts.googleapis.com/css?family=Montserrat:600,400|Fira+Mono&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #2e294e;
      --secondary: #e71d36;
      --background: #f9fafc;
      --card: #f3e9e5;
      --column: #e7ecef;
      --accent: #ff9f1c;
      --text: #22223b;
      --muted: #797596;
      --shadow: 0 8px 28px rgba(45, 35, 66, 0.12);
    }
    html, body {
      margin: 0;
      padding: 0;
      font-family: 'Montserrat', Arial, sans-serif;
      background: var(--background);
      color: var(--text);
      min-height: 100vh;
    }
    header {
      background: linear-gradient(100deg, var(--primary) 60%, var(--secondary) 100%);
      color: #fff;
      padding: 2.5rem 0 2rem 0;
      text-align: center;
      position: relative;
      box-shadow: var(--shadow);
    }
    .profile-pic {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 50%;
      border: 5px solid var(--accent);
      margin-top: -70px;
      background: #fff;
      box-shadow: 0 4px 14px rgba(45, 35, 66, 0.18);
      object-position: center top;
    }
    h1 {
      font-size: 2.1rem;
      margin: 0.7rem 0 0.25rem;
      letter-spacing: 1.2px;
      font-weight: 700;
      line-height: 1.1;
    }
    .subtitle {
      font-size: 1.1rem;
      color: var(--accent);
      margin-bottom: 0.9rem;
      font-weight: 500;
    }
    .contact-links {
      margin-top: 0.7rem;
      margin-bottom: 2.2rem;
      font-size: 1.07rem;
    }
    .contact-links a {
      color: var(--accent);
      text-decoration: none;
      margin: 0 0.7rem;
      transition: color 0.2s;
      font-weight: 600;
      letter-spacing: 0.2px;
    }
    .contact-links a:hover {
      color: var(--secondary);
      text-decoration: underline;
    }
    .main-columns {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      gap: 22px;
      margin: 0 auto;
      max-width: 1100px;
      padding: 36px 16px;
      flex-wrap: wrap;
    }
    .column-nav {
      background: var(--column);
      border-radius: 13px;
      box-shadow: var(--shadow);
      padding: 32px 20px;
      min-width: 210px;
      max-width: 260px;
      font-size: 1.09rem;
      font-weight: 600;
      display: flex;
      flex-direction: column;
      gap: 18px;
    }
    .column-nav a {
      display: block;
      color: var(--primary);
      padding: 10px 12px;
      border-radius: 7px;
      text-decoration: none;
      transition: background 0.12s, color 0.12s;
      font-size: 1.07rem;
      font-weight: 600;
      border-left: 4px solid transparent;
    }
    .column-nav a.active, .column-nav a:hover {
      background: var(--accent);
      color: #fff;
      border-left: 4px solid var(--secondary);
    }
    .column-content {
      background: var(--card);
      box-shadow: var(--shadow);
      border-radius: 13px;
      padding: 36px 38px 36px 38px;
      flex: 1 1 350px;
      min-width: 310px;
      max-width: 600px;
      display: none;
      animation: fadeIn 0.5s;
      margin-bottom: 30px;
      position: relative;
    }
    .column-content.active {
      display: block;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px);}
      to   { opacity: 1; transform: translateY(0);}
    }
    section h2 {
      color: var(--secondary);
      font-size: 1.33rem;
      margin-bottom: 0.6rem;
      margin-top: 0;
      border-left: 6px solid var(--accent);
      padding-left: 0.7rem;
      letter-spacing: 0.7px;
      font-weight: 700;
      background: linear-gradient(90deg, #fff5 0%, #f3e9e5 100%);
      border-radius: 3px;
      box-shadow: 0 0 0 0 #fff;
    }
    ul {
      padding-left: 1.2em;
      margin: 0;
    }
    ul li {
      margin-bottom: 0.55rem;
      font-size: 1.03rem;
    }
    .project-list li {
      margin-bottom: 1.15rem;
      background: #fff;
      border-left: 4px solid var(--secondary);
      border-radius: 4px;
      padding: 0.7em 1.1em 0.5em 1.2em;
      box-shadow: 0 1px 5px 0 rgba(0,48,73,0.04);
    }
    .project-title {
      font-weight: 700;
      color: var(--primary);
      font-size: 1.06rem;
    }
    .project-mentor {
      color: var(--muted);
      font-size: 0.99rem;
      font-style: italic;
      margin-left: 0.7em;
    }
    .about-block {
      background: #fff;
      padding: 1.2em 1.5em;
      border-left: 6px solid var(--accent);
      border-radius: 5px;
      margin-bottom: 1.5em;
      box-shadow: 0 1px 5px 0 rgba(247,127,0,0.05);
      font-size: 1.07rem;
    }
    .footer-bar {
      text-align:center;
      color:#bbb;
      font-size:0.92rem;
      margin:2.8rem 0 1.2rem 0;
      padding-bottom: 18px;
    }
    .footer-logo {
      display: block;
      margin: 10px auto 0 auto;
      width: 130px;
      height: auto;
      max-width: 90vw;
    }
    @media (max-width: 900px) {
      .main-columns {
        flex-direction: column;
        align-items: stretch;
        gap: 0;
      }
      .column-nav {
        flex-direction: row;
        justify-content: center;
        padding: 18px 12px;
        min-width: unset;
        max-width: unset;
        gap: 9px;
        margin-bottom: 16px;
      }
      .column-nav a {
        font-size: 0.97rem;
        padding: 7px 10px;
      }
      .column-content {
        padding: 18px 8vw 18px 8vw;
      }
    }
    @media (max-width: 500px) {
      .column-content {
        padding: 11px 2vw 11px 2vw;
        min-width: unset;
        max-width: unset;
      }
      .profile-pic {
        width: 70px;
        height: 70px;
        margin-top: -35px;
      }
      .footer-logo {
        width: 88px;
      }
    }
  </style>
</head>
<body>
  <header>
    <img src="image1" alt="Chirantan Maity's profile photo" class="profile-pic">
    <h1>Chirantan Maity</h1>
    <div class="subtitle">
      Technical Assistant, Division of Virology and Zoonoses, ICMR-NIRTH
    </div>
    <div class="contact-links">
      <a href="mailto:chirantan1712maity@gmail.com">chirantan1712maity@gmail.com</a> |
      <a href="mailto:chirantan.maity@icmr.gov.in">chirantan.maity@icmr.gov.in</a> |
      <a href="https://in.linkedin.com/in/chirantan-maity-91b8b2246" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </header>
  <div class="main-columns">
    <nav class="column-nav" id="columnNav">
      <a href="#about" class="active" onclick="showTab(event, 'about')">About Me</a>
      <a href="#expertise" onclick="showTab(event, 'expertise')">Expertise</a>
      <a href="#skills" onclick="showTab(event, 'skills')">Skills</a>
      <a href="#projects" onclick="showTab(event, 'projects')">Projects</a>
      <a href="#achievements" onclick="showTab(event, 'achievements')">Achievements</a>
      <a href="#alumni" onclick="showTab(event, 'alumni')">Alumni</a>
      <a href="#contact" onclick="showTab(event, 'contact')">Contact</a>
    </nav>
    <div class="column-content active" id="about">
      <section>
        <h2>About Me</h2>
        <div class="about-block">
          I currently work as a Technical Assistant in the Division of Virology and Zoonoses in ICMR-NIRTH. As a virologist, I have a profound knowledge of molecular virology and immunology. Here, I am involved in the <b>Pan India Respiratory Surveillance</b> and <b>Global Measles and Rubella Laboratory Network (GMRLN)</b> projects. Apart from this, I also monitor the Hepatitis viruses, Dengue, and Chikungunya serological and molecular testing and prevalence. Assuring the maintenance of Biosafety of this SL-VRDL lab is my additional job role.
        </div>
      </section>
    </div>
    <div class="column-content" id="expertise">
      <section>
        <h2>Areas of Expertise</h2>
        <ul>
          <li>Virology</li>
          <li>Molecular Biology</li>
          <li>Sanger Sequencing</li>
          <li>Serology</li>
          <li>Immunology</li>
          <li>Bioinformatics</li>
        </ul>
      </section>
    </div>
    <div class="column-content" id="skills">
      <section>
        <h2>Skills</h2>
        <ul>
          <li>Sanger sequencing</li>
          <li>Sequence analysis</li>
          <li>PCR</li>
          <li>Real-time PCR</li>
          <li>ELISA</li>
          <li>Cell-culture</li>
          <li>TCID<sub>50</sub></li>
          <li>Cloning</li>
          <li>Biosafety</li>
        </ul>
      </section>
    </div>
    <div class="column-content" id="projects">
      <section>
        <h2>Projects</h2>
        <ul class="project-list">
          <li>
            <span class="project-title">Global Measles and Rubella Laboratory Network (GMRLN)</span><br>
            Involved in surveillance, laboratory diagnosis, and reporting as part of the global initiative to eliminate measles and rubella.
          </li>
          <li>
            <span class="project-title">Pan India Respiratory Surveillance</span><br>
            Contributing to nationwide surveillance of respiratory viruses, including sample processing, molecular testing, and data analysis.
          </li>
          <li>
            <span class="project-title">Development of Tetraplex Real-time RT-PCR for Simultaneous Screening of Influenza Virus A, B, C and D</span>
            <span class="project-mentor">Under Dr. Varsha Potdar, Scientist-E, Head of Influenza Group, ICMR-NIV</span><br>
            Developed a multiplex assay for simultaneous detection of influenza virus types A, B, C, and D.
          </li>
          <li>
            <span class="project-title">Characterization and Antimicrobial Activity of Biologically Synthesized Silver Nanoparticles from Microorganisms</span>
            <span class="project-mentor">Under Dr. Arindam Roy, Assistant Professor, Dept. of Microbiology, Ramakrishna Mission Vidyamandira, Belur Math</span><br>
            Focused on nanoparticle synthesis from microbes and their antimicrobial characterization.
          </li>
        </ul>
      </section>
    </div>
    <div class="column-content" id="achievements">
      <section>
        <h2>Achievements</h2>
        <ul>
          <li>JAM-BT-2022</li>
          <li>GATE-XL-2022, 2023</li>
          <li>IIPCET-2022</li>
          <li>NFSUCET-2022</li>
        </ul>
      </section>
    </div>
    <div class="column-content" id="alumni">
      <section>
        <h2>Alumni</h2>
        <ul>
          <li>RKMV'22</li>
          <li>ICMR-NIV'24</li>
        </ul>
      </section>
    </div>
    <div class="column-content" id="contact">
      <section>
        <h2>Contact</h2>
        <ul>
          <li><strong>Email (Personal):</strong> <a href="mailto:chirantan1712maity@gmail.com">chirantan1712maity@gmail.com</a></li>
          <li><strong>Email (Office):</strong> <a href="mailto:chirantan.maity@icmr.gov.in">chirantan.maity@icmr.gov.in</a></li>
          <li><strong>LinkedIn:</strong> <a href="https://in.linkedin.com/in/chirantan-maity-91b8b2246" target="_blank" rel="noopener">chirantan-maity-91b8b2246</a></li>
        </ul>
      </section>
    </div>
  </div>
  <div class="footer-bar">
    Portfolio generated on 2025-08-04.
    <img src="image2" alt="ICMR NIRTH Logo" class="footer-logo">
  </div>
  <script>
    function showTab(event, tabId) {
      event.preventDefault();
      document.querySelectorAll('.column-content').forEach(function(el) {
        el.classList.remove('active');
      });
      document.querySelectorAll('.column-nav a').forEach(function(el) {
        el.classList.remove('active');
      });
      document.getElementById(tabId).classList.add('active');
      event.target.classList.add('active');
    }
    window.addEventListener('DOMContentLoaded', function() {
      var hash = window.location.hash.replace('#', '');
      if(hash && document.getElementById(hash)) {
        showTab({preventDefault:()=>{}}, hash);
        document.querySelector('.column-nav a[href="#'+hash+'"]').classList.add('active');
      }
    });
  </script>
</body>
</html>
