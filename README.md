# -AI-ML-Engineer-Roadmap-From-What-is-to-Senior
From absolute zero → Senior AI/ML Engineer — the most depth you'll find

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>AI/ML Senior Roadmap</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:system-ui,sans-serif;background:#0f1117;color:#e2e8f0;min-height:100vh}
:root{--accent:#6366f1;--accent2:#8b5cf6;--green:#10b981;--amber:#f59e0b;--red:#ef4444;--blue:#3b82f6;--cyan:#06b6d4;--pink:#ec4899;--bg:#0f1117;--bg2:#161b27;--bg3:#1e2535;--bg4:#252d3d;--border:#2d3748;--text:#e2e8f0;--muted:#94a3b8;--radius:10px}
.header{background:linear-gradient(135deg,#1a1f36 0%,#0f1117 50%,#1a1f36 100%);border-bottom:1px solid var(--border);padding:2rem;text-align:center;position:relative;overflow:hidden}
.header::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--accent),var(--cyan),var(--pink),var(--green));animation:shimmer 3s linear infinite;background-size:200%}
@keyframes shimmer{0%{background-position:0%}100%{background-position:200%}}
.header h1{font-size:2rem;font-weight:700;background:linear-gradient(135deg,#a5b4fc,#67e8f9,#f9a8d4);-webkit-background-clip:text;-webkit-text-fill-color:transparent;letter-spacing:-0.5px}
.header p{color:var(--muted);margin-top:.5rem;font-size:.95rem}
.stats-bar{display:flex;gap:1rem;justify-content:center;margin-top:1.5rem;flex-wrap:wrap}
.stat{background:var(--bg3);border:1px solid var(--border);border-radius:8px;padding:.5rem 1.2rem;font-size:.8rem;color:var(--muted)}
.stat span{color:var(--text);font-weight:600;font-size:.95rem;display:block}
.nav{display:flex;gap:.4rem;padding:1rem 1.5rem;background:var(--bg2);border-bottom:1px solid var(--border);overflow-x:auto;flex-wrap:nowrap;position:sticky;top:0;z-index:50}
.nav-btn{padding:.45rem 1rem;border:1px solid var(--border);border-radius:6px;background:transparent;color:var(--muted);cursor:pointer;font-size:.8rem;white-space:nowrap;transition:all .2s}
.nav-btn:hover,.nav-btn.active{background:var(--accent);border-color:var(--accent);color:#fff}
.main{max-width:1100px;margin:0 auto;padding:2rem 1rem}
.phase{display:none}
.phase.active{display:block}
.phase-header{display:flex;align-items:flex-start;gap:1.5rem;margin-bottom:2rem;padding:1.5rem;background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius)}
.phase-num{width:60px;height:60px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.4rem;font-weight:700;flex-shrink:0;border:2px solid}
.phase-info h2{font-size:1.4rem;font-weight:600;margin-bottom:.3rem}
.phase-info p{color:var(--muted);font-size:.9rem;line-height:1.6}
.phase-meta{display:flex;gap:1rem;margin-top:.8rem;flex-wrap:wrap}
.badge{padding:.25rem .75rem;border-radius:20px;font-size:.75rem;font-weight:500}
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-bottom:1.5rem}
.grid3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1.2rem;margin-bottom:1.5rem}
@media(max-width:720px){.grid2,.grid3{grid-template-columns:1fr}}
.card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.2rem}
.card h3{font-size:.95rem;font-weight:600;margin-bottom:1rem;display:flex;align-items:center;gap:.5rem}
.card h3 .icon{width:24px;height:24px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-size:14px}
ul.skill-list{list-style:none}
ul.skill-list li{padding:.35rem 0;border-bottom:1px solid var(--border);font-size:.85rem;color:var(--muted);display:flex;align-items:center;gap:.5rem}
ul.skill-list li:last-child{border-bottom:none}
ul.skill-list li::before{content:'→';color:var(--accent);font-size:.8rem;flex-shrink:0}
.project-card{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.2rem;margin-bottom:1rem}
.project-header{display:flex;align-items:flex-start;justify-content:space-between;gap:1rem;margin-bottom:.7rem}
.project-title{font-weight:600;font-size:.95rem}
.diff-badge{padding:.2rem .6rem;border-radius:4px;font-size:.7rem;font-weight:600}
.diff-easy{background:#0d2e1f;color:#10b981;border:1px solid #10b981}
.diff-med{background:#2d1f0a;color:#f59e0b;border:1px solid #f59e0b}
.diff-hard{background:#2d0f0f;color:#ef4444;border:1px solid #ef4444}
.diff-sr{background:#1f0d2d;color:#a855f7;border:1px solid #a855f7}
.project-desc{font-size:.83rem;color:var(--muted);line-height:1.6;margin-bottom:.8rem}
.project-tags{display:flex;gap:.4rem;flex-wrap:wrap}
.tag{padding:.15rem .55rem;background:var(--bg4);border:1px solid var(--border);border-radius:4px;font-size:.72rem;color:var(--muted)}
.tools-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:.7rem;margin-bottom:1.5rem}
.tool-item{background:var(--bg3);border:1px solid var(--border);border-radius:8px;padding:.7rem;text-align:center;font-size:.8rem}
.tool-icon{font-size:1.5rem;margin-bottom:.3rem}
.tool-name{font-weight:500;color:var(--text)}
.tool-cat{font-size:.7rem;color:var(--muted)}
.timeline{position:relative;padding-left:2rem}
.timeline::before{content:'';position:absolute;left:.5rem;top:0;bottom:0;width:2px;background:var(--border)}
.tl-item{position:relative;margin-bottom:1.5rem}
.tl-item::before{content:'';position:absolute;left:-1.7rem;top:.3rem;width:10px;height:10px;border-radius:50%;background:var(--accent);border:2px solid var(--bg)}
.tl-week{font-size:.75rem;color:var(--accent);font-weight:600;margin-bottom:.2rem}
.tl-task{font-size:.85rem;color:var(--text);margin-bottom:.2rem;font-weight:500}
.tl-sub{font-size:.8rem;color:var(--muted);line-height:1.5}
.resources-list{list-style:none}
.resources-list li{display:flex;align-items:flex-start;gap:.75rem;padding:.6rem 0;border-bottom:1px solid var(--border);font-size:.85rem}
.resources-list li:last-child{border-bottom:none}
.res-type{padding:.15rem .5rem;border-radius:4px;font-size:.7rem;font-weight:600;flex-shrink:0;margin-top:.1rem}
.res-course{background:#0d2031;color:#3b82f6;border:1px solid #3b82f6}
.res-book{background:#2d1f0a;color:#f59e0b;border:1px solid #f59e0b}
.res-paper{background:#1f0d2d;color:#a855f7;border:1px solid #a855f7}
.res-video{background:#2d0f0f;color:#ef4444;border:1px solid #ef4444}
.res-practice{background:#0d2e1f;color:#10b981;border:1px solid #10b981}
.accordion{margin-bottom:.7rem}
.acc-header{padding:.8rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:8px;cursor:pointer;display:flex;justify-content:space-between;align-items:center;font-size:.9rem;font-weight:500;user-select:none}
.acc-header:hover{border-color:var(--accent)}
.acc-header .arrow{transition:transform .2s;font-size:.8rem}
.acc-body{display:none;padding:1rem;background:var(--bg2);border:1px solid var(--border);border-top:none;border-radius:0 0 8px 8px;font-size:.85rem;color:var(--muted);line-height:1.7}
.acc-body.open{display:block}
.senior-req{background:linear-gradient(135deg,#1a1230,#0f1117);border:1px solid #6366f1;border-radius:var(--radius);padding:1.5rem;margin-bottom:1.5rem}
.senior-req h3{color:#a5b4fc;font-size:1rem;margin-bottom:.8rem}
.req-grid{display:grid;grid-template-columns:1fr 1fr;gap:.5rem}
@media(max-width:600px){.req-grid{grid-template-columns:1fr}}
.req-item{display:flex;gap:.5rem;align-items:flex-start;font-size:.83rem;color:var(--muted)}
.req-item::before{content:'✦';color:#6366f1;flex-shrink:0;font-size:.7rem;margin-top:.2rem}
.salary-table{width:100%;border-collapse:collapse;font-size:.85rem;margin-top:.5rem}
.salary-table th{padding:.6rem .8rem;background:var(--bg4);text-align:left;font-weight:500;border-bottom:1px solid var(--border);color:var(--muted);font-size:.78rem}
.salary-table td{padding:.6rem .8rem;border-bottom:1px solid var(--border);color:var(--text)}
.salary-table tr:last-child td{border-bottom:none}
.interview-section{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;margin-bottom:1.5rem}
.interview-section h3{font-size:1rem;font-weight:600;margin-bottom:1rem;color:var(--text)}
.q-item{padding:.6rem 0;border-bottom:1px solid var(--border);font-size:.85rem}
.q-item:last-child{border-bottom:none}
.q-cat{font-size:.7rem;color:var(--accent);font-weight:600;margin-bottom:.2rem}
.progress-bar{height:6px;background:var(--bg4);border-radius:3px;margin-top:.5rem;overflow:hidden}
.progress-fill{height:100%;border-radius:3px;transition:width .5s}
.checklist{list-style:none}
.checklist li{padding:.4rem 0;border-bottom:1px solid var(--border);font-size:.85rem;display:flex;gap:.6rem;align-items:flex-start}
.checklist li:last-child{border-bottom:none}
.chk{width:16px;height:16px;border-radius:3px;border:1px solid var(--border);flex-shrink:0;margin-top:.1rem;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:.7rem;transition:all .2s}
.chk.checked{background:var(--green);border-color:var(--green);color:#fff}
.section-title{font-size:1.1rem;font-weight:600;margin:2rem 0 1rem;color:var(--text);border-left:3px solid var(--accent);padding-left:.75rem}
.math-grid{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1.5rem}
@media(max-width:600px){.math-grid{grid-template-columns:1fr}}
.math-card{background:var(--bg3);border:1px solid var(--border);border-radius:8px;padding:1rem}
.math-card h4{font-size:.85rem;font-weight:600;margin-bottom:.6rem;color:var(--accent)}
.math-topics{font-size:.82rem;color:var(--muted);line-height:1.8}
.arch-box{background:var(--bg3);border:1px solid var(--border);border-radius:8px;padding:1rem;margin-bottom:.8rem}
.arch-box h4{font-size:.85rem;font-weight:600;margin-bottom:.5rem}
.arch-desc{font-size:.8rem;color:var(--muted);line-height:1.5;margin-bottom:.5rem}
.arch-apps{display:flex;gap:.3rem;flex-wrap:wrap}
.app-tag{padding:.1rem .45rem;background:#1a1f36;border:1px solid #6366f1;border-radius:4px;font-size:.7rem;color:#a5b4fc}
.warning-box{background:#2d1a0a;border:1px solid #f59e0b;border-radius:8px;padding:1rem;margin-bottom:1rem;font-size:.85rem;color:#fbbf24;display:flex;gap:.6rem}
.tip-box{background:#0a2d1f;border:1px solid #10b981;border-radius:8px;padding:1rem;margin-bottom:1rem;font-size:.85rem;color:#34d399;display:flex;gap:.6rem}
.xp-meter{display:flex;gap:.3rem;margin-top:.5rem}
.xp-dot{width:8px;height:8px;border-radius:50%}
.phase0-clr{background:#f59e0b;border-color:#f59e0b}
.phase1-clr{background:#10b981;border-color:#10b981}
.phase2-clr{background:#3b82f6;border-color:#3b82f6}
.phase3-clr{background:#8b5cf6;border-color:#8b5cf6}
.phase4-clr{background:#ec4899;border-color:#ec4899}
.phase5-clr{background:#ef4444;border-color:#ef4444}
.phase6-clr{background:#06b6d4;border-color:#06b6d4}
.roadmap-overview{background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;margin-bottom:2rem}
.ov-steps{display:flex;flex-direction:column;gap:.5rem}
.ov-step{display:flex;align-items:center;gap:1rem;padding:.6rem .8rem;border-radius:8px;cursor:pointer;transition:all .2s;border:1px solid transparent}
.ov-step:hover{background:var(--bg3);border-color:var(--border)}
.ov-dot{width:12px;height:12px;border-radius:50%;flex-shrink:0}
.ov-step-name{font-size:.9rem;font-weight:500;flex:1}
.ov-step-time{font-size:.78rem;color:var(--muted)}
.ov-step-lvl{font-size:.72rem;padding:.15rem .5rem;border-radius:4px;background:var(--bg4)}
.connector{width:2px;height:20px;background:var(--border);margin-left:5px}
</style>
</head>
<body>
<div class="header">
  <h1>🧠 AI / ML Engineer Roadmap</h1>
  <p>From absolute zero → Senior AI/ML Engineer — the most depth you'll find</p>
  <div class="stats-bar">
    <div class="stat"><span>18–24 mo</span>Timeline</div>
    <div class="stat"><span>7 Phases</span>Structured Path</div>
    <div class="stat"><span>40+</span>Projects</div>
    <div class="stat"><span>100+</span>Topics Covered</div>
    <div class="stat"><span>$120k–$350k+</span>Senior Salary</div>
  </div>
</div>

<div class="nav">
  <button class="nav-btn active" onclick="switchPhase(0)">🗺️ Overview</button>
  <button class="nav-btn" onclick="switchPhase(1)">📐 Phase 0: Prerequisites</button>
  <button class="nav-btn" onclick="switchPhase(2)">🐍 Phase 1: ML Foundations</button>
  <button class="nav-btn" onclick="switchPhase(3)">⚙️ Phase 2: Core ML</button>
  <button class="nav-btn" onclick="switchPhase(4)">🧠 Phase 3: Deep Learning</button>
  <button class="nav-btn" onclick="switchPhase(5)">🚀 Phase 4: Advanced AI</button>
  <button class="nav-btn" onclick="switchPhase(6)">🏗️ Phase 5: MLOps & Systems</button>
  <button class="nav-btn" onclick="switchPhase(7)">👑 Phase 6: Senior Level</button>
  <button class="nav-btn" onclick="switchPhase(8)">💼 Interview Prep</button>
</div>

<div class="main">

<!-- OVERVIEW -->
<div class="phase active" id="phase-0">
  <div class="roadmap-overview">
    <div class="section-title" style="margin-top:0">Your Journey at a Glance</div>
    <div class="ov-steps">
      <div class="ov-step" onclick="switchPhase(1)">
        <div class="ov-dot" style="background:#f59e0b"></div>
        <div class="ov-step-name">Phase 0 — Math, Statistics & Python</div>
        <div class="ov-step-time">Months 1–2</div>
        <div class="ov-step-lvl" style="color:#f59e0b">Foundation</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(2)">
        <div class="ov-dot" style="background:#10b981"></div>
        <div class="ov-step-name">Phase 1 — ML Foundations & Data Science</div>
        <div class="ov-step-time">Months 2–4</div>
        <div class="ov-step-lvl" style="color:#10b981">Beginner</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(3)">
        <div class="ov-dot" style="background:#3b82f6"></div>
        <div class="ov-step-name">Phase 2 — Core ML Algorithms & Feature Engineering</div>
        <div class="ov-step-time">Months 4–7</div>
        <div class="ov-step-lvl" style="color:#3b82f6">Intermediate</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(4)">
        <div class="ov-dot" style="background:#8b5cf6"></div>
        <div class="ov-step-name">Phase 3 — Deep Learning & Neural Networks</div>
        <div class="ov-step-time">Months 7–11</div>
        <div class="ov-step-lvl" style="color:#8b5cf6">Advanced</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(5)">
        <div class="ov-dot" style="background:#ec4899"></div>
        <div class="ov-step-name">Phase 4 — Advanced AI: NLP, CV, RL, LLMs</div>
        <div class="ov-step-time">Months 11–16</div>
        <div class="ov-step-lvl" style="color:#ec4899">Specialist</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(6)">
        <div class="ov-dot" style="background:#ef4444"></div>
        <div class="ov-step-name">Phase 5 — MLOps, Systems Design & Production</div>
        <div class="ov-step-time">Months 16–20</div>
        <div class="ov-step-lvl" style="color:#ef4444">Production</div>
      </div>
      <div class="connector"></div>
      <div class="ov-step" onclick="switchPhase(7)">
        <div class="ov-dot" style="background:#06b6d4"></div>
        <div class="ov-step-name">Phase 6 — Senior Skills: Research, Leadership, Architecture</div>
        <div class="ov-step-time">Months 20–24</div>
        <div class="ov-step-lvl" style="color:#06b6d4">Senior</div>
      </div>
    </div>
  </div>

  <div class="section-title">What Makes a Senior AI/ML Engineer?</div>
  <div class="grid2">
    <div class="card">
      <h3><span class="icon" style="background:#1a1f36">🧪</span> Technical Depth</h3>
      <ul class="skill-list">
        <li>Deep understanding of algorithms, not just API calls</li>
        <li>Ability to implement ML from scratch (math → code)</li>
        <li>Diagnose model failures and debug training instabilities</li>
        <li>Design large-scale ML architectures</li>
        <li>Read and implement research papers</li>
        <li>Know when NOT to use ML</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#0d2031">🏗️</span> Production Skills</h3>
      <ul class="skill-list">
        <li>Build ML pipelines that serve millions of requests</li>
        <li>Monitor, retrain, and maintain live models</li>
        <li>A/B testing and experimentation frameworks</li>
        <li>Data versioning, model versioning, experiment tracking</li>
        <li>Latency optimization, model compression, deployment</li>
        <li>Cost optimization at scale</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#1f0d2d">📊</span> Business Impact</h3>
      <ul class="skill-list">
        <li>Translate business problems into ML problems</li>
        <li>Define the right metrics (not just accuracy)</li>
        <li>Communicate results to non-technical stakeholders</li>
        <li>Estimate ROI of ML projects</li>
        <li>Know when a rule-based system beats ML</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#0a2d1f">👨‍💼</span> Leadership</h3>
      <ul class="skill-list">
        <li>Mentor junior engineers and review their ML work</li>
        <li>Lead ML project planning and estimation</li>
        <li>Drive technical decisions on ML infrastructure</li>
        <li>Collaborate with data engineers, PMs, researchers</li>
        <li>Contribute to open source or internal tooling</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Core Technology Stack (Senior)</div>
  <div class="tools-grid">
    <div class="tool-item"><div class="tool-icon">🐍</div><div class="tool-name">Python</div><div class="tool-cat">Primary Language</div></div>
    <div class="tool-item"><div class="tool-icon">🔥</div><div class="tool-name">PyTorch</div><div class="tool-cat">Deep Learning</div></div>
    <div class="tool-item"><div class="tool-icon">🤗</div><div class="tool-name">HuggingFace</div><div class="tool-cat">NLP / LLMs</div></div>
    <div class="tool-item"><div class="tool-icon">⚡</div><div class="tool-name">Ray / Spark</div><div class="tool-cat">Distributed</div></div>
    <div class="tool-item"><div class="tool-icon">🐳</div><div class="tool-name">Docker/K8s</div><div class="tool-cat">Deployment</div></div>
    <div class="tool-item"><div class="tool-icon">📊</div><div class="tool-name">MLflow/W&B</div><div class="tool-cat">Experiment Track</div></div>
    <div class="tool-item"><div class="tool-icon">☁️</div><div class="tool-name">AWS/GCP/Azure</div><div class="tool-cat">Cloud ML</div></div>
    <div class="tool-item"><div class="tool-icon">🗄️</div><div class="tool-name">SQL + NoSQL</div><div class="tool-cat">Data Storage</div></div>
    <div class="tool-item"><div class="tool-icon">📈</div><div class="tool-name">Grafana/Prom</div><div class="tool-cat">Monitoring</div></div>
    <div class="tool-item"><div class="tool-icon">🦀</div><div class="tool-name">Rust/C++</div><div class="tool-cat">Performance</div></div>
    <div class="tool-item"><div class="tool-icon">🔁</div><div class="tool-name">Airflow/Prefect</div><div class="tool-cat">Orchestration</div></div>
    <div class="tool-item"><div class="tool-icon">🧪</div><div class="tool-name">pytest + CI/CD</div><div class="tool-cat">Engineering</div></div>
  </div>

  <div class="tip-box">💡 <div><strong>Key Insight:</strong> Most people learn ML but few can deploy it. The gap between a mid-level and senior engineer is production experience — building systems that are reliable, scalable, and maintainable, not just notebooks with good accuracy.</div></div>
</div>

<!-- PHASE 0 -->
<div class="phase" id="phase-1">
  <div class="phase-header">
    <div class="phase-num phase0-clr" style="color:#451a03">P0</div>
    <div class="phase-info">
      <h2>Phase 0 — Prerequisites: Math, Statistics & Python</h2>
      <p>This is the non-negotiable foundation. Skip this and you'll be cargo-cult coding — copying models without understanding why they work. Senior engineers can derive the math, not just call fit().</p>
      <div class="phase-meta">
        <span class="badge" style="background:#2d1f0a;color:#f59e0b;border:1px solid #f59e0b">⏱ Months 1–2</span>
        <span class="badge" style="background:#2d1f0a;color:#f59e0b;border:1px solid #f59e0b">📚 Pre-ML Foundation</span>
      </div>
    </div>
  </div>

  <div class="section-title">Mathematics You Must Know</div>
  <div class="math-grid">
    <div class="math-card">
      <h4>Linear Algebra</h4>
      <div class="math-topics">
        Vectors, matrices, tensors<br>
        Matrix multiplication, transpose<br>
        Dot product, cross product<br>
        Eigenvalues & eigenvectors<br>
        Singular Value Decomposition (SVD)<br>
        Principal Component Analysis (PCA)<br>
        Norms: L1, L2, Frobenius<br>
        Rank, null space, column space<br>
        Determinants, inverse matrices
      </div>
    </div>
    <div class="math-card">
      <h4>Calculus & Optimization</h4>
      <div class="math-topics">
        Derivatives, partial derivatives<br>
        Chain rule (critical for backprop)<br>
        Gradient, Jacobian, Hessian<br>
        Optimization: minima/maxima<br>
        Gradient descent (manual derivation)<br>
        Lagrange multipliers<br>
        Taylor series expansion<br>
        Integral calculus (basics)<br>
        Multivariate calculus
      </div>
    </div>
    <div class="math-card">
      <h4>Probability & Statistics</h4>
      <div class="math-topics">
        Probability distributions (Gaussian, Bernoulli, etc.)<br>
        Bayes theorem — derive it by hand<br>
        Expectation, variance, covariance<br>
        Central Limit Theorem<br>
        Hypothesis testing, p-values<br>
        Maximum Likelihood Estimation<br>
        Markov chains, Monte Carlo<br>
        KL divergence, entropy<br>
        Confidence intervals
      </div>
    </div>
    <div class="math-card">
      <h4>Information Theory</h4>
      <div class="math-topics">
        Entropy, cross-entropy (why it's used as loss)<br>
        Mutual information<br>
        KL divergence<br>
        Jensen-Shannon divergence<br>
        Bits vs nats<br>
        Information gain (used in decision trees)<br>
        Channel capacity<br>
        Bits, coding theory basics
      </div>
    </div>
  </div>

  <div class="section-title">Python Mastery</div>
  <div class="grid3">
    <div class="card">
      <h3>Core Python</h3>
      <ul class="skill-list">
        <li>Data types, comprehensions, generators</li>
        <li>OOP: classes, inheritance, magic methods</li>
        <li>Decorators, context managers</li>
        <li>Type hints (mypy)</li>
        <li>Error handling, logging</li>
        <li>Async/await, concurrency</li>
        <li>Memory management, profiling</li>
        <li>Virtual envs, pip, poetry</li>
      </ul>
    </div>
    <div class="card">
      <h3>Scientific Python</h3>
      <ul class="skill-list">
        <li>NumPy — vectorized ops, broadcasting</li>
        <li>Pandas — DataFrames, groupby, merge</li>
        <li>Matplotlib & Seaborn — EDA plots</li>
        <li>SciPy — scientific computing</li>
        <li>Jupyter notebooks + lab</li>
        <li>Polars (modern fast DataFrames)</li>
        <li>Dask — parallel DataFrames</li>
      </ul>
    </div>
    <div class="card">
      <h3>Software Engineering</h3>
      <ul class="skill-list">
        <li>Git — branching, PRs, rebasing</li>
        <li>Clean code, SOLID principles</li>
        <li>Unit testing with pytest</li>
        <li>Documentation (docstrings, Sphinx)</li>
        <li>Code review skills</li>
        <li>CI/CD pipelines</li>
        <li>Packaging Python libraries</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Phase 0 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🔢 NumPy from Scratch — Implement Linear Algebra Ops</span>
      <span class="diff-badge diff-easy">Beginner</span>
    </div>
    <div class="project-desc">Build your own mini-numpy: matrix multiply, transpose, eigenvalue decomposition using only pure Python lists. This forces you to understand exactly what's happening under the hood and why broadcasting rules exist.</div>
    <div class="project-tags"><span class="tag">Python</span><span class="tag">Linear Algebra</span><span class="tag">From Scratch</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📊 Stats Dashboard — Exploratory Data Analysis (EDA)</span>
      <span class="diff-badge diff-easy">Beginner</span>
    </div>
    <div class="project-desc">Pick any real dataset (Kaggle: Titanic, House Prices, etc.). Do a full EDA: distributions, correlations, outlier detection, hypothesis tests. Write a detailed Jupyter notebook with every statistical finding explained.</div>
    <div class="project-tags"><span class="tag">Pandas</span><span class="tag">Statistics</span><span class="tag">Matplotlib</span><span class="tag">Kaggle</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🧮 Gradient Descent Visualizer</span>
      <span class="diff-badge diff-easy">Beginner</span>
    </div>
    <div class="project-desc">Implement gradient descent (batch, stochastic, mini-batch) from pure Python/NumPy. Visualize loss curves, learning rate effects, saddle points and local minima using Matplotlib animations.</div>
    <div class="project-tags"><span class="tag">Calculus</span><span class="tag">NumPy</span><span class="tag">Visualization</span><span class="tag">Optimization</span></div>
  </div>

  <div class="section-title">Resources</div>
  <div class="card">
    <ul class="resources-list">
      <li><span class="res-type res-book">Book</span><div><strong>Mathematics for Machine Learning</strong> — Deisenroth, Faisal, Ong (free PDF online) — THE book, covers linear algebra, calculus, prob theory</div></li>
      <li><span class="res-type res-course">Course</span><div><strong>3Blue1Brown: Essence of Linear Algebra</strong> — YouTube playlist. The best visual intuition builder. Watch before any textbook.</div></li>
      <li><span class="res-type res-course">Course</span><div><strong>Khan Academy Statistics</strong> — Free, complete probability and statistics track. Do all exercises.</div></li>
      <li><span class="res-type res-course">Course</span><div><strong>Python for Everybody (Dr. Chuck, Coursera)</strong> — Best structured Python intro. Or "Fluent Python" book for advanced.</div></li>
      <li><span class="res-type res-book">Book</span><div><strong>Think Stats / Think Bayes</strong> — Allen Downey. Statistics with code — perfect bridge between math and ML.</div></li>
      <li><span class="res-type res-practice">Practice</span><div><strong>LeetCode Easy/Medium</strong> — Solve 50+ Python problems. Data structures knowledge is expected in ML interviews.</div></li>
    </ul>
  </div>
</div>

<!-- PHASE 1 -->
<div class="phase" id="phase-2">
  <div class="phase-header">
    <div class="phase-num phase1-clr" style="color:#052e16">P1</div>
    <div class="phase-info">
      <h2>Phase 1 — ML Foundations & Data Science</h2>
      <p>Learn the core workflow: data → features → model → evaluation. Understand how ML actually works, the bias-variance tradeoff, overfitting/underfitting, and how to properly evaluate models.</p>
      <div class="phase-meta">
        <span class="badge" style="background:#0d2e1f;color:#10b981;border:1px solid #10b981">⏱ Months 2–4</span>
        <span class="badge" style="background:#0d2e1f;color:#10b981;border:1px solid #10b981">🌱 Beginner</span>
      </div>
    </div>
  </div>

  <div class="grid2">
    <div class="card">
      <h3><span class="icon" style="background:#0d2e1f">📉</span> Core ML Concepts</h3>
      <ul class="skill-list">
        <li>Supervised vs Unsupervised vs Reinforcement Learning</li>
        <li>Bias-variance tradeoff — derive mathematically</li>
        <li>Overfitting vs underfitting — detect and fix</li>
        <li>Train/validation/test split — why & how</li>
        <li>Cross-validation: K-fold, stratified, time-series</li>
        <li>Regularization: L1 (Lasso), L2 (Ridge), ElasticNet</li>
        <li>Loss functions: MSE, MAE, cross-entropy, Huber</li>
        <li>Hyperparameter tuning: grid search, random search, Bayesian</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#0d2e1f">📊</span> Model Evaluation</h3>
      <ul class="skill-list">
        <li>Classification: accuracy, precision, recall, F1, ROC-AUC</li>
        <li>Regression: RMSE, MAE, MAPE, R²</li>
        <li>Confusion matrix — interpret every cell</li>
        <li>When to use precision vs recall (class imbalance)</li>
        <li>PR curves vs ROC curves</li>
        <li>Statistical significance testing for models</li>
        <li>Calibration of probability outputs</li>
        <li>Learning curves — diagnose bias vs variance</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#0d2e1f">🔧</span> Feature Engineering</h3>
      <ul class="skill-list">
        <li>Handling missing data — imputation strategies</li>
        <li>Encoding categoricals: one-hot, ordinal, target encoding</li>
        <li>Scaling: standardization, min-max, robust scaler</li>
        <li>Feature selection: filter, wrapper, embedded methods</li>
        <li>Creating interaction features</li>
        <li>Handling skewed distributions (log transforms)</li>
        <li>Datetime feature extraction</li>
        <li>Dimensionality reduction (PCA, t-SNE, UMAP)</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon" style="background:#0d2e1f">🗃️</span> Data Pipeline</h3>
      <ul class="skill-list">
        <li>Scikit-learn Pipeline and ColumnTransformer</li>
        <li>Data leakage — detect and prevent (critical!)</li>
        <li>Data versioning with DVC</li>
        <li>EDA automation (ydata-profiling)</li>
        <li>SQL for data extraction</li>
        <li>Working with APIs and web scraping</li>
        <li>Data cleaning patterns</li>
      </ul>
    </div>
  </div>

  <div class="section-title">First Algorithms — Understand Deeply</div>
  <div class="accordion">
    <div class="acc-header" onclick="toggleAcc(this)">📏 Linear & Logistic Regression <span class="arrow">▼</span></div>
    <div class="acc-body">
      Derive the closed-form solution for linear regression (normal equations: θ = (XᵀX)⁻¹Xᵀy). Implement gradient descent for regression from scratch. Understand logistic regression as a GLM, sigmoid function, and why log-loss is the right loss function. Understand multicollinearity, VIF, and the assumptions of OLS. Know L1 vs L2 regularization effects on coefficients.
    </div>
  </div>
  <div class="accordion">
    <div class="acc-header" onclick="toggleAcc(this)">🌳 Decision Trees — From Root to Leaf <span class="arrow">▼</span></div>
    <div class="acc-body">
      Understand information gain and Gini impurity. Implement a decision tree from scratch using recursive binary splitting. Understand why deep trees overfit. Know about pruning: pre-pruning (max_depth, min_samples) and post-pruning (cost-complexity). Decision boundaries are axis-aligned — understand why.
    </div>
  </div>
  <div class="accordion">
    <div class="acc-header" onclick="toggleAcc(this)">🌲 Ensemble Methods: Random Forests & Boosting <span class="arrow">▼</span></div>
    <div class="acc-body">
      Bagging: how Random Forests reduce variance through bootstrapping + feature subsampling. Understand OOB (out-of-bag) error. Gradient Boosting: understand it as functional gradient descent (not just "trees in sequence"). XGBoost, LightGBM, CatBoost — know the differences in split finding algorithms, handling of categoricals, and missing values.
    </div>
  </div>
  <div class="accordion">
    <div class="acc-header" onclick="toggleAcc(this)">🔮 Support Vector Machines (SVM) <span class="arrow">▼</span></div>
    <div class="acc-body">
      Understand maximum margin classifier. The kernel trick — why it allows nonlinear decision boundaries without explicit feature mapping. C parameter (soft margin), gamma for RBF kernel. SVMs in high-dimensional spaces (text classification). Dual formulation and Lagrange multipliers.
    </div>
  </div>
  <div class="accordion">
    <div class="acc-header" onclick="toggleAcc(this)">🔵 K-Means, DBSCAN, Hierarchical Clustering <span class="arrow">▼</span></div>
    <div class="acc-body">
      K-means: EM algorithm interpretation, sensitivity to initialization (K-means++), choosing K with elbow/silhouette. DBSCAN: density-based, handles arbitrary shapes, epsilon and min_samples tuning, noise robustness. Hierarchical: dendrograms, linkage criteria. Evaluation: silhouette score, Davies-Bouldin, Calinski-Harabász.
    </div>
  </div>

  <div class="section-title">Phase 1 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🏡 House Price Prediction — End-to-End Pipeline</span>
      <span class="diff-badge diff-easy">Beginner</span>
    </div>
    <div class="project-desc">Full pipeline on Kaggle House Prices: EDA → feature engineering → multiple models (linear regression, RF, XGBoost, stack ensemble) → hyperparameter tuning → submission. Document every decision. Don't just hit a good score — understand WHY each feature matters.</div>
    <div class="project-tags"><span class="tag">Scikit-learn</span><span class="tag">XGBoost</span><span class="tag">Feature Engineering</span><span class="tag">Ensemble</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📧 Spam Classifier — Text ML Pipeline</span>
      <span class="diff-badge diff-easy">Beginner</span>
    </div>
    <div class="project-desc">Build a spam classifier with TF-IDF + Naive Bayes, then Logistic Regression, then LinearSVC. Compare results. Add a Flask API. Understand precision vs recall for spam (false positives are worse than false negatives here — why?).</div>
    <div class="project-tags"><span class="tag">NLP basics</span><span class="tag">TF-IDF</span><span class="tag">Naive Bayes</span><span class="tag">Flask</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🔍 Customer Segmentation — Unsupervised ML</span>
      <span class="diff-badge diff-med">Intermediate</span>
    </div>
    <div class="project-desc">Use K-Means, DBSCAN, and Gaussian Mixture Models on e-commerce data (RFM features: Recency, Frequency, Monetary). Compare cluster quality metrics. Build a business narrative: what does each cluster mean? What marketing action should each get?</div>
    <div class="project-tags"><span class="tag">K-Means</span><span class="tag">PCA</span><span class="tag">UMAP</span><span class="tag">Business Analysis</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">⚗️ ML Algorithm from Scratch Library</span>
      <span class="diff-badge diff-med">Intermediate</span>
    </div>
    <div class="project-desc">Implement Linear Regression, Logistic Regression, Decision Tree, K-Means, PCA, and SVM from scratch using only NumPy. Match scikit-learn's results. This is the single best learning exercise for a deep ML foundation. Put it on GitHub.</div>
    <div class="project-tags"><span class="tag">From Scratch</span><span class="tag">NumPy</span><span class="tag">Algorithms</span><span class="tag">GitHub</span></div>
  </div>
</div>

<!-- PHASE 2 -->
<div class="phase" id="phase-3">
  <div class="phase-header">
    <div class="phase-num phase2-clr" style="color:#0c2461">P2</div>
    <div class="phase-info">
      <h2>Phase 2 — Core ML Algorithms & Advanced Topics</h2>
      <p>Go deeper. This phase covers advanced ensemble methods, model interpretability (essential for production), time series, anomaly detection, and recommendation systems.</p>
      <div class="phase-meta">
        <span class="badge" style="background:#0d2031;color:#3b82f6;border:1px solid #3b82f6">⏱ Months 4–7</span>
        <span class="badge" style="background:#0d2031;color:#3b82f6;border:1px solid #3b82f6">🔵 Intermediate</span>
      </div>
    </div>
  </div>

  <div class="grid2">
    <div class="card">
      <h3>Advanced Ensemble Methods</h3>
      <ul class="skill-list">
        <li>XGBoost internals: second-order Taylor expansion of loss</li>
        <li>LightGBM: GOSS + EFB for speed</li>
        <li>CatBoost: ordered boosting for categoricals</li>
        <li>Stacking and blending ensembles</li>
        <li>Optuna/Hyperopt for automated HPO</li>
        <li>Feature importance: MDI, permutation, SHAP</li>
        <li>Early stopping, learning rate schedules</li>
      </ul>
    </div>
    <div class="card">
      <h3>Model Interpretability (Critical!)</h3>
      <ul class="skill-list">
        <li>SHAP values — global and local explanations</li>
        <li>LIME — local surrogate models</li>
        <li>Partial Dependence Plots (PDP)</li>
        <li>Individual Conditional Expectation (ICE)</li>
        <li>Feature interaction analysis</li>
        <li>Model cards and datasheets</li>
        <li>Algorithmic fairness metrics</li>
        <li>Counterfactual explanations</li>
      </ul>
    </div>
    <div class="card">
      <h3>Time Series</h3>
      <ul class="skill-list">
        <li>Stationarity — ADF test, KPSS test</li>
        <li>ARIMA, SARIMA, ARIMAX</li>
        <li>Exponential smoothing (Holt-Winters)</li>
        <li>Prophet — trend + seasonality decomposition</li>
        <li>Feature engineering for time series</li>
        <li>Walk-forward validation (no data leakage!)</li>
        <li>Neural forecasting: N-BEATS, TimesNet</li>
        <li>Multivariate: VAR models, Granger causality</li>
      </ul>
    </div>
    <div class="card">
      <h3>Anomaly Detection</h3>
      <ul class="skill-list">
        <li>Statistical: Z-score, IQR, moving averages</li>
        <li>Isolation Forest — how it works mathematically</li>
        <li>One-Class SVM</li>
        <li>Local Outlier Factor (LOF)</li>
        <li>Autoencoders for anomaly detection</li>
        <li>Streaming anomaly detection</li>
        <li>Evaluation without ground truth</li>
      </ul>
    </div>
    <div class="card">
      <h3>Recommendation Systems</h3>
      <ul class="skill-list">
        <li>Collaborative filtering: user-based, item-based</li>
        <li>Matrix factorization: SVD, ALS, NMF</li>
        <li>Content-based filtering</li>
        <li>Hybrid systems</li>
        <li>Neural collaborative filtering</li>
        <li>Two-tower models (candidate retrieval)</li>
        <li>Evaluation: NDCG, MAP, Hit Rate</li>
        <li>Implicit vs explicit feedback</li>
      </ul>
    </div>
    <div class="card">
      <h3>Bayesian Methods</h3>
      <ul class="skill-list">
        <li>Bayesian vs frequentist — understand the debate</li>
        <li>Bayesian inference: prior, likelihood, posterior</li>
        <li>Bayesian linear regression</li>
        <li>Gaussian Processes</li>
        <li>Markov Chain Monte Carlo (MCMC)</li>
        <li>Variational inference basics</li>
        <li>PyMC or Stan for probabilistic programming</li>
        <li>Bayesian A/B testing</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Phase 2 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">💳 Credit Risk Scorecard with Full Interpretability</span>
      <span class="diff-badge diff-med">Intermediate</span>
    </div>
    <div class="project-desc">Build a credit default prediction model (use Lending Club or Kaggle credit data). Use XGBoost, then analyze with SHAP. Build a scorecard that a business can understand. Add fairness analysis: does the model discriminate by gender/race? Implement reject inference for partially labeled data.</div>
    <div class="project-tags"><span class="tag">XGBoost</span><span class="tag">SHAP</span><span class="tag">Fairness</span><span class="tag">Business Logic</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📈 Stock Price Forecasting Pipeline</span>
      <span class="diff-badge diff-med">Intermediate</span>
    </div>
    <div class="project-desc">Forecast stock price/returns using ARIMA, Prophet, XGBoost with lag features, and LSTM. Use proper walk-forward validation. The key learning is NOT predicting stock prices accurately (impossible!) but understanding how to validate time series models correctly without data leakage.</div>
    <div class="project-tags"><span class="tag">ARIMA</span><span class="tag">Prophet</span><span class="tag">Walk-forward CV</span><span class="tag">Feature Engineering</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🎬 Movie Recommendation Engine</span>
      <span class="diff-badge diff-med">Intermediate</span>
    </div>
    <div class="project-desc">Build on MovieLens 25M dataset. Implement: (1) user-item collaborative filtering from scratch, (2) matrix factorization with ALS (implicit), (3) a neural two-tower model in PyTorch. Serve recommendations via a FastAPI endpoint. Evaluate with NDCG@10.</div>
    <div class="project-tags"><span class="tag">Collaborative Filtering</span><span class="tag">ALS</span><span class="tag">Neural Recsys</span><span class="tag">FastAPI</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🔬 Kaggle Competition: Top 10%</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Join a Kaggle tabular competition and aim for top 10%. This teaches: how to read winning notebooks, ensemble strategies, post-processing tricks, and how much feature engineering matters vs model selection. Study top solutions after competition ends.</div>
    <div class="project-tags"><span class="tag">Kaggle</span><span class="tag">Stacking</span><span class="tag">Advanced Feature Eng</span><span class="tag">Competition ML</span></div>
  </div>
</div>

<!-- PHASE 3 -->
<div class="phase" id="phase-4">
  <div class="phase-header">
    <div class="phase-num phase3-clr" style="color:#2e1065">P3</div>
    <div class="phase-info">
      <h2>Phase 3 — Deep Learning & Neural Networks</h2>
      <p>Go from perceptrons to modern Transformers. Understand backpropagation deeply, PyTorch internals, and how to train stable large models. This phase takes you from "ML engineer" to "deep learning engineer."</p>
      <div class="phase-meta">
        <span class="badge" style="background:#1f0d2d;color:#8b5cf6;border:1px solid #8b5cf6">⏱ Months 7–11</span>
        <span class="badge" style="background:#1f0d2d;color:#8b5cf6;border:1px solid #8b5cf6">🧠 Advanced</span>
      </div>
    </div>
  </div>

  <div class="section-title">Neural Network Fundamentals</div>
  <div class="grid3">
    <div class="card">
      <h3>Forward & Backward Pass</h3>
      <ul class="skill-list">
        <li>Perceptron → MLP architecture</li>
        <li>Activation functions: ReLU, GELU, Sigmoid, Tanh, Swish</li>
        <li>Backpropagation — derive by hand</li>
        <li>Computational graphs</li>
        <li>Vanishing/exploding gradients</li>
        <li>Gradient clipping</li>
        <li>Weight initialization: Xavier, He, Kaiming</li>
      </ul>
    </div>
    <div class="card">
      <h3>Training Techniques</h3>
      <ul class="skill-list">
        <li>Optimizers: SGD, Momentum, Adam, AdamW, Lion</li>
        <li>Learning rate schedules: warmup, cosine, cyclic</li>
        <li>Batch normalization — why it works</li>
        <li>Layer normalization (used in Transformers)</li>
        <li>Dropout, DropPath</li>
        <li>Data augmentation strategies</li>
        <li>Mixed precision training (fp16, bf16)</li>
        <li>Gradient accumulation</li>
      </ul>
    </div>
    <div class="card">
      <h3>PyTorch Mastery</h3>
      <ul class="skill-list">
        <li>Tensor operations, autograd, .backward()</li>
        <li>Custom nn.Module and forward()</li>
        <li>DataLoader, Dataset, Sampler</li>
        <li>Custom loss functions</li>
        <li>Custom training loops (not Trainer)</li>
        <li>torch.compile, TorchScript</li>
        <li>GPU memory management</li>
        <li>Distributed training (DDP)</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Deep Learning Architectures</div>
  <div class="arch-box">
    <h4>🖼️ Convolutional Neural Networks (CNNs)</h4>
    <div class="arch-desc">Convolution operation, stride, padding, receptive field. Pooling layers. Feature map visualization. Architectures: LeNet → AlexNet → VGG → ResNet → EfficientNet → ConvNeXt. Skip connections (ResNet) — why they solved vanishing gradients. Transfer learning and fine-tuning. Object detection: YOLO, Faster R-CNN. Semantic segmentation: U-Net.</div>
    <div class="arch-apps"><span class="app-tag">Image Classification</span><span class="app-tag">Object Detection</span><span class="app-tag">Segmentation</span><span class="app-tag">Medical Imaging</span></div>
  </div>
  <div class="arch-box">
    <h4>🔄 Recurrent Neural Networks (RNNs, LSTMs, GRUs)</h4>
    <div class="arch-desc">Vanishing gradient in RNNs. LSTM gates: input, forget, output, cell state (derive update equations). GRU as simplified LSTM. Bidirectional RNNs. Sequence-to-sequence with encoder-decoder. Attention mechanisms — before Transformers. Teacher forcing. BPTT (backprop through time).</div>
    <div class="arch-apps"><span class="app-tag">Text Generation</span><span class="app-tag">Time Series</span><span class="app-tag">Speech</span><span class="app-tag">Machine Translation</span></div>
  </div>
  <div class="arch-box">
    <h4>⚡ Transformers — The Most Important Architecture</h4>
    <div class="arch-desc">Self-attention: Q, K, V matrices. Scaled dot-product attention: softmax(QKᵀ/√d_k)V. Multi-head attention — why multiple heads? Positional encodings: sinusoidal vs learned. Feed-forward sub-layers. Layer norm placement: post vs pre. Encoder-only (BERT), decoder-only (GPT), encoder-decoder (T5). Attention complexity O(n²) — sparse attention solutions.</div>
    <div class="arch-apps"><span class="app-tag">NLP</span><span class="app-tag">Vision (ViT)</span><span class="app-tag">Audio</span><span class="app-tag">Protein Folding</span></div>
  </div>
  <div class="arch-box">
    <h4>🎨 Generative Models: VAEs, GANs, Diffusion</h4>
    <div class="arch-desc">VAEs: encoder-decoder + reparameterization trick, ELBO loss. GANs: generator vs discriminator, mode collapse, Wasserstein GAN. Diffusion models: forward (noise adding) and reverse (denoising) processes, DDPM, DDIM, score matching, classifier-free guidance. Stable Diffusion architecture.</div>
    <div class="arch-apps"><span class="app-tag">Image Generation</span><span class="app-tag">Text-to-Image</span><span class="app-tag">Drug Discovery</span><span class="app-tag">Video</span></div>
  </div>
  <div class="arch-box">
    <h4>🔊 Graph Neural Networks (GNNs)</h4>
    <div class="arch-desc">Message passing framework. GCN, GraphSAGE, GAT (graph attention). Node classification, link prediction, graph classification. Heterogeneous graphs. GNNs for molecular property prediction (used in drug discovery). Over-smoothing problem. PyG (PyTorch Geometric) / DGL.</div>
    <div class="arch-apps"><span class="app-tag">Social Networks</span><span class="app-tag">Molecules</span><span class="app-tag">Knowledge Graphs</span><span class="app-tag">Fraud Detection</span></div>
  </div>

  <div class="section-title">Phase 3 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🔥 Build a Transformer from Scratch</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Implement the original "Attention Is All You Need" transformer in PyTorch from scratch — multi-head attention, positional encoding, encoder, decoder. Train on English→French translation (Multi30k). This is the most important deep learning exercise. Reference: Andrej Karpathy's nanoGPT.</div>
    <div class="project-tags"><span class="tag">PyTorch</span><span class="tag">Transformer</span><span class="tag">From Scratch</span><span class="tag">Attention</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🩺 Medical Image Segmentation — U-Net</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Brain tumor segmentation on BraTS dataset. Build U-Net with skip connections. Handle 3D MRI data. Use Dice loss + BCE. Implement TTA (test-time augmentation). This combines CNNs, medical domain knowledge, and production thinking (model uncertainty is life-critical).</div>
    <div class="project-tags"><span class="tag">U-Net</span><span class="tag">Dice Loss</span><span class="tag">Medical AI</span><span class="tag">3D Data</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🎭 Character-Level Language Model (GPT-style)</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Follow Karpathy's makemore/nanoGPT. Build a character-level GPT to generate Shakespeare. Then scale: add BPE tokenization, multiple transformer blocks, KV cache for inference, top-k/nucleus sampling. Deploy as a REST API.</div>
    <div class="project-tags"><span class="tag">GPT</span><span class="tag">Language Model</span><span class="tag">BPE</span><span class="tag">Inference Optimization</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🧬 Molecular Property Prediction with GNNs</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Predict HOMO-LUMO gap or solubility of molecules using Graph Neural Networks (GCN/GAT) with PyTorch Geometric on QM9 or ESOL dataset. Learn SMILES representation, molecular graphs, and how GNNs encode chemical structure.</div>
    <div class="project-tags"><span class="tag">PyTorch Geometric</span><span class="tag">GNN</span><span class="tag">Chemistry</span><span class="tag">Message Passing</span></div>
  </div>

  <div class="section-title">Learning Resources</div>
  <div class="card">
    <ul class="resources-list">
      <li><span class="res-type res-course">Course</span><div><strong>fast.ai Practical Deep Learning</strong> — Legendary course. Top-down approach. Free. Do it before Andrew Ng for intuition-first learning.</div></li>
      <li><span class="res-type res-course">Course</span><div><strong>Andrej Karpathy's Neural Nets Zero to Hero</strong> — YouTube. Build everything from scratch. The best DL course for actual understanding.</div></li>
      <li><span class="res-type res-book">Book</span><div><strong>Deep Learning (Goodfellow, Bengio, Courville)</strong> — The "deep learning bible." Read chapters on optimization, regularization, and sequence models.</div></li>
      <li><span class="res-type res-paper">Paper</span><div><strong>"Attention Is All You Need" (Vaswani 2017)</strong> — Read, implement, and re-read. The most important ML paper of the decade.</div></li>
      <li><span class="res-type res-paper">Paper</span><div><strong>"Deep Residual Learning" (He 2015)</strong> — Understand skip connections and how they enable 100+ layer networks.</div></li>
    </ul>
  </div>
</div>

<!-- PHASE 4 -->
<div class="phase" id="phase-5">
  <div class="phase-header">
    <div class="phase-num phase4-clr" style="color:#500724">P4</div>
    <div class="phase-info">
      <h2>Phase 4 — Advanced AI: NLP, CV, Reinforcement Learning & LLMs</h2>
      <p>Specialize. Modern AI is dominated by large models. This phase covers fine-tuning LLMs, building RAG systems, computer vision at scale, and reinforcement learning including RLHF (how ChatGPT was trained).</p>
      <div class="phase-meta">
        <span class="badge" style="background:#2d0828;color:#ec4899;border:1px solid #ec4899">⏱ Months 11–16</span>
        <span class="badge" style="background:#2d0828;color:#ec4899;border:1px solid #ec4899">🎯 Specialist</span>
      </div>
    </div>
  </div>

  <div class="section-title">Large Language Models (LLMs) — Essential for 2025+</div>
  <div class="grid2">
    <div class="card">
      <h3>LLM Fundamentals</h3>
      <ul class="skill-list">
        <li>Pre-training: next-token prediction at scale</li>
        <li>Tokenization: BPE, WordPiece, SentencePiece</li>
        <li>Scaling laws (Chinchilla): compute-optimal training</li>
        <li>BERT (masked LM), GPT (causal LM), T5 (seq2seq)</li>
        <li>Context window limits and long-context models</li>
        <li>Emergent abilities and in-context learning</li>
        <li>Chain-of-thought prompting</li>
        <li>KV cache and inference optimization</li>
      </ul>
    </div>
    <div class="card">
      <h3>Fine-Tuning & Alignment</h3>
      <ul class="skill-list">
        <li>Full fine-tuning vs parameter-efficient (PEFT)</li>
        <li>LoRA and QLoRA — mathematical intuition</li>
        <li>Instruction tuning (FLAN, InstructGPT)</li>
        <li>RLHF: reward model + PPO (how ChatGPT was trained)</li>
        <li>DPO (Direct Preference Optimization)</li>
        <li>Constitutional AI (Anthropic's approach)</li>
        <li>Evaluation: MMLU, HumanEval, BIG-bench</li>
        <li>Quantization: GPTQ, AWQ, GGUF (llama.cpp)</li>
      </ul>
    </div>
    <div class="card">
      <h3>RAG Systems (High Demand!)</h3>
      <ul class="skill-list">
        <li>Retrieval-Augmented Generation architecture</li>
        <li>Dense vs sparse retrieval (BM25 vs embeddings)</li>
        <li>Vector databases: Pinecone, Weaviate, Chroma, pgvector</li>
        <li>Embedding models: text-embedding-ada, E5, BGE</li>
        <li>Chunking strategies for documents</li>
        <li>Reranking with cross-encoders</li>
        <li>HyDE, multi-query retrieval</li>
        <li>RAG evaluation: faithfulness, relevance</li>
      </ul>
    </div>
    <div class="card">
      <h3>LLM Agents & Tools</h3>
      <ul class="skill-list">
        <li>ReAct framework (Reason + Act)</li>
        <li>Tool use / function calling</li>
        <li>LangChain, LlamaIndex — when to use, when to avoid</li>
        <li>Multi-agent systems</li>
        <li>Code generation agents</li>
        <li>Memory systems for agents</li>
        <li>Structured output (JSON mode)</li>
        <li>Prompt injection and security</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Advanced Computer Vision</div>
  <div class="grid3">
    <div class="card">
      <h3>Vision Transformers</h3>
      <ul class="skill-list">
        <li>ViT — image patches as tokens</li>
        <li>DeiT — data-efficient training</li>
        <li>Swin Transformer — hierarchical ViT</li>
        <li>DINO/DINOv2 — self-supervised vision</li>
        <li>SAM (Segment Anything Model)</li>
        <li>CLIP — contrastive vision-language</li>
      </ul>
    </div>
    <div class="card">
      <h3>Multimodal Models</h3>
      <ul class="skill-list">
        <li>CLIP — zero-shot image classification</li>
        <li>DALL-E, Stable Diffusion architecture</li>
        <li>LLaVA, GPT-4V — visual LLMs</li>
        <li>Contrastive learning</li>
        <li>Image-text alignment</li>
        <li>Video understanding</li>
      </ul>
    </div>
    <div class="card">
      <h3>Production CV</h3>
      <ul class="skill-list">
        <li>Model compression for edge (MobileNet, EfficientLite)</li>
        <li>TensorRT optimization</li>
        <li>ONNX export</li>
        <li>Real-time inference pipelines</li>
        <li>Data labeling workflows</li>
        <li>Active learning for annotation</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Reinforcement Learning</div>
  <div class="grid2">
    <div class="card">
      <h3>RL Foundations</h3>
      <ul class="skill-list">
        <li>MDP: states, actions, rewards, transitions, discount factor</li>
        <li>Bellman equations — derive them</li>
        <li>Dynamic Programming: value iteration, policy iteration</li>
        <li>Monte Carlo methods</li>
        <li>Temporal Difference: Q-learning, SARSA</li>
        <li>Exploration vs exploitation: ε-greedy, UCB, Thompson sampling</li>
        <li>Deep Q-Network (DQN): experience replay, target network</li>
      </ul>
    </div>
    <div class="card">
      <h3>Advanced RL</h3>
      <ul class="skill-list">
        <li>Policy gradient: REINFORCE, actor-critic</li>
        <li>PPO (Proximal Policy Optimization) — used in RLHF!</li>
        <li>SAC (Soft Actor-Critic)</li>
        <li>Model-based RL: Dyna, MuZero</li>
        <li>Multi-agent RL</li>
        <li>Offline RL / Conservative Q-learning</li>
        <li>RL for LLMs (RLHF, GRPO)</li>
        <li>Gymnasium, Stable-Baselines3</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Phase 4 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🤖 Fine-tune LLaMA for Domain Q&A with QLoRA</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Fine-tune LLaMA-3 or Mistral on a domain-specific Q&A dataset (medical, legal, or code) using QLoRA (4-bit quantization + LoRA). Use Unsloth for speed. Evaluate with domain-specific benchmarks. Serve with vLLM. Compare to GPT-4 baseline.</div>
    <div class="project-tags"><span class="tag">QLoRA</span><span class="tag">HuggingFace</span><span class="tag">vLLM</span><span class="tag">LLaMA</span><span class="tag">Unsloth</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📄 Production RAG System — 10K Financial Reports</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Build a RAG pipeline over SEC 10-K financial filings. Implement: hierarchical chunking, hybrid search (BM25 + dense), cross-encoder reranking, faithfulness evaluation with RAGAS. Build a streaming API with FastAPI + Redis caching. This is exactly what companies hire for.</div>
    <div class="project-tags"><span class="tag">RAG</span><span class="tag">Weaviate</span><span class="tag">Cross-Encoder</span><span class="tag">RAGAS</span><span class="tag">FastAPI</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🎮 Deep RL Agent — Atari Game (from scratch)</span>
      <span class="diff-badge diff-hard">Hard</span>
    </div>
    <div class="project-desc">Implement DQN from the DeepMind 2015 paper to play Atari Breakout. Implement: frame stacking, experience replay, target network, epsilon decay. Then upgrade to Double DQN and Dueling DQN. Track metrics in W&B. This builds deep intuition for RL training dynamics.</div>
    <div class="project-tags"><span class="tag">DQN</span><span class="tag">Gymnasium</span><span class="tag">PyTorch</span><span class="tag">W&B</span><span class="tag">Atari</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🛡️ RLHF Training Pipeline (Mini-scale)</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Implement a mini RLHF pipeline: (1) train reward model on preference data, (2) fine-tune a small LM with PPO using the reward model. Use trl library. This gives deep insight into how alignment works and is directly relevant to AI safety research roles.</div>
    <div class="project-tags"><span class="tag">RLHF</span><span class="tag">PPO</span><span class="tag">trl</span><span class="tag">Reward Model</span><span class="tag">Alignment</span></div>
  </div>
</div>

<!-- PHASE 5 -->
<div class="phase" id="phase-6">
  <div class="phase-header">
    <div class="phase-num phase5-clr" style="color:#450a0a">P5</div>
    <div class="phase-info">
      <h2>Phase 5 — MLOps, Systems Design & Production ML</h2>
      <p>The gap between a hobbyist and a senior engineer is production. Anyone can get 90% accuracy in a notebook. Senior engineers build systems that stay accurate, scale to millions, and don't break at 3am.</p>
      <div class="phase-meta">
        <span class="badge" style="background:#2d0f0f;color:#ef4444;border:1px solid #ef4444">⏱ Months 16–20</span>
        <span class="badge" style="background:#2d0f0f;color:#ef4444;border:1px solid #ef4444">🏭 Production</span>
      </div>
    </div>
  </div>

  <div class="grid2">
    <div class="card">
      <h3>ML Pipeline Design</h3>
      <ul class="skill-list">
        <li>Feature stores: Feast, Hopsworks, Tecton</li>
        <li>Data versioning: DVC, Delta Lake, Iceberg</li>
        <li>Pipeline orchestration: Airflow, Prefect, Kubeflow</li>
        <li>Online vs offline feature computation</li>
        <li>Training pipelines: parametrized, reproducible</li>
        <li>Data validation: Great Expectations, Pandera</li>
        <li>Schema evolution handling</li>
      </ul>
    </div>
    <div class="card">
      <h3>Model Deployment</h3>
      <ul class="skill-list">
        <li>REST API serving: FastAPI, Flask, gRPC</li>
        <li>Batch inference pipelines</li>
        <li>Streaming inference (Kafka)</li>
        <li>BentoML, Seldon, KFServing, Ray Serve</li>
        <li>Model containers: Docker, GPU containers</li>
        <li>Kubernetes for ML workloads</li>
        <li>Serverless inference (Lambda, Cloud Run)</li>
        <li>Shadow deployments, canary releases</li>
      </ul>
    </div>
    <div class="card">
      <h3>Experiment Tracking & Versioning</h3>
      <ul class="skill-list">
        <li>MLflow: tracking, registry, projects</li>
        <li>Weights & Biases: sweeps, artifacts, reports</li>
        <li>Neptune, CometML</li>
        <li>Model registry and staging</li>
        <li>Reproducibility: seeds, configs, environments</li>
        <li>Hydra for configuration management</li>
        <li>DVC pipelines for data + model versioning</li>
      </ul>
    </div>
    <div class="card">
      <h3>Model Monitoring</h3>
      <ul class="skill-list">
        <li>Data drift: KS test, PSI, Jensen-Shannon</li>
        <li>Concept drift detection</li>
        <li>Model performance degradation alerts</li>
        <li>Evidently AI, Whylogs, NannyML</li>
        <li>Prometheus + Grafana for ML metrics</li>
        <li>Logging predictions, features, outcomes</li>
        <li>Alerting on drift triggers retraining</li>
      </ul>
    </div>
    <div class="card">
      <h3>Performance & Optimization</h3>
      <ul class="skill-list">
        <li>Model quantization: INT8, INT4, FP16</li>
        <li>Knowledge distillation</li>
        <li>Pruning (unstructured, structured)</li>
        <li>ONNX Runtime, TensorRT, OpenVINO</li>
        <li>Dynamic batching for throughput</li>
        <li>Speculative decoding for LLMs</li>
        <li>Profiling with PyTorch Profiler</li>
      </ul>
    </div>
    <div class="card">
      <h3>Cloud ML Platforms</h3>
      <ul class="skill-list">
        <li>AWS: SageMaker, EMR, S3, Lambda</li>
        <li>GCP: Vertex AI, BigQuery ML, GKE</li>
        <li>Azure: Azure ML, Databricks</li>
        <li>Spark + PySpark for big data ML</li>
        <li>Cost optimization: spot instances, reserved</li>
        <li>Multi-cloud strategies</li>
        <li>Infrastructure as Code (Terraform)</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Phase 5 Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🏗️ Full MLOps Platform — End-to-End</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Build a complete MLOps platform for a churn prediction model: DVC data versioning → feature store (Feast) → MLflow tracking → automated retraining pipeline (Airflow) → Docker + FastAPI serving → drift monitoring (Evidently) → Grafana dashboard. CI/CD with GitHub Actions. This is a portfolio centerpiece.</div>
    <div class="project-tags"><span class="tag">DVC</span><span class="tag">Feast</span><span class="tag">MLflow</span><span class="tag">Airflow</span><span class="tag">Docker</span><span class="tag">Evidently</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">⚡ High-Throughput LLM Serving System</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Deploy a quantized LLM (Mistral 7B GPTQ) with vLLM for batched inference. Implement: async request handling, streaming tokens, rate limiting, caching with Redis, load balancing (Nginx). Benchmark: latency P50/P95/P99, throughput (tokens/sec), GPU utilization. Optimize to &lt;100ms P50.</div>
    <div class="project-tags"><span class="tag">vLLM</span><span class="tag">Quantization</span><span class="tag">Redis</span><span class="tag">Benchmarking</span><span class="tag">Kubernetes</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📊 Real-Time ML Feature Pipeline with Kafka</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Build a real-time feature pipeline: user events → Kafka → Flink/Spark Streaming → online feature store → &lt;10ms feature serving for fraud detection. Implement feature freshness monitoring. Handle late-arriving data. This is what big tech data/ML teams build daily.</div>
    <div class="project-tags"><span class="tag">Kafka</span><span class="tag">Spark Streaming</span><span class="tag">Feature Store</span><span class="tag">Redis</span><span class="tag">Fraud Detection</span></div>
  </div>
</div>

<!-- PHASE 6 -->
<div class="phase" id="phase-7">
  <div class="phase-header">
    <div class="phase-num phase6-clr" style="color:#083344">P6</div>
    <div class="phase-info">
      <h2>Phase 6 — Senior Level: Research, Architecture & Leadership</h2>
      <p>This is what separates senior engineers from staff/principal. At this level, you drive technical direction, read and apply research, mentor teams, and design systems that last years.</p>
      <div class="phase-meta">
        <span class="badge" style="background:#083344;color:#06b6d4;border:1px solid #06b6d4">⏱ Months 20–24+</span>
        <span class="badge" style="background:#083344;color:#06b6d4;border:1px solid #06b6d4">👑 Senior+</span>
      </div>
    </div>
  </div>

  <div class="section-title">Research Skills</div>
  <div class="grid2">
    <div class="card">
      <h3>Reading Papers</h3>
      <ul class="skill-list">
        <li>How to skim: title → abstract → figures → intro → conclusion → details</li>
        <li>Critically evaluate claims and baselines</li>
        <li>Reproduce results from scratch</li>
        <li>Identify limitations and failure modes</li>
        <li>Track papers: Arxiv Sanity, Papers With Code, Semantic Scholar</li>
        <li>Weekly paper reading habit</li>
        <li>Write paper summaries and share with team</li>
      </ul>
    </div>
    <div class="card">
      <h3>Must-Read Paper Cannon</h3>
      <ul class="skill-list">
        <li>Attention Is All You Need (2017)</li>
        <li>BERT (Devlin 2018), GPT-2/3 (Brown 2020)</li>
        <li>Scaling Laws (Kaplan 2020)</li>
        <li>InstructGPT / RLHF (Ouyang 2022)</li>
        <li>LoRA (Hu 2021)</li>
        <li>Retrieval-Augmented Generation (Lewis 2020)</li>
        <li>ResNet, U-Net, YOLO</li>
        <li>AlphaFold 2 (Jumper 2021)</li>
      </ul>
    </div>
  </div>

  <div class="section-title">System Design for ML</div>
  <div class="senior-req">
    <h3>ML System Design — Questions You Must Nail</h3>
    <div class="req-grid">
      <div class="req-item">Design a recommendation system for Netflix (100M users)</div>
      <div class="req-item">Design a fraud detection system (&lt;10ms latency)</div>
      <div class="req-item">Design a search ranking system (Google/Amazon)</div>
      <div class="req-item">Design a ride-share ETA prediction system</div>
      <div class="req-item">Design a content moderation system at scale</div>
      <div class="req-item">Design an LLM serving platform (1000 RPS)</div>
      <div class="req-item">Design an ML feature store from scratch</div>
      <div class="req-item">Design a news feed ranking algorithm</div>
    </div>
  </div>

  <div class="grid2">
    <div class="card">
      <h3>Architecture Patterns</h3>
      <ul class="skill-list">
        <li>Two-tower models (retrieval + ranking)</li>
        <li>Multi-task learning architectures</li>
        <li>Mixture of Experts (MoE)</li>
        <li>Distillation pipelines (teacher → student)</li>
        <li>Cascade classifiers (cheap first, expensive second)</li>
        <li>Ensemble design for production</li>
        <li>Online learning vs batch retraining</li>
        <li>Multi-armed bandit for exploration</li>
      </ul>
    </div>
    <div class="card">
      <h3>Leadership & Communication</h3>
      <ul class="skill-list">
        <li>Mentor junior engineers — review their code and ML decisions</li>
        <li>Write tech specs for ML projects</li>
        <li>Run ML project retrospectives</li>
        <li>Explain models to product managers and execs</li>
        <li>Estimate effort and timelines for ML projects</li>
        <li>Build team-wide best practices for ML</li>
        <li>Interview candidates — design ML interview questions</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Senior-Level Projects</div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🔬 Research Replication + Extension</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Pick a recent ArXiv paper (2024–2025) in your specialty area. Replicate their results, then extend: try a different dataset, a novel architecture modification, or a different evaluation. Write a blog post or technical report. This demonstrates research-engineering bridge — highly valued at top companies.</div>
    <div class="project-tags"><span class="tag">Research</span><span class="tag">ArXiv</span><span class="tag">Novel Experiments</span><span class="tag">Blog Post</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">🏢 Open Source ML Library Contribution</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Contribute a non-trivial feature or bug fix to HuggingFace Transformers, scikit-learn, PyTorch, or LangChain. Review issues, understand the codebase, write tests. Even a merged PR to a major library demonstrates code quality and collaboration skills at a senior level.</div>
    <div class="project-tags"><span class="tag">Open Source</span><span class="tag">HuggingFace</span><span class="tag">PyTorch</span><span class="tag">Code Quality</span></div>
  </div>
  <div class="project-card">
    <div class="project-header">
      <span class="project-title">📝 ML System Design Document</span>
      <span class="diff-badge diff-sr">Senior</span>
    </div>
    <div class="project-desc">Write a full design document for a production ML system (e.g., fraud detection or recommendation). Include: problem framing, data requirements, feature engineering, model choice + tradeoffs, evaluation strategy, serving architecture, monitoring plan, failure modes, cost analysis. This mirrors actual senior work.</div>
    <div class="project-tags"><span class="tag">System Design</span><span class="tag">Documentation</span><span class="tag">Architecture</span><span class="tag">Tradeoffs</span></div>
  </div>

  <div class="section-title">Salary Ranges (2025)</div>
  <div class="card">
    <table class="salary-table">
      <tr><th>Role</th><th>US (Remote-friendly)</th><th>UK</th><th>EU</th><th>Experience</th></tr>
      <tr><td>ML Engineer</td><td>$100k–$150k</td><td>£60k–£90k</td><td>€55k–€85k</td><td>0–2 yrs</td></tr>
      <tr><td>Mid-Level ML Eng</td><td>$150k–$200k</td><td>£90k–£120k</td><td>€85k–€110k</td><td>2–5 yrs</td></tr>
      <tr><td>Senior ML Engineer</td><td>$200k–$280k</td><td>£120k–£160k</td><td>€110k–€150k</td><td>5–8 yrs</td></tr>
      <tr><td>Staff ML Engineer</td><td>$280k–$400k+</td><td>£160k–£220k</td><td>€150k–€200k</td><td>8+ yrs</td></tr>
      <tr><td>AI Research Scientist</td><td>$200k–$400k+</td><td>£130k–£200k</td><td>€120k–€180k</td><td>PhD + papers</td></tr>
    </table>
    <p style="font-size:.75rem;color:var(--muted);margin-top:.5rem">* FAANG/top AI labs pay 30–50% higher + substantial equity. Pakistan rates vary significantly.</p>
  </div>
</div>

<!-- INTERVIEW PREP -->
<div class="phase" id="phase-8">
  <div class="phase-header">
    <div class="phase-num" style="background:#fef3c7;color:#78350f;border-color:#f59e0b">💼</div>
    <div class="phase-info">
      <h2>Interview Preparation — Land That Senior Role</h2>
      <p>Senior ML interviews cover 4 areas: ML depth, coding, system design, and behavioral. You need to be strong in all of them.</p>
    </div>
  </div>

  <div class="grid2">
    <div class="interview-section">
      <h3>🧮 ML Theory Questions (Must Know Cold)</h3>
      <div class="q-item"><div class="q-cat">Fundamentals</div>Explain bias-variance tradeoff with the decomposition formula. How do you fix each?</div>
      <div class="q-item"><div class="q-cat">Gradient Descent</div>Why does Adam converge faster than SGD? What are its failure modes?</div>
      <div class="q-item"><div class="q-cat">Transformers</div>Walk me through the full attention mechanism. Why do we scale by √d_k?</div>
      <div class="q-item"><div class="q-cat">Regularization</div>What's the geometric interpretation of L1 vs L2 regularization?</div>
      <div class="q-item"><div class="q-cat">Probability</div>Derive the EM algorithm. Give an ML example where you'd use it.</div>
      <div class="q-item"><div class="q-cat">Training</div>Why does batch normalization help? What issues does it cause in RNNs?</div>
      <div class="q-item"><div class="q-cat">LLMs</div>Explain how RLHF works. What are the reward model's limitations?</div>
    </div>

    <div class="interview-section">
      <h3>🔧 Practical ML Questions</h3>
      <div class="q-item"><div class="q-cat">Debugging</div>Your model has 95% train accuracy but 60% test accuracy. Walk me through debugging.</div>
      <div class="q-item"><div class="q-cat">Class Imbalance</div>You have 1:100 imbalanced classes. What are your options? Which do you choose?</div>
      <div class="q-item"><div class="q-cat">Production</div>Your model was 90% accurate last month. Now it's 75%. What happened?</div>
      <div class="q-item"><div class="q-cat">Metrics</div>Your PM wants to improve "model quality." How do you define that?</div>
      <div class="q-item"><div class="q-cat">Data</div>You have 1M rows but suspect significant label noise. What do you do?</div>
      <div class="q-item"><div class="q-cat">Scale</div>Your model needs to serve 100k RPS. Current setup does 1k RPS. What do you do?</div>
    </div>
  </div>

  <div class="section-title">ML System Design Interview Framework</div>
  <div class="card">
    <div style="font-size:.9rem;font-weight:600;margin-bottom:.8rem;color:var(--accent)">Use this structure for every ML design question:</div>
    <div class="timeline">
      <div class="tl-item">
        <div class="tl-week">Step 1 (5 min)</div>
        <div class="tl-task">Clarify requirements</div>
        <div class="tl-sub">What is the ML objective? What's the scale? Latency requirements? Data availability? Deployment constraints? Don't start designing without asking.</div>
      </div>
      <div class="tl-item">
        <div class="tl-week">Step 2 (5 min)</div>
        <div class="tl-task">Define metrics</div>
        <div class="tl-sub">Offline metrics (AUC, NDCG, F1). Online metrics (CTR, conversion, revenue). How do they align? What's your North Star metric? How do you A/B test?</div>
      </div>
      <div class="tl-item">
        <div class="tl-week">Step 3 (10 min)</div>
        <div class="tl-task">Data & features</div>
        <div class="tl-sub">What data do you have? What features matter? How do you compute them? Online vs offline features? Handle cold start for new users/items?</div>
      </div>
      <div class="tl-item">
        <div class="tl-week">Step 4 (10 min)</div>
        <div class="tl-task">Model architecture</div>
        <div class="tl-sub">Start simple (logistic regression baseline). Then scale up. Multi-stage (retrieval → ranking → re-ranking). Model tradeoffs. Training strategy.</div>
      </div>
      <div class="tl-item">
        <div class="tl-week">Step 5 (5 min)</div>
        <div class="tl-task">Serving & infrastructure</div>
        <div class="tl-sub">How is the model deployed? Latency budget? Batch vs online prediction? Caching strategy? Feature store? How do you handle failures?</div>
      </div>
      <div class="tl-item">
        <div class="tl-week">Step 6 (5 min)</div>
        <div class="tl-task">Monitoring & iteration</div>
        <div class="tl-sub">What metrics do you monitor? When do you retrain? How do you detect model degradation? How do you roll back?</div>
      </div>
    </div>
  </div>

  <div class="section-title">Coding Interview Focus</div>
  <div class="grid3">
    <div class="card">
      <h3>Data Structures/Algorithms</h3>
      <ul class="skill-list">
        <li>Arrays, strings, hash maps</li>
        <li>Trees, graphs, BFS/DFS</li>
        <li>Dynamic programming</li>
        <li>Sorting and searching</li>
        <li>Sliding window, two pointers</li>
        <li>100 LeetCode Medium minimum</li>
      </ul>
    </div>
    <div class="card">
      <h3>ML Coding Tasks</h3>
      <ul class="skill-list">
        <li>Implement k-means from scratch</li>
        <li>Write custom loss function in PyTorch</li>
        <li>Vectorized operations in NumPy</li>
        <li>Implement precision@k for recsys</li>
        <li>Cross-validation loop from scratch</li>
        <li>Debug a training loop bug live</li>
      </ul>
    </div>
    <div class="card">
      <h3>Behavioral (STAR Method)</h3>
      <ul class="skill-list">
        <li>"Tell me about an ML project failure"</li>
        <li>"How did you improve model performance?"</li>
        <li>"How do you prioritize ML work?"</li>
        <li>"Tell me about a difficult stakeholder"</li>
        <li>"How do you mentor junior engineers?"</li>
        <li>Prepare 6 strong STAR stories</li>
      </ul>
    </div>
  </div>

  <div class="section-title">Your 90-Day Job Application Checklist</div>
  <div class="card">
    <ul class="checklist" id="checklist">
      <li><div class="chk" onclick="toggleChk(this)"></div><span>GitHub profile: 5+ ML projects with READMEs, clean code, and documented results</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Portfolio blog (Medium, Substack, personal site) with 3+ deep technical articles</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>LinkedIn updated: certifications, projects, quantified impact ("improved model AUC by 8%")</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>ML algorithms from scratch repo — the ultimate resume signal</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Kaggle profile: at least 1 competition in top 20%</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>LeetCode: 100+ problems solved (Easy + Medium), comfortable with patterns</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>ML system design: practiced 10+ problems out loud</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Paper summary blog: "I implemented X paper, here's what I learned"</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Open source contribution: at least 1 merged PR to a known library</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Mock interviews: 5+ full mock sessions with another person</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Target companies list: research their ML stack, papers, blog posts</span></li>
      <li><div class="chk" onclick="toggleChk(this)"></div><span>Certifications: AWS ML Specialty or GCP Professional ML Engineer</span></li>
    </ul>
  </div>

  <div class="tip-box">🎯 <div><strong>Final Advice:</strong> Depth over breadth. Companies hiring senior ML engineers would rather have someone who deeply understands transformers and can debug training instabilities than someone who "knows" 20 algorithms at surface level. Pick 2 specialties (e.g., NLP + MLOps), go extremely deep, build production projects, and make your GitHub your resume.</div></div>
</div>

</div><!-- main -->

<script>
function switchPhase(n){
  document.querySelectorAll('.phase').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById('phase-'+n).classList.add('active');
  document.querySelectorAll('.nav-btn')[n].classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
}
function toggleAcc(header){
  var body=header.nextElementSibling;
  var arrow=header.querySelector('.arrow');
  body.classList.toggle('open');
  arrow.textContent=body.classList.contains('open')?'▲':'▼';
}
function toggleChk(el){
  el.classList.toggle('checked');
  el.textContent=el.classList.contains('checked')?'✓':'';
}
</script>
</body>
</html>
