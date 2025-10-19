<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>CloudTech Analytics — Data training, dashboards & AI for teams</title>
  <meta name="description" content="CloudTech Analytics: Practical data analytics, data science, and dashboarding training for professionals and teams. Courses, projects, consulting and internships.">
  <meta property="og:title" content="CloudTech Analytics" />
  <meta property="og:description" content="Practical data analytics, data science & dashboarding for teams and individuals." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#0f172a" />

  <!-- Favicons / simple SVG logo placeholder -->
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' rx='20' fill='%230a84ff'/%3E%3Ctext x='50' y='57' font-size='48' fill='white' text-anchor='middle' font-family='Arial, Helvetica, sans-serif'%3ECT%3C/text%3E%3C/svg%3E">

  <style>
    :root{
      --bg:#0b1220; --card:#0f172a; --muted:#9aa4b2; --accent1:linear-gradient(135deg,#0ea5e9 0%, #7c3aed 100%); --glass: rgba(255,255,255,0.03);
      --radius:14px;
      --maxw:1100px;
      --ff: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:var(--ff); background: radial-gradient(1200px 600px at 10% 20%, rgba(124,58,237,0.12), transparent 6%), radial-gradient(1000px 400px at 95% 80%, rgba(14,165,233,0.06), transparent 6%), var(--bg); color:#e6eef8; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
      line-height:1.45; padding:28px 20px;
    }
    .container{max-width:var(--maxw); margin:0 auto}

    /* Header */
    header{display:flex; align-items:center; justify-content:space-between; gap:18px}
    .brand{display:flex; align-items:center; gap:12px}
    .logo{width:56px; height:56px; border-radius:12px; display:grid; place-items:center; background:var(--accent1); box-shadow:0 6px 18px rgba(12,14,20,0.6); font-weight:700}
    .brand h1{font-size:18px;margin:0}
    .nav{display:flex; gap:12px; align-items:center}
    .nav a{color:var(--muted); text-decoration:none; font-weight:600; padding:8px 12px; border-radius:10px}
    .nav a:hover{color:white; background:var(--glass)}
    .cta-primary{background:var(--accent1); padding:10px 14px; border-radius:12px; color:white; text-decoration:none; font-weight:700; box-shadow:0 8px 24px rgba(124,58,237,0.18);}

    /* Hero */
    .hero{display:grid; grid-template-columns:1fr 420px; gap:36px; align-items:center; margin-top:36px}
    .hero .lead{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent); padding:28px; border-radius:18px; box-shadow:0 6px 30px rgba(2,6,23,0.6)}
    .eyebrow{display:inline-block; padding:6px 10px; border-radius:999px; background:rgba(255,255,255,0.04); color: #bcd7ff; font-weight:700; font-size:13px}
    .title{font-size:28px; margin:14px 0 8px; color:#fff}
    .subtitle{color:var(--muted); margin:0 0 18px}
    .lead p{margin:0 0 18px}
    .actions{display:flex; gap:12px; align-items:center}
    .card-stats{display:flex; gap:12px; margin-top:18px}
    .stat{background:rgba(255,255,255,0.02); padding:10px 12px; border-radius:12px; text-align:center}
    .stat strong{display:block; font-size:16px}

    /* Mock dashboard card */
    .mock{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border-radius:14px; padding:16px; box-shadow: inset 0 1px 0 rgba(255,255,255,0.02);}
    .mock .header{display:flex; justify-content:space-between; align-items:center; margin-bottom:12px}
    .filters{display:flex; gap:8px}
    .chip{padding:6px 10px; background:rgba(255,255,255,0.03); border-radius:10px; font-size:13px}
    .chart{height:200px; border-radius:10px; background:linear-gradient(90deg,#06202c,#0b1530); display:flex; align-items:center; justify-content:center; color:var(--muted)}

    /* Features */
    .features{display:grid; grid-template-columns:repeat(3,1fr); gap:18px; margin-top:34px}
    .feature{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent); padding:18px; border-radius:12px}
    .feature h3{margin:10px 0 6px}
    .feature p{margin:0; color:var(--muted)}

    /* Testimonials */
    .testimonials{margin-top:34px; display:flex; gap:14px}
    .test{background:rgba(255,255,255,0.02); padding:16px; border-radius:12px}

    /* Footer */
    footer{margin-top:48px; padding-top:18px; border-top:1px solid rgba(255,255,255,0.03); display:flex; justify-content:space-between; align-items:center}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr;}
      .features{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:560px){
      .nav{display:none}
      .features{grid-template-columns:1fr}
      .logo{width:46px;height:46px}
      .title{font-size:22px}
    }

    /* Subtle animated icon */
    .pulse{display:inline-block; width:12px; height:12px; border-radius:50%; background:rgba(124,58,237,0.9); box-shadow:0 0 0 0 rgba(124,58,237,0.5); animation:pulse 2s infinite}
    @keyframes pulse{0%{box-shadow:0 0 0 0 rgba(124,58,237,0.6)}70%{box-shadow:0 0 0 18px rgba(124,58,237,0)}100%{box-shadow:0 0 0 0 rgba(124,58,237,0)}}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">CT</div>
        <div>
          <h1>CloudTech Analytics</h1>
          <div style="font-size:12px;color:var(--muted);">Data training, dashboards & AI for teams</div>
        </div>
      </div>

      <nav class="nav" aria-label="Main navigation">
        <a href="#courses">Courses</a>
        <a href="#projects">Projects</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a class="cta-primary" href="#signup">Get started</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="lead" role="region" aria-labelledby="lead-title">
          <span class="eyebrow"><span class="pulse" style="margin-right:8px"></span> New cohort open</span>
          <h2 id="lead-title" class="title">Build dashboards, ship models, and get real-world analytics experience</h2>
          <p class="subtitle">Hands-on courses, practical projects and team upskilling designed for product teams, analysts and early-stage startups.</p>

          <p>We teach tools that get you results: SQL, Python, Looker/Mode, Power BI, dashboards with automated pipelines, and deployable ML prototypes.</p>

          <div class="actions">
            <a class="cta-primary" href="#signup">Enroll now — free preview</a>
            <a href="#courses" style="color:var(--muted); text-decoration:none; padding:10px 12px; border-radius:12px; background:rgba(255,255,255,0.02)">View courses</a>
          </div>

          <div class="card-stats" aria-hidden="true">
            <div class="stat"><strong>120+</strong><span style="color:var(--muted);font-size:12px">Projects completed</span></div>
            <div class="stat"><strong>4.8/5</strong><span style="color:var(--muted);font-size:12px">Average rating</span></div>
            <div class="stat"><strong>Teams</strong><span style="color:var(--muted);font-size:12px">Hiring-ready graduates</span></div>
          </div>
        </div>

        <aside class="mock" aria-hidden="false">
          <div class="header">
            <div style="font-weight:700">Sales dashboard</div>
            <div class="filters">
              <div class="chip">Last 30d</div>
              <div class="chip">Region</div>
            </div>
          </div>
          <div class="chart">Interactive sales chart (mock)</div>
          <div style="display:flex; gap:12px; margin-top:12px;">
            <div class="chip">Revenue</div>
            <div class="chip">Customers</div>
            <div class="chip">Conversion</div>
          </div>
        </aside>
      </section>

      <section id="courses" class="features" aria-labelledby="features-title">
        <h2 id="features-title" style="grid-column:1/-1; margin-bottom:0">What we offer</h2>
        <div class="feature">
          <h3>Practical courses</h3>
          <p>Short, project-focused modules — SQL to production pipelines, dashboarding, and model deployment.</p>
        </div>
        <div class="feature">
          <h3>Company upskilling</h3>
          <p>Tailored training for teams: curriculum, mentorship, and capstone projects aligned to your product metrics.</p>
        </div>
        <div class="feature">
          <h3>Internships & projects</h3>
          <p>Real data projects for learners with clear specs and review — teams can sponsor tasks and hire top performers.</p>
      </section>

      <section id="projects" style="margin-top:28px">
        <h2>Recent projects</h2>
        <div style="display:grid; grid-template-columns:repeat(3,1fr); gap:12px; margin-top:12px">
          <div class="test">Customer churn pipeline — SQL + Python ETL</div>
          <div class="test">Executive sales dashboard — Power BI / Looker</div>
          <div class="test">NLP topic model for reviews — prototype</div>
        </div>
      </section>

      <section id="about" style="margin-top:28px">
        <h2>About CloudTech</h2>
        <p style="color:var(--muted)">We are a small team of data practitioners who build tools and teach product-led analytics. Our goal: make analytics practical and useful — not just notebooks. We work with startups and teams across EMEA and remotely worldwide.</p>
      </section>

      <section style="margin-top:28px">
        <h2>Testimonials</h2>
        <div class="testimonials">
          <div class="test">“Great hands-on training — we shipped a dashboard in two weeks.” — Product Lead, Fintech</div>
          <div class="test">“The interns delivered usable analyses and hiring-ready skills.” — Head of Analytics, Marketplace</div>
        </div>
      </section>

      <section id="contact" style="margin-top:28px">
        <h2>Get in touch</h2>
        <p style="color:var(--muted)">Email: <a href="mailto:hi@cloudtechanalytics.com">hi@cloudtechanalytics.com</a> • GitHub: <a href="https://github.com/cloudtech-analytics">github.com/cloudtech-analytics</a></p>

        <div style="margin-top:12px">
          <a class="cta-primary" href="#signup">Request a quote / schedule intro</a>
        </div>
      </section>

    </main>

    <footer>
      <div style="display:flex; gap:12px; align-items:center">
        <div style="display:flex; align-items:center; gap:10px">
          <div class="logo" style="width:40px;height:40px;border-radius:10px">CT</div>
          <div style="font-size:14px">CloudTech Analytics</div>
        </div>
        <div style="color:var(--muted); font-size:13px">© CloudTech Analytics — 2025</div>
      </div>
      <div style="color:var(--muted); font-size:13px">Built with ❤️ • <a href="#" style="color:var(--muted);text-decoration:underline">Privacy</a></div>
    </footer>
  </div>
</body>
</html>
