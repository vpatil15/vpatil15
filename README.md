<title>Vaishnavi Patil</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&family=DM+Mono:wght@400;500&display=swap">

<style>
  :root {
    --bg: #F5F7FA;
    --surface: #FFFFFF;
    --border: #DDE3EC;
    --text: #0D1829;
    --muted: #6B7A96;
    --accent: #2B6CB0;
    --accent-soft: #E8F0FB;
    --tag-bg: #EDF2F7;
    --tag-text: #334E74;
    --divider: #E2E8F0;
    --code-bg: #EFF3F9;
  }

  @media (prefers-color-scheme: dark) {
    :root:not([data-theme="light"]) {
      --bg: #0C1220;
      --surface: #141D30;
      --border: #1E2D46;
      --text: #E2EAF4;
      --muted: #7A90AF;
      --accent: #5A9FD4;
      --accent-soft: #0F1E35;
      --tag-bg: #1A2840;
      --tag-text: #8BB4D8;
      --divider: #1C2D44;
      --code-bg: #111C2E;
    }
  }

  :root[data-theme="dark"] {
    --bg: #0C1220;
    --surface: #141D30;
    --border: #1E2D46;
    --text: #E2EAF4;
    --muted: #7A90AF;
    --accent: #5A9FD4;
    --accent-soft: #0F1E35;
    --tag-bg: #1A2840;
    --tag-text: #8BB4D8;
    --divider: #1C2D44;
    --code-bg: #111C2E;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', system-ui, sans-serif;
    font-size: 15px;
    line-height: 1.7;
    min-height: 100vh;
    padding: 40px 20px 80px;
    transition: background 0.2s, color 0.2s;
  }

  .page {
    max-width: 660px;
    margin: 0 auto;
  }

  /* Header */
  .header {
    padding-bottom: 28px;
    border-bottom: 1px solid var(--divider);
    margin-bottom: 36px;
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 2.4rem;
    letter-spacing: -0.02em;
    color: var(--text);
    text-wrap: balance;
    line-height: 1.1;
    margin-bottom: 10px;
  }

  .tagline {
    font-size: 0.95rem;
    font-weight: 500;
    color: var(--accent);
    letter-spacing: 0.01em;
    margin-bottom: 12px;
  }

  .bio {
    font-size: 0.95rem;
    color: var(--muted);
    font-weight: 300;
    max-width: 56ch;
    line-height: 1.65;
  }

  /* Sections */
  .section {
    margin-bottom: 36px;
  }

  .section-label {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 14px;
  }

  /* Experience */
  .exp-row {
    display: flex;
    align-items: baseline;
    gap: 10px;
    padding: 8px 0;
    border-bottom: 1px solid var(--divider);
  }

  .exp-row:last-child { border-bottom: none; }

  .exp-title {
    font-weight: 500;
    font-size: 0.93rem;
    color: var(--text);
    flex: 1;
  }

  .exp-company {
    color: var(--muted);
    font-size: 0.88rem;
    font-weight: 300;
  }

  .exp-date {
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    color: var(--muted);
    white-space: nowrap;
    opacity: 0.75;
  }

  /* Tech stack */
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
  }

  .tag {
    background: var(--tag-bg);
    color: var(--tag-text);
    font-family: 'DM Mono', monospace;
    font-size: 0.78rem;
    padding: 4px 10px;
    border-radius: 4px;
    letter-spacing: 0.01em;
  }

  .tag-group {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .tag-row {
    display: flex;
    align-items: flex-start;
    gap: 14px;
  }

  .cat-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
    white-space: nowrap;
    padding-top: 5px;
    min-width: 90px;
    letter-spacing: 0.01em;
    opacity: 0.8;
  }

  /* Projects */
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px 20px;
    margin-bottom: 10px;
    transition: border-color 0.15s;
  }

  .project-card:last-child { margin-bottom: 0; }
  .project-card:hover { border-color: var(--accent); }

  .project-name {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 1rem;
    color: var(--text);
    margin-bottom: 5px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .project-name a {
    color: inherit;
    text-decoration: none;
    border-bottom: 1.5px solid var(--border);
    padding-bottom: 1px;
    transition: border-color 0.15s;
  }

  .project-name a:hover { border-color: var(--accent); color: var(--accent); }

  .project-desc {
    font-size: 0.88rem;
    color: var(--muted);
    font-weight: 300;
    line-height: 1.6;
    margin-bottom: 10px;
  }

  .project-stack {
    font-family: 'DM Mono', monospace;
    font-size: 0.73rem;
    color: var(--muted);
    opacity: 0.75;
  }

  /* Connect */
  .links {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    color: var(--accent);
    text-decoration: none;
    font-size: 0.9rem;
    font-weight: 500;
    padding: 7px 14px;
    border: 1px solid var(--accent);
    border-radius: 5px;
    transition: background 0.15s, color 0.15s;
    opacity: 0.85;
  }

  .link:hover {
    background: var(--accent-soft);
    opacity: 1;
  }

  /* Raw markdown toggle */
  .raw-toggle {
    margin-top: 44px;
    padding-top: 24px;
    border-top: 1px solid var(--divider);
  }

  .raw-toggle summary {
    font-family: 'Syne', sans-serif;
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    cursor: pointer;
    user-select: none;
    margin-bottom: 14px;
  }

  .raw-toggle summary:hover { color: var(--text); }

  .raw-toggle summary::marker { content: ''; }

  .raw-block {
    background: var(--code-bg);
    border: 1px solid var(--border);
    border-radius: 7px;
    padding: 20px;
    font-family: 'DM Mono', monospace;
    font-size: 0.8rem;
    line-height: 1.75;
    color: var(--text);
    white-space: pre-wrap;
    word-break: break-word;
    margin-top: 12px;
    overflow-x: auto;
  }
</style>

<div class="page">

  <header class="header">
    <h1 class="name">Vaishnavi Patil</h1>
    <p class="tagline">MS Computer Science · Santa Clara University · San Francisco, CA</p>
    <p class="bio">Software engineer with 4 years of industry experience building distributed backend systems and APIs. Focused on backend systems, distributed systems, and applied ML.</p>
  </header>

  <section class="section">
    <div class="section-label">Experience</div>
    <div class="exp-row">
      <span class="exp-title">Teaching Assistant – Advanced OS <span class="exp-company">· Santa Clara University</span></span>
      <span class="exp-date">Sep–Dec 2025</span>
    </div>
    <div class="exp-row">
      <span class="exp-title">Software Development Engineer II <span class="exp-company">· Tata Consultancy Services</span></span>
      <span class="exp-date">2023 – 2025</span>
    </div>
    <div class="exp-row">
      <span class="exp-title">Software Development Engineer I <span class="exp-company">· Tata Consultancy Services</span></span>
      <span class="exp-date">2021 – 2023</span>
    </div>
  </section>

  <section class="section">
    <div class="section-label">Tech Stack</div>
    <div class="tag-group">
      <div class="tag-row">
        <span class="cat-label">Languages</span>
        <div class="tags">
          <span class="tag">Python</span>
          <span class="tag">Java</span>
          <span class="tag">Golang</span>
          <span class="tag">C</span>
          <span class="tag">C++</span>
        </div>
      </div>
      <div class="tag-row">
        <span class="cat-label">Databases</span>
        <div class="tags">
          <span class="tag">PostgreSQL</span>
          <span class="tag">MongoDB</span>
          <span class="tag">DynamoDB</span>
          <span class="tag">Redis</span>
          <span class="tag">SQL</span>
          <span class="tag">Elasticsearch</span>
        </div>
      </div>
      <div class="tag-row">
        <span class="cat-label">Cloud &amp; DevOps</span>
        <div class="tags">
          <span class="tag">AWS</span>
          <span class="tag">Docker</span>
          <span class="tag">Kubernetes</span>
          <span class="tag">Jenkins</span>
          <span class="tag">Git</span>
          <span class="tag">Grafana</span>
          <span class="tag">Looker</span>
        </div>
      </div>
      <div class="tag-row">
        <span class="cat-label">Frameworks</span>
        <div class="tags">
          <span class="tag">Spring Boot</span>
          <span class="tag">React</span>
          <span class="tag">Node.js</span>
          <span class="tag">FastAPI</span>
          <span class="tag">Flask</span>
        </div>
      </div>
      <div class="tag-row">
        <span class="cat-label">Practices</span>
        <div class="tags">
          <span class="tag">Agile</span>
          <span class="tag">CI/CD</span>
          <span class="tag">DevOps</span>
          <span class="tag">Scrum</span>
        </div>
      </div>
    </div>
  </section>

  <section class="section">
    <div class="section-label">Projects</div>
    <div class="project-card">
      <div class="project-name">
        <a href="https://github.com/vpatil15">ChatGPT-X</a>
      </div>
      <p class="project-desc">Full-stack conversational AI with multi-modal input processing and dynamic RAG. Achieved 90% test coverage with OAuth 2.0 and GDPR-compliant auth.</p>
      <div class="project-stack">MongoDB · Express · React · Node.js · TypeScript · OpenAI API</div>
    </div>
    <div class="project-card">
      <div class="project-name">
        <a href="https://github.com/vpatil15">PawsConnect</a>
      </div>
      <p class="project-desc">Social media app for pets with real-time content sharing and Google OAuth. Improved app performance 15% through Redux state optimization.</p>
      <div class="project-stack">React · Redux · Firebase · JavaScript</div>
    </div>
  </section>

  <section class="section">
    <div class="section-label">Connect</div>
    <div class="links">
      <a class="link" href="https://www.linkedin.com/in/vaishnavipatil390/">LinkedIn</a>
      <a class="link" href="https://vpatil15.github.io/Portfolio/">Portfolio</a>
      <a class="link" href="mailto:vaishnavipatil390@gmail.com">Email</a>
    </div>
  </section>

  <details class="raw-toggle">
    <summary>▸ Raw Markdown — copy to GitHub</summary>
    <div class="raw-block"># Vaishnavi Patil

**MS Computer Science and Engineering @ Santa Clara University** · San Francisco, CA

Software engineer with 4 years of industry experience building distributed backend systems and APIs. Currently focused on distributed systems, Agentic AI, and backend engineering.


---

## Tech Stack

| | |
|---|---|
| **Languages** | `Python` `Java` `Golang` `C` `C++` |
| **Databases** | `PostgreSQL` `MongoDB` `DynamoDB` `Redis` `SQL` `Elasticsearch` |
| **Cloud & DevOps** | `AWS` `Docker` `Kubernetes` `Jenkins` `Git` `Grafana` `Looker` |
| **Frameworks** | `Spring Boot` `React` `Node.js` `FastAPI` `Flask` |
| **Practices** | `Agile` `CI/CD` `DevOps` `Scrum` |
---

## Connect

[LinkedIn](https://www.linkedin.com/in/vaishnavipatil390/) · [Portfolio](https://vpatil15.github.io/Portfolio/) · vaishnavipatil390@gmail.com</div>
  </details>

</div>
