<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>My Site</title>
  <meta name="description" content="Personal website" />
  <style>
    :root{
      --bg: #0f172a;
      --text: #e5e7eb;
      --muted: #94a3b8;
      --card: #111827;
      --brand: #22d3ee;
      --brand-2: #a78bfa;
      --radius: 18px;
      --maxw: 960px;
    }

    * { box-sizing: border-box; }
    html, body { margin:0; padding:0; }
    body {
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, Inter, Arial, sans-serif;
      line-height: 1.6; color: var(--text); background: radial-gradient(1200px 800px at 80% -10%, rgba(34,211,238,.15), transparent 60%), radial-gradient(800px 600px at -10% 20%, rgba(167,139,250,.12), transparent 60%), var(--bg);
    }
    a { color: var(--brand); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .container { max-width: var(--maxw); margin: 0 auto; padding: 24px; }

    .nav { position: sticky; top: 0; backdrop-filter: blur(8px); background: rgba(15,23,42,.6); border-bottom: 1px solid rgba(255,255,255,.06); z-index: 20; }
    .nav .inner { display:flex; align-items:center; justify-content: space-between; gap: 12px; padding: 12px 24px; max-width: var(--maxw); margin: 0 auto; }
    .brand { font-weight: 800; letter-spacing: .2px; }
    .menu { display:flex; gap: 18px; }
    .menu a { color: var(--muted); font-weight: 600; }
    .menu a:hover { color: var(--text); }

    .hero { padding: 72px 24px 40px; text-align: center; position: relative; }
    .hero h1 { font-size: clamp(32px, 6vw, 54px); line-height:1.1; margin: 0 0 12px; }
    .hero p { color: var(--muted); margin: 0 auto 22px; max-width: 700px; }
    .profile-pic {
      position: absolute;
      top: 20px;
      right: 20px;
      width: 130px;
      height: 130px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid var(--brand);
      box-shadow: 0 0 12px rgba(34,211,238,.4);
    }

    section { padding: 40px 0; }
    h2 { font-size: clamp(24px, 4.5vw, 34px); margin: 0 0 18px; }
    .grid { display:grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 18px; }
    .card { background: rgba(17,24,39,.8); border: 1px solid rgba(255,255,255,.06); border-radius: var(--radius); padding: 18px; }
    .card h3 { margin: 0 0 8px; font-size: 20px; }
    .card p { color: var(--muted); margin: 0 0 12px; }

    footer { border-top: 1px solid rgba(255,255,255,.06); color: var(--muted); }
    .pill { display:inline-block; padding:4px 10px; border-radius: 999px; background: rgba(255,255,255,.06); color: var(--muted); font-size: 12px; font-weight:700; letter-spacing:.3px; }
  </style>
</head>
<body>
  <nav class="nav">
    <div class="inner">
      <div class="brand">My Site</div>
      <div class="menu">
        <a href="#projects">Rotations</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <header class="hero container">
    <img src="1a8961bc-7b4a-4b35-9a63-f5b158c621d4.JPG" alt="Profile picture" class="profile-pic" />
    <span class="pill">Welcome</span>
    <h1>Hi, I'm <span style="color:var(--brand)">Shelly!</span></h1>
    <p>A graduate student at the WSoS in the Molecular and Cellular Neuroscience track.</p>
  </header>

  <section id="projects" class="container">
    <h2>Rotations</h2>
    <div class="grid">
      <article class="card">
        <h3>Rotation One</h3>
        <p>For my first rotation in <a href="https://www.yaron-lab.com/" target="_blank" rel="noreferrer">Yaron's Lab</a>, I'll be working on DRG sensory neurons hyperinnervation under inflammation.</p>
      </article>

      <article class="card">
        <h3>Rotation Two</h3>
        <p>For my next rotation in <a href="https://www.weizmann.ac.il/molgen/hornstein/home/" target="_blank" rel="noreferrer">Hornstein's Lab</a>, I'll be working on genes related to ALS.</p>
      </article>

      <article class="card">
        <h3>Rotation Three</h3>
        <p>I haven't selected my last one yet, so suggestions are very welcome!</p>
      </article>
    </div>
  </section>

  <section id="about" class="container">
    <h2>About</h2>
    <div class="card" style="padding:24px">
      <p>As you probably already know, my name is Shelly. In my free time I like to play the flute, since I played with the Israeli Youth Philharmonic Orchestra and completed 15 Bagrut points in music studies. I finished my undergraduate at the Hebrew University, majoring in neuoroscience. During the past two years I worked in <a href="https://medneuro.huji.ac.il/lab-sites/joshua-a-goldberg/" target="_blank" rel="noreferrer">Goldberg's Lab</a>, where I studied Parkinson's Disease on mice. Recently I started my graduate studies at the Weizmann Institute and am hoping that someday I'll be able to code in Python for any lab project that I might need, without having to rely on anyone!</p>
    </div>
  </section>

  <section id="contact" class="container">
    <h2>Contact</h2>
    <div class="card" style="padding:24px">
      <p>Email: <a href="mailto:shelly.gilad@weizmann.ac.il">shelly.gilad@weizmann.ac.il</a><br>
      GitHub: <a href="https://github.com/shellygil" target="_blank" rel="noreferrer">@shellygil</a></p>
    </div>
  </section>

  <footer class="container">
    <p>© <span id="year"></span> Shelly Gilad · Built with GitHub Pages</p>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
