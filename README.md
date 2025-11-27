<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Mostafa Eid — Machine Learning & Software</title>
  <meta name="description" content="Mostafa Eid — M.Sc. Computer Science. Machine learning for biomedical data, federated learning, reproducible code and clear write-ups."/>
  <link rel="icon" href="/favicon.ico">
  <!-- Open Graph / social previews -->
  <meta property="og:title" content="Mostafa Eid — Machine Learning & Software" />
  <meta property="og:description" content="Machine learning for biomedical data. Projects, skills, and contact." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://mostafa772.github.io/portfolio/" />
  <meta property="og:image" content="/og-image.png" />

  <style>
    /* Minimal, modern CSS. Customize colors below. */
    :root{
      --bg: #0f1724; /* dark navy */
      --card: #0b1220;
      --muted: #99a0b3;
      --accent: #6ee7b7; /* mint */
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.02);
      --radius: 12px;
      --max-width: 1100px;
      --ff-sans: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--ff-sans);
      background:linear-gradient(180deg,var(--bg),#071022 140%);
      color:#e6eef6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      padding:32px 16px;
      display:flex;justify-content:center;
    }
    .site{width:100%;max-width:var(--max-width)}
    header{
      display:flex;align-items:center;justify-content:space-between;margin-bottom:28px;
    }
    .brand{display:flex;gap:16px;align-items:center}
    .me-circle{width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,#0b1430, #10203a);display:flex;align-items:center;justify-content:center;font-weight:700}
    .brand h1{margin:0;font-size:18px}
    nav{display:flex;gap:12px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;padding:8px 12px;border-radius:8px}
    nav a.cta{background:var(--accent);color:#06221a;font-weight:600}
    .hero{display:grid;grid-template-columns:1fr 320px;gap:24px;align-items:center;margin-bottom:28px}
    .hero .intro h2{margin:0 0 12px 0;font-size:28px}
    .hero .intro p{margin:0;color:var(--muted)}
    .skills{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
    .pill{background:var(--glass);padding:6px 10px;border-radius:999px;color:var(--muted);font-size:13px}

    /* Projects grid */
    .controls{display:flex;gap:8px;align-items:center;margin:18px 0}
    .search{flex:1}
    input[type=search]{width:100%;padding:10px;border-radius:10px;border:1px solid var(--glass-2);background:transparent;color:inherit}
    .filters{display:flex;gap:8px}
    .btn{padding:8px 12px;border-radius:10px;background:var(--glass);border:1px solid var(--glass-2);cursor:pointer;color:var(--muted)}

    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:14px;border-radius:var(--radius);border:1px solid rgba(255,255,255,0.03);display:flex;flex-direction:column;gap:12px}
    .card img{width:100%;height:160px;object-fit:cover;border-radius:8px}
    .card h3{margin:0;font-size:16px}
    .card p{margin:0;color:var(--muted);font-size:13px}
    .card .meta{display:flex;justify-content:space-between;align-items:center}
    .tags{display:flex;gap:6px;flex-wrap:wrap}
    .tag{font-size:12px;padding:6px;border-radius:8px;background:var(--glass);color:var(--muted)}

    footer{margin-top:36px;color:var(--muted);font-size:13px}

    /* Modal */
    .modal-backdrop{position:fixed;inset:0;background:rgba(2,6,12,0.6);display:none;align-items:center;justify-content:center;padding:20px}
    .modal{background:linear-gradient(180deg,#071021,#071026);max-width:900px;width:100%;padding:18px;border-radius:16px}
    .modal .grid{grid-template-columns:1fr 360px}

    /* small screens */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr}
      .grid{grid-template-columns:repeat(2,1fr)}
      .modal .grid{grid-template-columns:1fr}
    }
    @media (max-width:600px){
      .grid{grid-template-columns:1fr}
      header{flex-direction:column;align-items:flex-start;gap:12px}
    }

    /* subtle animations */
    .card{transition:transform .18s ease, box-shadow .18s ease}
    .card:hover{transform:translateY(-6px);box-shadow:0 10px 30px rgba(2,8,20,0.6)}
  </style>
</head>
<body>
  <div class="site" id="site">
    <header>
      <div class="brand">
        <div class="me-circle">ME</div>
        <div>
          <h1>Mostafa Eid</h1>
          <div style="color:var(--muted);font-size:13px;">M.Sc. Computer Science — University of Pisa</div>
        </div>
      </div>
      <nav aria-label="Main navigation">
        <a href="#projects">Projects</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
        <a class="cta" href="assets/documents/Mostafa_Eid_CV.pdf" target="_blank" rel="noopener noreferrer">View CV</a>
      </nav>
    </header>

    <section class="hero" aria-labelledby="intro">
      <div class="intro">
        <h2 id="intro">Machine Learning, Federated Learning, and Reliable Systems</h2>
        <p>I’m Mostafa, a Computer Science graduate student building robust machine learning tools for biomedical data — reproducible code, clear write-ups, and production-ready experiments.</p>
        <div class="skills" id="skills">
          <span class="pill">Python</span>
          <span class="pill">PyTorch</span>
          <span class="pill">TensorFlow</span>
          <span class="pill">Docker</span>
          <span class="pill">Flask</span>
          <span class="pill">SQL</span>
        </div>

      </div>
      <aside>
        <div style="background:var(--card);padding:8px;border-radius:12px;border:1px solid rgba(255,255,255,0.03)">
          <h4 style="margin:0 0 8px 0">Contacts</h4>
          <p style="margin:0;color:var(--muted);font-size:14px">mostafa2222.me@gmail.com</p>
          <div style="display:flex;gap:8px;margin-top:12px">
            <a class="btn" href="https://github.com/mostafa772">GitHub</a>
            <a class="btn" href="https://www.linkedin.com/in/mostafa-eid772/">LinkedIn</a>
            <a class="btn" href="https://www.kaggle.com/mostafa772">Kaggle</a>
          </div>
        </div>
      </aside>

    </section>

    <section id="projects">
      <div class="controls">
        <div class="search"><input type="search" id="q" placeholder="Search projects, e.g. federated learning, EEG..."></div>
        <div class="filters" role="tablist" aria-label="Filter projects">
          <button class="btn" data-filter="*">All</button>
          <button class="btn" data-filter="ml">ML</button>
          <button class="btn" data-filter="bio">Bio</button>
          <button class="btn" data-filter="sys">Systems</button>
        </div>
      </div>

      <div class="grid" id="grid">
        <!-- Example project cards: replace titles/images/descriptions with your own -->
        <article class="card" data-tags="ml bio">
          <img loading="lazy" src="/assets/projects/eeg-thumb.jpg" alt="EEG classification project screenshot">
          <h3>EEG classification with Federated Learning</h3>
          <p>Thesis work: decentralized training across hospitals with privacy-preserving aggregation.</p>
          <div class="meta">
            <div class="tags"><span class="tag">PyTorch</span><span class="tag">Federated</span></div>
            <div><button class="btn" data-open>Details</button></div>
          </div>
        </article>

        <article class="card" data-tags="ml sys">
          <img loading="lazy" src="/assets/projects/rl-thumb.jpg" alt="RL agent visualisation">
          <h3>NetHack RL agent</h3>
          <p>Reinforcement learning agent trained on NetHack with distributed replay and curriculum learning.</p>
          <div class="meta">
            <div class="tags"><span class="tag">Gymnasium</span><span class="tag">RL</span></div>
            <div><button class="btn" data-open>Details</button></div>
          </div>
        </article>
        
        <article class="card" data-tags="ml sys">
          <img loading="lazy" src="/assets/projects/rl-thumb.jpg" alt="RL agent visualisation">
          <h3>NetHack RL agent</h3>
          <p>Reinforcement learning agent trained on NetHack with distributed replay and curriculum learning.</p>
          <div class="meta">
            <div class="tags"><span class="tag">Gymnasium</span><span class="tag">RL</span></div>
            <div><button class="btn" data-open>Details</button></div>
          </div>
        </article>

        <article class="card" data-tags="bio ml">
          <img loading="lazy" src="/assets/projects/scrna-thumb.jpg" alt="scRNA-seq analysis">
          <h3>Comparative scRNA-seq Analysis</h3>
          <p>Integrated PBMC datasets across autoimmune diseases to find disease-specific signatures.</p>
          <div class="meta">
            <div class="tags"><span class="tag">Scanpy</span><span class="tag">XAI</span></div>
            <div><button class="btn" data-open>Details</button></div>
          </div>
        </article>

        <!-- add more cards... -->
      </div>
    </section>

    <!-- Modal template -->
    <div class="modal-backdrop" id="backdrop" role="dialog" aria-modal="true" aria-hidden="true">
      <div class="modal" role="document">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
          <h3 id="modal-title">Project title</h3>
          <button class="btn" id="close">Close</button>
        </div>
        <div class="grid">
          <div>
            <img id="modal-image" src="/assets/projects/eeg-thumb.jpg" alt="screenshot" style="width:100%;height:320px;object-fit:cover;border-radius:8px;margin-bottom:12px">
            <p id="modal-desc" style="color:var(--muted)"></p>
            <p style="margin-top:12px"><a id="modal-git" class="btn" href="#">View on GitHub</a></p>
          </div>
          <aside style="padding-left:12px">
            <h4>Details</h4>
            <ul id="modal-meta" style="color:var(--muted)"></ul>
          </aside>
        </div>
      </div>
    </div>

    <footer id="contact">
      <div>Mostafa Eid · Master's Student — University of Pisa</div>
      <div style="margin-top:8px;color:var(--muted)">mostafa2222.me@gmail.com</a></div>
    </footer>
  </div>

  <script>
    // Lightweight JS: filtering, search, modal
    const grid = document.getElementById('grid');
    const cards = Array.from(grid.querySelectorAll('.card'));
    const q = document.getElementById('q');
    const filters = document.querySelectorAll('[data-filter]');

    function applyFilter(tag){
      const term = q.value.trim().toLowerCase();
      cards.forEach(c=>{
        const tags = c.dataset.tags || '';
        const matchesTag = (tag === '*' || tags.includes(tag));
        const text = (c.innerText || '').toLowerCase();
        const matchesText = !term || text.includes(term);
        c.style.display = (matchesTag && matchesText) ? '' : 'none';
      })
    }

    filters.forEach(b=>b.addEventListener('click',()=>applyFilter(b.dataset.filter)));
    q.addEventListener('input',()=>applyFilter('*'));

    // Modal logic
    const backdrop = document.getElementById('backdrop');
    const modalTitle = document.getElementById('modal-title');
    const modalDesc = document.getElementById('modal-desc');
    const modalImage = document.getElementById('modal-image');
    const modalMeta = document.getElementById('modal-meta');
    const modalGit = document.getElementById('modal-git');
    document.querySelectorAll('[data-open]').forEach((btn,i)=>{
      btn.addEventListener('click', (ev)=>{
        const card = ev.target.closest('.card');
        modalTitle.textContent = card.querySelector('h3').textContent;
        modalDesc.textContent = card.querySelector('p').textContent;
        modalImage.src = card.querySelector('img').src;
        modalImage.alt = card.querySelector('img').alt;
        // metadata (tags)
        modalMeta.innerHTML = '';
        card.querySelectorAll('.tag').forEach(t=>{
          const li = document.createElement('li'); li.textContent = t.textContent; modalMeta.appendChild(li);
        });
        modalGit.href = '#';
        backdrop.style.display = 'flex';
        backdrop.setAttribute('aria-hidden','false');
      })
    })
    document.getElementById('close').addEventListener('click',()=>{
      backdrop.style.display='none';backdrop.setAttribute('aria-hidden','true');
    })
    backdrop.addEventListener('click',(e)=>{ if(e.target===backdrop){ backdrop.style.display='none'; backdrop.setAttribute('aria-hidden','true'); } })

    // small accessibility: keyboard close
    document.addEventListener('keydown',(e)=>{ if(e.key==='Escape'){ backdrop.style.display='none'; backdrop.setAttribute('aria-hidden','true'); } })

    // progressive enhancement: mutate cards from existing HTML easily
  </script>
</body>
</html>