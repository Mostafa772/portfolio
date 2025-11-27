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
    :root{--bg:#0f1724;--card:#0b1220;--muted:#94a3b8;--accent:#6ee7b7;--glass: rgba(255,255,255,0.04);--maxw:1100px;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial}
    *{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;background:linear-gradient(180deg,#071028 0%,var(--bg) 100%);color:#e6eef6;line-height:1.45}
    .wrap{max-width:var(--maxw);margin:36px auto;padding:20px}
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

    /* Projects area now dynamic */
    .projects-wrap{margin-top:18px}
    .projects-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}

    /* Project card with hover screenshot reveal */
    .proj{position:relative;overflow:visible;padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), transparent);border:1px solid rgba(255,255,255,0.02);cursor:pointer}
    .proj h3{margin:0 0 6px 0;font-size:16px}
    .proj p{margin:0;color:var(--muted);font-size:14px}
    .proj .meta{margin-top:10px;font-size:13px;color:var(--muted)}

    /* Screenshot preview */
    .screenshot-wrap{position:absolute;right:-12px;top:-12px;width:320px;height:200px;border-radius:10px;overflow:hidden;box-shadow:0 12px 40px rgba(2,6,23,0.6);transform-origin:left top;z-index:20;pointer-events:none;opacity:0;transform:translateY(6px) scale(.98);transition:all .22s cubic-bezier(.2,.9,.3,1)}
    .screenshot{width:100%;height:100%;object-fit:cover;display:block}
    .proj:hover .screenshot-wrap{opacity:1;transform:translateY(0) scale(1)}

    /* small badge for tech */
    .tags{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}
    .tag{background:rgba(255,255,255,0.02);padding:6px 8px;border-radius:8px;font-size:12px;color:var(--muted);border:1px solid rgba(255,255,255,0.02)}

    aside .card{position:sticky;top:24px}
    footer{margin-top:36px;padding:18px;text-align:center;color:var(--muted);font-size:14px}

    /* responsive */
    @media (max-width:980px){.hero{grid-template-columns:1fr;}.projects-grid{grid-template-columns:repeat(2,1fr)}.avatar{width:48px;height:48px}.screenshot-wrap{display:none}}
    @media (max-width:640px){.projects-grid{grid-template-columns:1fr}.nav-hide{display:none}}

    /* subtle hover */
    .proj:hover{transform:translateY(-6px);transition:transform .18s ease, box-shadow .18s ease}
    .btn-ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:inherit;padding:8px 10px;border-radius:8px}

    /* small utilities */
    .muted-block{color:var(--muted);font-size:14px}
    .controls{display:flex;gap:8px;align-items:center}
    .edit-note{margin-top:10px;color:var(--muted);font-size:13px}
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
        <p class="muted">I’m a Computer Science graduate currently pursuing a Master's at the University of Pisa. I focus on machine learning for biomedical data, producing reproducible code and clear write-ups.</p>

        <div class="projects-wrap" id="projects">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <h4 style="margin:8px 0 6px 0">Featured projects</h4>
            <div class="controls">
              <button id="toggle-images" class="btn-ghost">Toggle screenshots</button>
            </div>
          </div>

          <div class="projects-grid" id="projects-grid" aria-live="polite">
            <!-- Projects are rendered here from JS -->
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
          <div style="margin-top:12px"><a class="btn" href="https://www.linkedin.com">LinkedIn</a> <a class="btn" href="https://github.com/Mostafa772">GitHub</a></div>
        </div>
 <!-- style="margin-top:14px" -->
        <div class="card">
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

  <script>
    /* -----------------------------
       PROJECTS DATA (edit here)
       ----------------------------- */
    const projects = [
      {
        id: 'nn-scratch',
        title: 'Neural Network From Scratch',
        description: 'A pure NumPy implementation of a feed-forward neural network to learn backpropagation from first principles.',
        tech: ['Python','NumPy'],
        image: 'assets/nn-scratch.png',
        url: 'https://github.com/Mostafa772/nn-from-scratch'
      },
      {
        id: 'seismic-py',
        title: 'Seismic.py Library',
        description: 'Re-implemented Rust seismic routines into a modular Python API for ML integration and analysis.',
        tech: ['Python','API'],
        image: 'assets/seismic.png',
        url: 'https://github.com/Mostafa772/seismic'
      },
      {
        id: 'nyc-jobs',
        title: 'NYC Jobs Analyzer',
        description: 'Full-stack analytics app with a REST API ingesting NYC Open Data, containerized with Docker.',
        tech: ['Flask','Docker','SQLAlchemy'],
        image: 'assets/nyc-jobs.png',
        url: 'https://github.com/Mostafa772/nyc-jobs-analyzer'
      }
    ];

    /* -----------------------------
       RENDERING & INTERACTIONS
       ----------------------------- */
    const grid = document.getElementById('projects-grid');
    const toggleBtn = document.getElementById('toggle-images');
    let screenshotsEnabled = true;

    function createProjectCard(p){
      const card = document.createElement('article');
      card.className = 'proj card';
      card.setAttribute('tabindex','0');
      card.setAttribute('role','button');
      card.onclick = () => { if(p.url) window.open(p.url,'_blank') };
      card.onkeypress = (e) => { if(e.key === 'Enter') card.click() };

      const title = document.createElement('h3'); title.textContent = p.title;
      const desc = document.createElement('p'); desc.textContent = p.description;
      const meta = document.createElement('div'); meta.className = 'meta muted-block'; meta.textContent = p.url ? new URL(p.url).hostname.replace('www.','') : '';

      const tags = document.createElement('div'); tags.className = 'tags';
      (p.tech||[]).forEach(t=>{ const sp = document.createElement('div'); sp.className='tag'; sp.textContent = t; tags.appendChild(sp)});

      // screenshot wrapper (hover reveal)
      const shotWrap = document.createElement('div'); shotWrap.className='screenshot-wrap';
      const img = document.createElement('img'); img.className='screenshot';
      img.alt = p.title + ' screenshot';
      // graceful fallback: if image path not present, show generated svg data URL
      if(p.image){
        img.src = p.image;
        img.onerror = ()=>{ img.src = generatePlaceholder(p.title) };
      } else img.src = generatePlaceholder(p.title);
      shotWrap.appendChild(img);

      card.appendChild(title);
      card.appendChild(desc);
      card.appendChild(tags);
      card.appendChild(meta);
      card.appendChild(shotWrap);
      return card;
    }

    function generatePlaceholder(text){
      const w=800,h=500;
      const svg = `<svg xmlns='http://www.w3.org/2000/svg' width='${w}' height='${h}'><rect width='100%' height='100%' fill='#0b1220'/><text x='50%' y='50%' fill='#6ee7b7' font-family='Inter,Arial' font-size='34' text-anchor='middle' dominant-baseline='middle'>${escapeHtml(text)}</text></svg>`;
      return 'data:image/svg+xml;base64,' + btoa(svg);
    }

    function escapeHtml(s){ return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

    function renderProjects(){
      grid.innerHTML = '';
      projects.forEach(p => grid.appendChild(createProjectCard(p)));
    }

    toggleBtn.addEventListener('click', ()=>{
      screenshotsEnabled = !screenshotsEnabled;
      document.querySelectorAll('.screenshot-wrap').forEach(w=> w.style.display = screenshotsEnabled ? 'block' : 'none');
      toggleBtn.textContent = screenshotsEnabled ? 'Hide screenshots' : 'Show screenshots';
    });

    // initial render
    renderProjects();

    // accessibility: when focusing a card with keyboard, also reveal screenshot
    document.addEventListener('focusin', (e)=>{
      const card = e.target.closest('.proj');
      document.querySelectorAll('.screenshot-wrap').forEach(w=> w.style.opacity = 0);
      if(card){ const sw = card.querySelector('.screenshot-wrap'); if(sw) sw.style.opacity = 1; }
    });

    // expose projects to window for easy editing from the browser devtools
    window.__projects = projects;

    /* Helpful tip: you can edit the `projects` array above or open browser console and modify `window.__projects` then call renderProjects() to see changes live. */
  </script>
</body>
</html>
