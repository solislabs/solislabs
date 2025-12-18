<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Solis Labs — Audiovisual Studio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0e0f12;
      --bg-soft: #14161b;
      --text: #e5e7eb;
      --text-dim: #9ca3af;
      --accent: #8b8f99;
      --line: rgba(255,255,255,0.08);
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      background: radial-gradient(1200px 600px at 70% -10%, #1b1e26, var(--bg));
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* subtle stars */
    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background-image: radial-gradient(1px 1px at 20% 30%, rgba(255,255,255,.15), transparent 40%),
                        radial-gradient(1px 1px at 80% 70%, rgba(255,255,255,.12), transparent 40%),
                        radial-gradient(1px 1px at 50% 10%, rgba(255,255,255,.08), transparent 40%);
      pointer-events: none;
      z-index: 0;
    }

    header, section, footer {
      position: relative;
      z-index: 1;
    }

    header {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 4rem 1.5rem;
    }

    header h1 {
      font-size: clamp(2.5rem, 5vw, 4rem);
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    header p {
      max-width: 680px;
      margin: 0 auto 2rem;
      color: var(--text-dim);
      font-size: 1.05rem;
    }

    .scroll {
      font-size: 0.8rem;
      color: var(--text-dim);
      letter-spacing: 0.2em;
      text-transform: uppercase;
      opacity: 0.6;
    }

    section {
      padding: 5rem 1.5rem;
      border-top: 1px solid var(--line);
      background: linear-gradient(180deg, transparent, rgba(255,255,255,0.01));
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
    }

    h2 {
      font-size: 1.6rem;
      font-weight: 500;
      margin-bottom: 1.5rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .about {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2rem;
    }

    .card {
      background: var(--bg-soft);
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 2rem;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 20px 60px rgba(0,0,0,0.35);
    }

    .card h3 {
      font-weight: 500;
      margin-bottom: 0.8rem;
    }

    .card p {
      color: var(--text-dim);
      font-size: 0.95rem;
    }

    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
    }

    .service {
      padding: 1.5rem;
      border-left: 2px solid var(--accent);
      background: rgba(255,255,255,0.02);
    }

    .service span {
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      color: var(--text-dim);
      text-transform: uppercase;
    }

    .service h4 {
      margin: 0.5rem 0 0.6rem;
      font-weight: 500;
    }

    .service p {
      font-size: 0.9rem;
      color: var(--text-dim);
    }

    footer {
      padding: 3rem 1.5rem;
      border-top: 1px solid var(--line);
      text-align: center;
      color: var(--text-dim);
      font-size: 0.85rem;
    }

    /* reveal animation */
    .reveal {
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.8s ease;
    }
	
	.video-wrapper {
	  position: relative;
	  padding-top: 56.25%; /* 16:9 */
	}

	.video-wrapper iframe {
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	}

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>
<body>

  <header>
    <div>
      <h1>Solis Labs</h1>
      <p>
        An independent audiovisual studio specializing in the creation of contemporary and engaging media projects.
      </p>
      <div class="scroll">Scroll</div>
    </div>
  </header>

  <section>
    <div class="container reveal">
      <h2>Showreel</h2>
		<div class="video-wrapper">
		<iframe 
		  src="https://youtube.com/embed/QM47jBr99RQ"
		  frameborder="0"
		  allow="fullscreen; picture-in-picture"
		  allowfullscreen>
		</iframe>
	</div>
   </section>

  <section>
    <div class="container reveal">
      <h2>What is Solis Labs</h2>
      <div class="about">
        <div class="card">
          <h3>One-person studio</h3>
          <p>
            Solis Labs is a solo studio built around a unified creative workflow.
            One mind, one vision, full control over image, sound and rhythm.
          </p>
        </div>
        <div class="card">
          <h3>System thinking</h3>
          <p>
            Projects are designed as systems, not isolated assets.
            Visuals, animation and audio are developed together to reinforce meaning and mood.
          </p>
        </div>
        <div class="card">
          <h3>Experimental mindset</h3>
          <p>
            Inspired by sci-fi, minimalism and digital space.
            Each project is treated as a small universe with its own rules.
          </p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container reveal">
      <h2>Core Capabilities</h2>
      <div class="services">
        <div class="service">
          <span>01</span>
          <h4>Video & Editing</h4>
          <p>Rhythm-driven editing, narrative pacing, visual clarity.</p>
        </div>
        <div class="service">
          <span>02</span>
          <h4>Sound & Music</h4>
          <p>Sound design, music composition, atmosphere and emotion.</p>
        </div>
        <div class="service">
          <span>03</span>
          <h4>Motion & 2D/3D</h4>
          <p>Motion graphics, basic 3D scenes, abstract animation.</p>
        </div>
        <div class="service">
          <span>04</span>
          <h4>Audiovisual Systems</h4>
          <p>Integrated pipelines for games, trailers, and experimental media.</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container reveal">
      <h2>Selected Works</h2>
      <div class="about">
        <div class="card">
          <h3>Video Showcase</h3>
          <p>YouTube / Vimeo embed placeholder</p>
          <div style="margin-top:1rem; aspect-ratio:16/9; background:rgba(255,255,255,0.04); border:1px dashed var(--line); border-radius:10px; display:flex; align-items:center; justify-content:center; color:var(--text-dim); font-size:0.85rem;">Embed video here</div>
        </div>
        <div class="card">
          <h3>Visual Frames</h3>
          <p>Image or gallery placeholder</p>
          <div style="margin-top:1rem; height:200px; background:rgba(255,255,255,0.04); border:1px dashed var(--line); border-radius:10px; display:flex; align-items:center; justify-content:center; color:var(--text-dim); font-size:0.85rem;">Insert image</div>
        </div>
        <div class="card">
          <h3>Experimental Piece</h3>
          <p>Another video or visual experiment</p>
          <div style="margin-top:1rem; aspect-ratio:16/9; background:rgba(255,255,255,0.04); border:1px dashed var(--line); border-radius:10px; display:flex; align-items:center; justify-content:center; color:var(--text-dim); font-size:0.85rem;">Embed video here</div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container reveal">
      <h2>Contact</h2>
      <div class="about">
        <div class="card">
          <h3>Get in touch</h3>
          <p>
            Solis Labs is open for collaboration, internships and media projects.
            <br><br>
            <strong>Email:</strong> solis.iso@hotmail.com<br>
            <strong>Location:</strong> Germany / Remote
          </p>
        </div>
        <div class="card">
          <h3>Links</h3>
          <p>
            <a href="https://www.youtube.com/channel/UC4uI1v3uI9xhMdRSCdIs3Zw" style="color:var(--text); text-decoration:none;">YouTube</a><br>
            <a href="https://panzoid.com/creations/search?q=user:Aiva" style="color:var(--text); text-decoration:none;">Panzoid</a><br>
            <a href="https://okvpd.newgrounds.com/" style="color:var(--text); text-decoration:none;">Newgrounds</a><br>
            <a href="https://github.com/solislabs" style="color:var(--text); text-decoration:none;">GitHub</a>
          </p>
        </div>
      </div>
    </div>
  </section>

  <footer>
    © Solis Labs — Independent Audiovisual Studio
  </footer>

  <script>
    const reveals = document.querySelectorAll('.reveal');

    function revealOnScroll() {
      const trigger = window.innerHeight * 0.85;
      reveals.forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < trigger) el.classList.add('active');
      });
    }

    window.addEventListener('scroll', revealOnScroll);
    revealOnScroll();
  </script>

</body>
</html>
