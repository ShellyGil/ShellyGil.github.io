<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>My Site</title>
  <meta name="description" content="Personal website" />
  <style>
    /* ===== Easy theme knobs ===== */
    :root{
      --bg: #0f172a;          /* page background */
      --text: #e5e7eb;        /* primary text */
      --muted: #94a3b8;       /* secondary text */
      --card: #111827;        /* card background */
      --brand: #22d3ee;       /* accent color */
      --brand-2: #a78bfa;     /* secondary accent */
      --radius: 18px;         /* card/button rounding */
      --maxw: 960px;          /* content width */
    }

    /* ===== Base ===== */
    * { box-sizing: border-box; }
    html, body { margin:0; padding:0; }
    body {
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, Inter, Arial, sans-serif;
      line-height: 1.6; color: var(--text); background: radial-gradient(1200px 800px at 80% -10%, rgba(34,211,238,.15), transparent 60%), radial-gradient(800px 600px at -10% 20%, rgba(167,139,250,.12), transparent 60%), var(--bg);
    }
    a { color: var(--brand); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .container { max-width: var(--maxw); margin: 0 auto; padding: 24px; }

    /* ===== Top nav ===== */
    .nav { position: sticky; top: 0; backdrop-filter: blur(8px); background: rgba(15,23,42,.6); border-bottom: 1px solid rgba(255,255,255,.06); z-index: 20; }
    .nav .inner { display:flex; align-items:center; justify-content: space-between; gap: 12px; padding: 12px 24px; max-width: var(--maxw); margin: 0 auto; }
    .brand { font-weight: 800; letter-spacing: .2px; }
    .menu { display:flex; gap: 18px; }
    .menu a { color: var(--muted); font-weight: 600; }
    .menu a:hover { color: var(--text); }

    /* ===== Hero ===== */
    .hero { padding: 72px 24px 40px; text-align: center; }
    .hero h1 { font-size: clamp(32px, 6vw, 54px); line-height:1.1; margin: 0 0 12px; }
    .hero p { color: var(--muted); margin: 0 auto 22px; max-width: 700px; }
    .cta { display:inline-flex; gap:12px; flex-wrap: wrap; justify-content:center; }
    .btn { background: linear-gradient(135deg, var(--brand), var(--brand-2)); color:#0b1020; font-weight:800; padding: 12px 18px; border-radius: var(--radius); border: none; box-shadow: 0 10px 20px rgba(34,211,238,.15), 0 4px 10px rgba(167,139,250,.12); }
    .btn.secondary { background: transparent; color: var(--text); border:1px solid rgba(255,255,255,.12); }

    /* ===== Sections ===== */
    section { padding: 40px 0; }
    h2 { font-size: clamp(24px, 4.5vw, 34px); margin: 0 0 18px; }
    .grid { display:grid; grid-template-columns: repeat(12, 1fr); gap: 18px; }
    .card { grid-column: span 12; background: rgba(17,24,39,.8); border: 1px solid rgba(255,255,255,.06); border-radius: var(--radius); padding: 18px; }
    .card h3 { margin: 0 0 8px; font-size: 20px; }
    .card p { color: var(--muted); margin: 0 0 12px; }
    @media (min-width: 720px) {
      .card { grid-column: span 4; }
    }

    /* ===== Footer ===== */
    footer { border-top: 1px solid rgba(255,255,255,.06); color: var(--muted); }

    /* ===== Utilities ===== */
    .pill { display:inline-block; padding:4px 10px; border-radius: 999px; background: rgba(255,255,255,.06); color: var(--muted); font-size: 12px; font-weight:700; letter-spacing:.3px; }
  </style>
</head>
<body>
  <!-- Top nav -->
  <nav class="nav">
    <div class="inner">
      <div class="brand">My Site</div>
      <div class="menu">
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <header class="hero container">
    <span class="pill">Welcome</span>
    <h1>Hi, I'm <span style="color:var(--brand)">Your Name</span>.</h1>
    <p>A short one-liner about who you are and what you do. Keep it friendly and clear. You can edit everything in this single file.</p>
    <div class="cta">
      <a class="btn" href="#projects">See my work</a>
      <a class="btn secondary" href="#contact">Contact me</a>
    </div>
  </header>

  <!-- Projects -->
  <section id="projects" class="container">
    <h2>Projects</h2>
    <div class="grid">
      <article class="card">
        <h3>Project One</h3>
        <p>Describe what it is, why it matters, and your role. Add a link below.</p>
        <a href="#">View project →</a>
      </article>
      <article class="card">
        <h3>Project Two</h3>
        <p>Another quick description. Keep it 1–2 sentences. You can paste images inside cards if you like.</p>
        <a href="#">View project →</a>
      </article>
      <article class="card">
        <h3>Project Three</h3>
        <p>Short blurb goes here. If you have more than 3 projects, duplicate a card.</p>
        <a href="#">View project →</a>
      </article>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="container">
    <h2>About</h2>
    <div class="card" style="padding:24px">
      <p>Write 3–5 sentences about you: what you do, tools you use, and what you're looking for. You can include <strong>bold</strong> text and <a href="#">links</a>.</p>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="container">
    <h2>Contact</h2>
    <div class="card" style="padding:24px">
      <p>Email: <a href="mailto:you@example.com">you@example.com</a><br>
      GitHub: <a href="https://github.com/yourusername" target="_blank" rel="noreferrer">@yourusername</a>
      </p>
    </div>
  </section>

  <footer class="container">
    <p>© <span id="year"></span> Your Name · Built with GitHub Pages</p>
  </footer>

  <script>
    // set year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>



