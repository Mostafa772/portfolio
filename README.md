<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Mostafa Eid — Machine Learning & Software</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  <meta name="description" content="Mostafa Eid — Master's Student in Computer Science. Machine Learning, Federated Learning, Full-stack projects." />
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#94a3b8; --accent:#6ee7b7; --glass: rgba(255,255,255,0.04);
      --maxw:1100px; font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:linear-gradient(180deg,#071028 0%,var(--bg) 100%);color:#e6eef6;line-height:1.5}
    .wrap{max-width:var(--maxw);margin:40px auto;padding:24px}

    header{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;gap:14px;align-items:center}
    .avatar{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#60a5fa);display:flex;align-items:center;justify-content:center;font-weight:700;color:#042029}
    .brand h1{margin:0;font-size:18px}
    nav{display:flex;gap:12px;align-items:center}
    a.btn{background:var(--glass);padding:8px 12px;border-radius:8px;text-decoration:none;color:var(--accent);font-weight:600;border:1px solid rgba(255,255,255,0.04)}

    .hero{display:grid;grid-template-columns:1fr 360px;gap:28px;margin-top:28px;align-items:start}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:14px;padding:22px;border:1px solid rgba(255,255,255,0.03)}
    .hero-left h2{margin:0 0 8px 0;font-size:32px}
    .muted{color:var(--muted)}
    .skills{display:flex;flex-wrap:wrap;gap:8px;margin-top:12px}
    .pill{background:rgba(255,255,255,0.03);padding:6px 10px;border-radius:999px;font-size:13px;color:var(--muted);border:1px solid rgba(255,255,255,0.02)}

    .projects-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:18px}
    .proj{padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), transparent);border:1px solid rgba(255,255,255,0.02)}
    .proj h3{margin:0 0 6px 0;font-size:16px}
    .proj p{margin:0;color:var(--muted);font-size:14px}
    .proj .meta{margin-top:10px;font-size:13px;color:var(--muted)}

    aside .card{position:sticky;top:24px}

    footer{margin-top:36px;padding:18px;text-align:center;color:var(--muted);font-size:14px}

    /* responsive */
    @media (max-width:980px){.hero{grid-template-columns:1fr;}.projects-grid{grid-template-columns:repeat(2,1fr)}.avatar{width:48px;height:48px}}
    @media (max-width:640px){.projects-grid{grid-template-columns:1fr}.nav-hide{display:none}}

    /* subtle hover */
    .proj:hover{transform:translateY(-6px);transition:transform .18s ease, box-shadow .18s ease;box-shadow:0 10px 30px rgba(2,6,23,0.6)}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:inherit;padding:8px 10px;border-radius:8px}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="avatar">ME</div>
        <div>
          <h1>Mostafa Eid</h1>
          <div class="muted">M.Sc. Computer Science — University of Pisa</div>
        </div>
      </div>
      <nav>
        <a class="btn" href="#projects">Projects</a>
        <a class="btn" href="#skills">Skills</a>
        <a class="btn" href="#contact">Contact</a>
        <a class="btn-ghost nav-hide" href="cv.md">View CV</a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-left card">
        <h2>Machine Learning, Federated Learning, and Reliable systems</h2>
        <p class="muted">I’m a Computer Science graduate (MIPT) currently pursuing a Master's at the University of Pisa. I focus on machine learning for biomedical data, producing reproducible code and clear write-ups.</p>

        <div style="margin-top:18px">
          <h4 style="margin:0 0 6px 0">Featured projects</h4>
          <div class="projects-grid" id="projects">
            <article class="proj">
              <h3>Neural Network From Scratch</h3>
              <p>A pure NumPy implementation of a feed-forward neural network to learn backpropagation from first principles.</p>
              <div class="meta">Tech: Python, NumPy · Result: 99% on MONK1</div>
            </article>

            <article class="proj">
              <h3>Seismic.py Library</h3>
              <p>Re-implemented Rust seismic routines into a modular Python API for ML integration and analysis.</p>
              <div class="meta">Tech: Python · API design</div>
            </article>

            <article class="proj">
              <h3>NYC Jobs Analyzer</h3>
              <p>Full-stack analytics app with a REST API ingesting NYC Open Data, containerized with Docker.</p>
              <div class="meta">Tech: Flask, Docker, SQLAlchemy</div>
            </article>
          </div>
        </div>

        <section id="skills" style="margin-top:18px">
          <h4 style="margin:0 0 8px 0">Skills</h4>
          <div class="skills">
            <span class="pill">Python</span>
            <span class="pill">PyTorch</span>
            <span class="pill">TensorFlow</span>
            <span class="pill">NumPy</span>
            <span class="pill">Docker</span>
            <span class="pill">Flask</span>
            <span class="pill">SQL</span>
          </div>
        </section>

      </div>

      <aside>
        <div class="card">
          <h4 style="margin-top:0">About</h4>
          <p class="muted">Master's Student in Computer Science @ University of Pisa. Thesis: Classification of EEG Data With Federated Learning.</p>
          <div style="margin-top:12px"><a class="btn" href="https://www.linkedin.com">LinkedIn</a> <a class="btn" href="https://github.com/Mostafa772/portfolio">GitHub</a></div>
        </div>

        <div class="card" style="margin-top:14px">
          <h4 style="margin-top:0">Contact</h4>
          <p class="muted">Prefer email for professional inquiries. Or link your contact form here.</p>
          <div style="margin-top:8px"><a class="btn" href="#contact">Say hello</a></div>
        </div>
      </aside>
    </section>

    <footer id="contact">
      <div style="margin-bottom:8px">Mostafa Eid · Master's Student — University of Pisa</div>
      <div class="muted">Quick links: <a href="cv.md" style="color:var(--accent);text-decoration:none">View CV</a> · <a href="https://github.com/Mostafa772" style="color:var(--accent);text-decoration:none">GitHub</a></div>
    </footer>
  </div>
</body>
</html>
