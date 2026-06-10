<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>John Clyde Montaña</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg:        #0d0d10;
    --bg-card:   #13131a;
    --bg-card2:  #18181f;
    --border:    rgba(255,255,255,0.07);
    --border-md: rgba(255,255,255,0.11);
    --red:       #e84040;
    --red-glow:  rgba(232,64,64,0.12);
    --red-bdr:   rgba(232,64,64,0.28);
    --orange:    #e0822e;
    --green:     #3dba6e;
    --green-glow:rgba(61,186,110,0.1);
    --blue:      #4a8fd9;
    --blue-glow: rgba(74,143,217,0.1);
    --yellow:    #d4a838;
    --text:      #e6e4de;
    --muted:     #6e6c66;
    --dim:       #3a3835;
    --mono: 'JetBrains Mono', monospace;
    --sans: 'Inter', sans-serif;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    font-size: 14px;
    line-height: 1.65;
    padding: 48px 24px 80px;
    max-width: 820px;
    margin: 0 auto;
  }

  /* ── HEADER ── */
  .header {
    border-bottom: 1px solid var(--border-md);
    padding-bottom: 28px;
    margin-bottom: 32px;
  }
  .header-eyebrow {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 12px;
  }
  .header-name {
    font-family: var(--mono);
    font-size: 36px;
    font-weight: 700;
    color: var(--text);
    letter-spacing: -0.03em;
    line-height: 1;
    margin-bottom: 10px;
  }
  .header-role {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
    border: 1px solid var(--border-md);
    border-radius: 5px;
    padding: 4px 10px;
  }
  .dot {
    width: 6px; height: 6px; border-radius: 50%;
    background: var(--green);
    flex-shrink: 0;
  }

  /* ── SECTION HEADING ── */
  .sh {
    font-family: var(--mono);
    font-size: 9px;
    color: var(--dim);
    text-transform: uppercase;
    letter-spacing: 0.16em;
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 14px;
  }
  .sh::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }
  section { margin-bottom: 32px; }

  /* ── ABOUT ── */
  .about-text {
    font-size: 13.5px;
    color: #b0aea8;
    line-height: 1.8;
    max-width: 620px;
  }
  .about-text strong {
    color: var(--text);
    font-weight: 500;
  }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  .skill-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
  }
  .skill-card-label {
    font-family: var(--mono);
    font-size: 9px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 6px;
  }
  .skill-card-val {
    font-size: 12.5px;
    color: var(--text);
    font-weight: 500;
  }
  .skill-bar-wrap {
    margin-top: 8px;
    height: 2px;
    background: rgba(255,255,255,0.05);
    border-radius: 2px;
  }
  .skill-bar { height: 100%; border-radius: 2px; }
  .bar-red    { background: var(--red);    opacity: 0.7; }
  .bar-orange { background: var(--orange); opacity: 0.7; }
  .bar-blue   { background: var(--blue);   opacity: 0.7; }
  .bar-green  { background: var(--green);  opacity: 0.7; }
  .bar-yellow { background: var(--yellow); opacity: 0.7; }
  .bar-muted  { background: var(--muted);  opacity: 0.6; }

  /* ── ALERT ROWS (experience/stack items) ── */
  .alert-list { display: flex; flex-direction: column; gap: 8px; }
  .alert-row {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
  }
  .pill {
    font-family: var(--mono);
    font-size: 9px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    padding: 3px 8px;
    border-radius: 4px;
    flex-shrink: 0;
    margin-top: 2px;
    white-space: nowrap;
  }
  .pill-r { background: var(--red-glow);   color: #f08080; border: 1px solid var(--red-bdr); }
  .pill-g { background: var(--green-glow); color: var(--green); border: 1px solid rgba(61,186,110,0.28); }
  .pill-b { background: var(--blue-glow);  color: var(--blue);  border: 1px solid rgba(74,143,217,0.25); }
  .pill-o { background: rgba(224,130,46,0.1); color: var(--orange); border: 1px solid rgba(224,130,46,0.28); }

  .alert-main { font-size: 13px; color: var(--text); font-weight: 500; }
  .alert-sub  { font-family: var(--mono); font-size: 10px; color: var(--muted); margin-top: 2px; }

  /* ── GOAL PANEL ── */
  .goal-panel {
    background: var(--bg-card);
    border: 1px solid var(--red-bdr);
    border-left: 2px solid var(--red);
    border-radius: 8px;
    padding: 16px 18px;
  }
  .goal-label {
    font-family: var(--mono);
    font-size: 9px;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: #f08080;
    margin-bottom: 8px;
  }
  .goal-text {
    font-size: 13px;
    color: #b0aea8;
    line-height: 1.75;
  }
  .goal-text strong { color: var(--text); font-weight: 500; }

  /* ── FOOTER ── */
  .footer {
    border-top: 1px solid var(--border);
    padding-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .footer-links { display: flex; gap: 8px; }
  .footer-link {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--muted);
    border: 1px solid var(--border-md);
    border-radius: 5px;
    padding: 4px 10px;
    text-decoration: none;
  }
  .footer-link:hover { color: var(--text); }
  .footer-ts {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--dim);
  }

  @media (max-width: 580px) {
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .header-name { font-size: 26px; }
    .footer { flex-direction: column; gap: 14px; align-items: flex-start; }
  }
</style>
</head>
<body>

  <!-- HEADER -->
  <header class="header">
    <div class="header-eyebrow">// README.md</div>
    <div class="header-name">John Clyde Montaña</div>
    <div class="header-role">
      <span class="dot"></span>
      Junior SOC Analyst &nbsp;·&nbsp; Cybersecurity Enthusiast
    </div>
  </header>

  <!-- ABOUT -->
  <section>
    <div class="sh">about</div>
    <p class="about-text">
      Junior SOC Analyst focused on <strong>security monitoring</strong>, <strong>threat detection</strong>, and <strong>incident response</strong>.
      Background in <strong>DAM</strong> (Multiplatform App Development) and <strong>SMR</strong> (Systems &amp; Networks).
      Currently building skills in blue team operations, networking, and cybersecurity fundamentals —
      with a goal of growing into SOC specialization roles.
    </p>
  </section>

  <!-- SKILLS -->
  <section>
    <div class="sh">skills &amp; tools</div>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-card-label">SIEM</div>
        <div class="skill-card-val">Wazuh</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-red" style="width:75%"></div></div>
      </div>
      <div class="skill-card">
        <div class="skill-card-label">Environment</div>
        <div class="skill-card-val">Linux</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-orange" style="width:70%"></div></div>
      </div>
      <div class="skill-card">
        <div class="skill-card-label">Automation</div>
        <div class="skill-card-val">Scripting</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-blue" style="width:50%"></div></div>
      </div>
      <div class="skill-card">
        <div class="skill-card-label">Domain</div>
        <div class="skill-card-val">Networking</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-yellow" style="width:60%"></div></div>
      </div>
      <div class="skill-card">
        <div class="skill-card-label">Ops</div>
        <div class="skill-card-val">Blue Team</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-green" style="width:55%"></div></div>
      </div>
      <div class="skill-card">
        <div class="skill-card-label">Background</div>
        <div class="skill-card-val">DAM · SMR</div>
        <div class="skill-bar-wrap"><div class="skill-bar bar-muted" style="width:80%"></div></div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE / STACK -->
  <section>
    <div class="sh">focus areas</div>
    <div class="alert-list">
      <div class="alert-row">
        <span class="pill pill-r">Active</span>
        <div>
          <div class="alert-main">Security Monitoring &amp; Threat Detection</div>
          <div class="alert-sub">Incident response · Log analysis · Alert triage</div>
        </div>
      </div>
      <div class="alert-row">
        <span class="pill pill-g">Running</span>
        <div>
          <div class="alert-main">SIEM Operations — Wazuh</div>
          <div class="alert-sub">Rule tuning · Linux agent deployment · Event correlation</div>
        </div>
      </div>
      <div class="alert-row">
        <span class="pill pill-b">Learning</span>
        <div>
          <div class="alert-main">Blue Team &amp; Network Fundamentals</div>
          <div class="alert-sub">SOC workflows · Packet analysis · Threat intel basics</div>
        </div>
      </div>
      <div class="alert-row">
        <span class="pill pill-o">Stack</span>
        <div>
          <div class="alert-main">Scripting &amp; Basic Automation</div>
          <div class="alert-sub">Bash · Python basics · Task automation in Linux environments</div>
        </div>
      </div>
    </div>
  </section>

  <!-- GOAL -->
  <section>
    <div class="sh">objective</div>
    <div class="goal-panel">
      <div class="goal-label">// current_target</div>
      <div class="goal-text">
        Aiming to grow in <strong>SOC operations</strong> and advance into
        <strong>cybersecurity specialization roles</strong>. Building a solid foundation
        in blue team practices, threat hunting, and security tooling to move
        toward a long-term career in defensive security.
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="footer-links">
      <a class="footer-link" href="#">LinkedIn</a>
      <a class="footer-link" href="#">GitHub</a>
      <a class="footer-link" href="#">TryHackMe</a>
    </div>
    <div class="footer-ts">Last updated: 2026-06-10</div>
  </footer>

</body>
</html>
