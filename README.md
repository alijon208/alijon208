
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .readme {
    font-family: 'Fira Code', monospace;
    background: var(--surface-0);
    color: var(--text-primary);
    padding: 32px 28px;
    max-width: 680px;
    margin: 0 auto;
  }

  .header-block { text-align: center; margin-bottom: 36px; }

  .typing-container {
    display: inline-block;
    border: 0.5px solid var(--border-strong);
    border-radius: 6px;
    padding: 10px 20px;
    margin-bottom: 20px;
    background: var(--surface-1);
  }

  .typing-text {
    font-size: 13px;
    font-weight: 500;
    color: var(--text-secondary);
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--text-primary);
    width: 0;
    animation: typing 3s steps(40, end) forwards, blink 0.75s step-end infinite;
    animation-delay: 0.3s;
  }

  @keyframes typing {
    from { width: 0; }
    to { width: 22ch; }
  }
  @keyframes blink {
    from, to { border-color: transparent; }
    50% { border-color: var(--text-primary); }
  }

  .name-prefix { font-size: 11px; color: var(--text-muted); letter-spacing: 2px; text-transform: uppercase; margin-bottom: 4px; }
  .name-main { font-size: 22px; font-weight: 600; color: var(--text-primary); letter-spacing: -0.5px; }
  .name-role { font-size: 12px; color: var(--text-secondary); margin-top: 4px; }

  .divider { border: none; border-top: 0.5px solid var(--border); margin: 24px 0; }

  .section-label {
    font-size: 10px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--text-muted);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-label::after { content: ''; flex: 1; height: 0.5px; background: var(--border); }

  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 28px; }

  .about-card {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 8px;
    padding: 14px;
  }
  .about-card .icon { font-size: 16px; margin-bottom: 6px; display: block; }
  .about-card p { font-size: 11px; color: var(--text-secondary); line-height: 1.6; }
  .about-card strong { color: var(--text-primary); font-weight: 500; }

  .skills-svg-wrap {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 10px;
    overflow: hidden;
    padding: 16px;
    margin-bottom: 28px;
  }

  .focus-list { list-style: none; margin-bottom: 28px; }
  .focus-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 10px 0;
    border-bottom: 0.5px solid var(--border);
    font-size: 12px;
    color: var(--text-secondary);
    line-height: 1.5;
  }
  .focus-item:last-child { border-bottom: none; }
  .focus-num { font-size: 10px; color: var(--text-muted); min-width: 18px; padding-top: 1px; font-weight: 500; }

  /* Projects */
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 28px; }

  .project-card {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    transition: border-color 0.2s, background 0.2s;
    cursor: pointer;
    text-decoration: none;
    display: block;
  }
  .project-card:hover { border-color: var(--border-stronger); background: var(--surface-2); }

  .project-card.add-card {
    border-style: dashed;
    opacity: 0.5;
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100px;
    cursor: default;
  }

  .project-num { font-size: 9px; color: var(--text-muted); letter-spacing: 2px; margin-bottom: 6px; }
  .project-title { font-size: 13px; font-weight: 500; color: var(--text-primary); margin-bottom: 6px; }
  .project-desc { font-size: 11px; color: var(--text-secondary); line-height: 1.5; margin-bottom: 10px; }
  .project-tags { display: flex; gap: 6px; flex-wrap: wrap; }
  .project-tag {
    font-size: 9px;
    color: var(--text-muted);
    border: 0.5px solid var(--border);
    border-radius: 4px;
    padding: 2px 6px;
    letter-spacing: 0.5px;
  }
  .project-link {
    display: flex;
    align-items: center;
    gap: 5px;
    font-size: 10px;
    color: var(--text-muted);
    margin-top: 10px;
    padding-top: 10px;
    border-top: 0.5px solid var(--border);
  }
  .project-link i { font-size: 12px; }

  /* Portfolio CTA */
  .portfolio-cta {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: var(--surface-1);
    border: 0.5px solid var(--border-strong);
    border-radius: 10px;
    padding: 18px 20px;
    margin-bottom: 28px;
    text-decoration: none;
    transition: border-color 0.2s, background 0.2s;
    cursor: pointer;
  }
  .portfolio-cta:hover { border-color: var(--border-stronger); background: var(--surface-2); }

  .portfolio-cta-left { display: flex; flex-direction: column; gap: 4px; }
  .portfolio-cta-eyebrow { font-size: 9px; letter-spacing: 2px; color: var(--text-muted); text-transform: uppercase; }
  .portfolio-cta-title { font-size: 14px; font-weight: 500; color: var(--text-primary); }
  .portfolio-cta-url { font-size: 11px; color: var(--text-muted); }

  .portfolio-cta-arrow {
    width: 32px;
    height: 32px;
    border: 0.5px solid var(--border-strong);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    transition: background 0.2s;
  }
  .portfolio-cta:hover .portfolio-cta-arrow { background: var(--surface-0); }
  .portfolio-cta-arrow i { font-size: 15px; color: var(--text-secondary); }

  /* Connect */
  .connect-row { display: flex; gap: 10px; flex-wrap: wrap; }
  .connect-badge {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 8px 14px;
    border: 0.5px solid var(--border-strong);
    border-radius: 6px;
    font-size: 11px;
    color: var(--text-secondary);
    background: var(--surface-1);
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
  }
  .connect-badge:hover { background: var(--surface-2); color: var(--text-primary); border-color: var(--border-stronger); }
  .connect-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--text-muted); }

  .footer-quote {
    margin-top: 28px;
    padding: 14px 18px;
    border-left: 2px solid var(--border-stronger);
    font-size: 11px;
    color: var(--text-muted);
    font-style: italic;
  }

  /* Animations */
  .skill-bar-fill {
    transform-origin: left;
    animation: barGrow 1.2s cubic-bezier(0.16, 1, 0.3, 1) both;
  }
  @keyframes barGrow { from { transform: scaleX(0); } to { transform: scaleX(1); } }
  .skill-bar-fill:nth-child(1) { animation-delay: 0.1s; }
  .skill-bar-fill:nth-child(2) { animation-delay: 0.2s; }
  .skill-bar-fill:nth-child(3) { animation-delay: 0.3s; }
  .skill-bar-fill:nth-child(4) { animation-delay: 0.4s; }
  .skill-bar-fill:nth-child(5) { animation-delay: 0.5s; }
  .skill-bar-fill:nth-child(6) { animation-delay: 0.6s; }
  .skill-bar-fill:nth-child(7) { animation-delay: 0.7s; }
  .skill-bar-fill:nth-child(8) { animation-delay: 0.8s; }
  .skill-bar-fill:nth-child(9) { animation-delay: 0.9s; }
  .skill-bar-fill:nth-child(10) { animation-delay: 1.0s; }

  .node-dot { opacity: 0; animation: fadeIn 0.4s forwards; }
  @keyframes fadeIn { to { opacity: 1; } }
  .category-label { opacity: 0; animation: fadeIn 0.5s forwards 0.2s; }

  @media (prefers-reduced-motion: reduce) {
    .skill-bar-fill, .node-dot, .category-label, .typing-text {
      animation: none; width: auto; transform: scaleX(1); opacity: 1;
    }
    .typing-text { border-right: none; }
  }
</style>

<div class="readme">

  <!-- Header -->
  <div class="header-block">
    <div class="typing-container">
      <div class="typing-text">Frontend Developer 👨‍💻</div>
    </div>
    <div class="name-prefix">Hello, I'm</div>
    <div class="name-main">Muxammad Ali</div>
    <div class="name-role">Abdruxmonov · Tashkent, Uzbekistan</div>
  </div>

  <hr class="divider">

  <!-- About -->
  <div class="section-label">About me</div>
  <div class="about-grid">
    <div class="about-card">
      <span class="icon"><i class="ti ti-sparkles" aria-hidden="true"></i></span>
      <p>Turning ideas into <strong>beautiful</strong> and functional web experiences</p>
    </div>
    <div class="about-card">
      <span class="icon"><i class="ti ti-seedling" aria-hidden="true"></i></span>
      <p>Currently mastering <strong>React, Redux</strong> and modern JS tooling</p>
    </div>
    <div class="about-card">
      <span class="icon"><i class="ti ti-target" aria-hidden="true"></i></span>
      <p>Goal: become a <strong>professional</strong> frontend engineer</p>
    </div>
    <div class="about-card">
      <span class="icon"><i class="ti ti-wand" aria-hidden="true"></i></span>
      <p>Never stops experimenting with <strong>design & animation</strong></p>
    </div>
  </div>

  <!-- Skills -->
  <div class="section-label">Tech stack</div>
  <div class="skills-svg-wrap">
    <svg width="100%" viewBox="0 0 620 310" role="img">
      <title>Skills diagram</title>
      <desc>Horizontal bar chart showing proficiency across frontend skills</desc>

      <text class="category-label ts" x="0" y="18" fill="var(--text-muted)" font-size="9" letter-spacing="2" font-family="'Fira Code',monospace">CORE</text>
      <text x="0" y="42" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">HTML5</text>
      <rect x="68" y="30" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="30" width="285" height="14" rx="2" fill="var(--text-primary)" opacity="0.85"/>
      <text x="378" y="42" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">95%</text>

      <text x="0" y="65" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">CSS3</text>
      <rect x="68" y="53" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="53" width="270" height="14" rx="2" fill="var(--text-primary)" opacity="0.8"/>
      <text x="378" y="65" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">90%</text>

      <text x="0" y="88" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">SCSS</text>
      <rect x="68" y="76" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="76" width="240" height="14" rx="2" fill="var(--text-primary)" opacity="0.75"/>
      <text x="378" y="88" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">80%</text>

      <line x1="0" y1="104" x2="620" y2="104" stroke="var(--border)" stroke-width="0.5"/>
      <text class="category-label ts" x="0" y="122" fill="var(--text-muted)" font-size="9" letter-spacing="2" font-family="'Fira Code',monospace">JAVASCRIPT</text>

      <text x="0" y="146" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">JS ES6+</text>
      <rect x="68" y="134" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="134" width="225" height="14" rx="2" fill="var(--text-primary)" opacity="0.78"/>
      <text x="378" y="146" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">75%</text>

      <text x="0" y="169" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">React</text>
      <rect x="68" y="157" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="157" width="210" height="14" rx="2" fill="var(--text-primary)" opacity="0.75"/>
      <text x="378" y="169" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">70%</text>

      <text x="0" y="192" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Redux</text>
      <rect x="68" y="180" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="180" width="180" height="14" rx="2" fill="var(--text-primary)" opacity="0.7"/>
      <text x="378" y="192" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">60%</text>

      <line x1="0" y1="208" x2="620" y2="208" stroke="var(--border)" stroke-width="0.5"/>
      <text class="category-label ts" x="0" y="226" fill="var(--text-muted)" font-size="9" letter-spacing="2" font-family="'Fira Code',monospace">TOOLING &amp; PLATFORM</text>

      <text x="0" y="250" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Vite</text>
      <rect x="68" y="238" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="238" width="240" height="14" rx="2" fill="var(--text-primary)" opacity="0.75"/>
      <text x="378" y="250" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">80%</text>

      <text x="0" y="273" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Firebase</text>
      <rect x="68" y="261" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="261" width="165" height="14" rx="2" fill="var(--text-primary)" opacity="0.68"/>
      <text x="378" y="273" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">55%</text>

      <text x="0" y="296" font-size="11" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Bootstrap</text>
      <rect x="68" y="284" width="300" height="14" rx="2" fill="var(--border)" opacity="0.5"/>
      <rect class="skill-bar-fill" x="68" y="284" width="255" height="14" rx="2" fill="var(--text-primary)" opacity="0.8"/>
      <text x="378" y="296" font-size="10" fill="var(--text-muted)" font-family="'Fira Code',monospace">85%</text>

      <!-- Stack map -->
      <text x="450" y="18" font-size="9" letter-spacing="2" fill="var(--text-muted)" font-family="'Fira Code',monospace">STACK MAP</text>
      <circle class="node-dot" cx="468" cy="50" r="16" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="468" y="54" font-size="9" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">HTML</text>
      <circle class="node-dot" cx="524" cy="50" r="16" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="524" y="54" font-size="9" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">CSS</text>
      <circle class="node-dot" cx="580" cy="50" r="16" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="580" y="54" font-size="9" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">SCSS</text>
      <circle class="node-dot" cx="468" cy="110" r="18" fill="var(--surface-2)" stroke="var(--border-stronger)" stroke-width="0.8"/>
      <text x="468" y="108" font-size="8" text-anchor="middle" fill="var(--text-primary)" font-family="'Fira Code',monospace" font-weight="500">JS</text>
      <text x="468" y="118" font-size="7" text-anchor="middle" fill="var(--text-muted)" font-family="'Fira Code',monospace">ES6+</text>
      <circle class="node-dot" cx="536" cy="110" r="20" fill="var(--surface-2)" stroke="var(--border-stronger)" stroke-width="1"/>
      <text x="536" y="114" font-size="9" text-anchor="middle" fill="var(--text-primary)" font-family="'Fira Code',monospace" font-weight="500">React</text>
      <circle class="node-dot" cx="600" cy="110" r="16" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="600" y="114" font-size="8" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Redux</text>
      <line x1="484" y1="66" x2="518" y2="94" stroke="var(--border)" stroke-width="0.5" stroke-dasharray="3 2"/>
      <line x1="540" y1="66" x2="538" y2="90" stroke="var(--border)" stroke-width="0.5" stroke-dasharray="3 2"/>
      <line x1="564" y1="66" x2="554" y2="92" stroke="var(--border)" stroke-width="0.5" stroke-dasharray="3 2"/>
      <line x1="554" y1="130" x2="596" y2="200" stroke="var(--border)" stroke-width="0.5" stroke-dasharray="3 2"/>
      <circle class="node-dot" cx="468" cy="180" r="14" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="468" y="184" font-size="8" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Vite</text>
      <circle class="node-dot" cx="510" cy="200" r="14" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="510" y="204" font-size="7" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Firebase</text>
      <circle class="node-dot" cx="560" cy="180" r="14" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="560" y="184" font-size="7" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Boot.</text>
      <circle class="node-dot" cx="600" cy="200" r="14" fill="none" stroke="var(--border-strong)" stroke-width="0.5"/>
      <text x="600" y="204" font-size="7" text-anchor="middle" fill="var(--text-secondary)" font-family="'Fira Code',monospace">Tailwind</text>
      <line x1="484" y1="126" x2="470" y2="166" stroke="var(--border)" stroke-width="0.5" stroke-dasharray="3 2"/>
    </svg>
  </div>

  <!-- Current Focus -->
  <div class="section-label">Current focus</div>
  <ul class="focus-list">
    <li class="focus-item"><span class="focus-num">01</span><span>Building responsive UI components with React and SCSS</span></li>
    <li class="focus-item"><span class="focus-num">02</span><span>Learning modern JS (ES6+), state management, Vite tooling</span></li>
    <li class="focus-item"><span class="focus-num">03</span><span>Improving accessibility and performance on small projects</span></li>
  </ul>

  <!-- Projects -->
  <div class="section-label">Projects</div>
  <div class="projects-grid">
    <div class="project-card add-card">
      <p style="font-size:11px; color: var(--text-muted); text-align:center">
        <i class="ti ti-plus" aria-hidden="true"></i><br>Add project
      </p>
    </div>
    <div class="project-card add-card">
      <p style="font-size:11px; color: var(--text-muted); text-align:center">
        <i class="ti ti-plus" aria-hidden="true"></i><br>Add project
      </p>
    </div>
  </div>

  <!-- Portfolio CTA -->
  <div class="section-label">Portfolio</div>
  <a class="portfolio-cta" href="https://your-portfolio.com" target="_blank" rel="noopener">
    <div class="portfolio-cta-left">
      <span class="portfolio-cta-eyebrow">Live site</span>
      <span class="portfolio-cta-title">muhammadali.dev</span>
      <span class="portfolio-cta-url">your-portfolio.com</span>
    </div>
    <div class="portfolio-cta-arrow">
      <i class="ti ti-arrow-up-right" aria-hidden="true"></i>
    </div>
  </a>

  <!-- Connect -->
  <div class="section-label">Connect</div>
  <div class="connect-row">
    <a class="connect-badge" href="https://t.me/abduraxmonovm" target="_blank" rel="noopener">
      <span class="connect-dot"></span>
      Telegram · @abduraxmonovm
    </a>
    <a class="connect-badge" href="https://instagram.com/abduraxmon0v" target="_blank" rel="noopener">
      <span class="connect-dot"></span>
      Instagram · @abduraxmon0v
    </a>
  </div>

  <div class="footer-quote">"Code. Learn. Build. Repeat."</div>

</div>
