---
title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<button id="theme-toggle">🌙 Dark</button>

<div class="hero fade-in">
  <img class="hero-pic" src="/assets/img/charley.jpeg" alt="Charley Sanchez portrait">
  <div class="hero-text">
    <h1>{{ site.title }}</h1>
    <p class="hero-tagline">ML Researcher focused on Healthcare & Privacy</p>
    <p class="hero-bio">I work on ML systems that help clinicians make better decisions. Currently in Prof. Wenbo Wu's lab at Johns Hopkins, focusing on causal inference and privacy-preserving clinical NLP.</p>
    <p class="hero-links">
      <a href="/about/">📄 About</a>
      <a href="/assets/docs/Charley_Sanchez_CV.pdf" target="_blank">📋 CV</a>
      <a href="/assets/docs/Charley_Sanchez_Resume.pdf" target="_blank">📑 Resume</a>
      <a href="https://github.com/charleysanchez" target="_blank">💻 GitHub</a>
      <a href="https://www.linkedin.com/in/charley-sanchez-034745297/" target="_blank">🔗 LinkedIn</a>
    </p>
  </div>
</div>

---

## Research Interests

<div class="research-interests">
  <p>
    I want to build systems that clinicians can actually use: developed with their input, tested in real settings, and refined until they work. My current projects include:
  </p>
  <p>
    <strong>Causal Inference for Healthcare</strong>: Estimating treatment effects from observational health data using Double-Debiased ML.<br>
    <strong>Privacy-Preserving Clinical NLP</strong>: Training LLMs on decentralized clinical notes with federated learning to extract Social Determinants of Health.<br>
    <strong>Embedded Vision Systems</strong>: Real-time, privacy-aware perception on edge devices like the Jetson Orin Nano.
  </p>
</div>

---

## Featured Projects

<ul class="grid">
{% for p in site.data.projects %}
  <li class="card">
    {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
    {% endif %}
    {% if p.type %}
      <span class="project-type">{{ p.type }}</span>
    {% endif %}
    {% if p.venue %}
      <span class="project-venue">{{ p.venue }}</span>
    {% endif %}
    <h3>
      {{ p.title }}
      {% if p.metric %}
        <span class="impact-metric">{{ p.metric }}</span>
      {% endif %}
    </h3>
    <p>{{ p.description }}</p>
    {% if p.tech %}
      <div class="tech-tags">
        {% for t in p.tech %}
          <span class="tech-tag">{{ t }}</span>
        {% endfor %}
      </div>
    {% endif %}
    <p class="links">
      {% if p.repo %}<a href="{{ p.repo }}" target="_blank">Code</a>{% endif %}
      {% if p.demo %}<a href="{{ p.demo }}" target="_blank">Demo</a>{% endif %}
      {% if p.paper %}<a href="{{ p.paper }}" target="_blank">Paper</a>{% endif %}
    </p>
  </li>
{% endfor %}
</ul>

---

## Technical Reports

<ul class="publications-list">
  <li class="publication-item">
    <div class="publication-title">PAVAC: Privacy-Aware Vehicular Autonomous Computation</div>
    <div class="publication-venue">Under review at ICRA 2026</div>
    <div class="publication-links">
      <a href="/assets/docs/AVPrivacy_report.pdf" target="_blank">📄 PDF</a>
      <a href="https://github.com/charleysanchez/AVPrivacy-Jetson" target="_blank">💻 Code</a>
    </div>
  </li>
  <li class="publication-item">
    <div class="publication-title">sEMG Keystroke Recognition with Residual BiLSTM Networks</div>
    <div class="publication-venue">Technical Report, 2025</div>
    <div class="publication-links">
      <a href="/assets/docs/SEmg_report.pdf" target="_blank">📄 PDF</a>
      <a href="https://github.com/charleysanchez/SOTA-4" target="_blank">💻 Code</a>
    </div>
  </li>
  <li class="publication-item">
    <div class="publication-title">Analyzing Spurious Feature Reliance in Pretrained Language Models</div>
    <div class="publication-venue">Technical Report, 2024</div>
    <div class="publication-links">
      <a href="/assets/docs/spurious_report.pdf" target="_blank">📄 PDF</a>
      <a href="https://github.com/metehanberker1/pretrained-encoders-spurious-learning-analysis" target="_blank">💻 Code</a>
    </div>
  </li>
</ul>

---

## Education

<div class="education-card">
  <h4>M.Eng. in Electrical & Computer Engineering</h4>
  <div class="institution">University of California, Los Angeles (UCLA)</div>
  <div class="year">2025</div>
  <div class="details">Specialization in Artificial Intelligence</div>
</div>

<div class="education-card">
  <h4>B.S. in Physics</h4>
  <div class="institution">University of California, Santa Barbara (UCSB)</div>
  <div class="year">2023</div>
</div>

---

## Experience

<div class="experience-card">
  <h4>Research Volunteer</h4>
  <div class="company">Johns Hopkins University, Prof. Wenbo Wu's Lab</div>
  <div class="period">2025 – Present</div>
  <ul>
    <li><strong>Double-Debiased ML:</strong> Built experimental framework studying deep learning architectures as nuisance models in multi-treatment causal inference; found Residual MLP blocks minimize covariate distortion (paper in preparation)</li>
    <li><strong>Federated Clinical NLP:</strong> Designing privacy-preserving system to extract Social Determinants of Health from decentralized clinical notes using federated LLMs</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Graduate Researcher</h4>
  <div class="company">UCLA, Prof. Nader Sehatbakhsh's Lab</div>
  <div class="period">2024 – 2025</div>
  <ul>
    <li>Co-developed <strong>Argus</strong>, a real-time privacy-preserving video system for delivery robots (under review at ICRA 2026)</li>
    <li>Optimized Jetson Orin Nano pipeline for face detection and anonymization with strict latency/memory constraints</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Data Engineer</h4>
  <div class="company">Econ One Research</div>
  <div class="period">2024</div>
  <ul>
    <li>Built PostgreSQL data platform for economic litigation analysis</li>
    <li>Developed multithreaded pipelines for large-scale data ingestion</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Diagnostic Lab Technician</h4>
  <div class="company">Clinical Laboratory</div>
  <div class="period">2023</div>
  <ul>
    <li>Verified orders and turnaround times for patient samples in Epic EHR</li>
    <li>This is where I first saw how software choices affect patient care, which pushed me toward healthcare ML</li>
  </ul>
</div>

---

## Skills & Tools

<div class="skills-grid">
  <div class="skill-category">
    <h3>Machine Learning</h3>
    <div class="skill-pills">
      <span class="skill-pill">PyTorch</span>
      <span class="skill-pill">TensorFlow</span>
      <span class="skill-pill">Transformers</span>
      <span class="skill-pill">GANs</span>
      <span class="skill-pill">Diffusion Models</span>
      <span class="skill-pill">CNNs</span>
      <span class="skill-pill">BiLSTM</span>
    </div>
  </div>
  
  <div class="skill-category">
    <h3>Deployment & Inference</h3>
    <div class="skill-pills">
      <span class="skill-pill">ONNX Runtime</span>
      <span class="skill-pill">TensorRT</span>
      <span class="skill-pill">TorchServe</span>
      <span class="skill-pill">Docker</span>
      <span class="skill-pill">NVIDIA Jetson</span>
      <span class="skill-pill">REST APIs</span>
    </div>
  </div>
  
  <div class="skill-category">
    <h3>Infrastructure</h3>
    <div class="skill-pills">
      <span class="skill-pill">CUDA</span>
      <span class="skill-pill">Multi-GPU HPC</span>
      <span class="skill-pill">GitHub Actions</span>
      <span class="skill-pill">W&B</span>
      <span class="skill-pill">PostgreSQL</span>
      <span class="skill-pill">AWS Bedrock</span>
    </div>
  </div>
  
  <div class="skill-category">
    <h3>Domains</h3>
    <div class="skill-pills">
      <span class="skill-pill">Medical Imaging</span>
      <span class="skill-pill">Privacy-Aware ML</span>
      <span class="skill-pill">NLP</span>
      <span class="skill-pill">Computer Vision</span>
      <span class="skill-pill">Signal Processing</span>
    </div>
  </div>
  
  <div class="skill-category">
    <h3>Languages & Tools</h3>
    <div class="skill-pills">
      <span class="skill-pill">Python</span>
      <span class="skill-pill">C/C++</span>
      <span class="skill-pill">Bash</span>
      <span class="skill-pill">LaTeX</span>
      <span class="skill-pill">Git</span>
      <span class="skill-pill">NumPy</span>
      <span class="skill-pill">Pandas</span>
    </div>
  </div>
</div>

---

## Get in Touch {#contact}

<div class="contact-section">
  <p>I'm always excited to collaborate on impactful ML projects, discuss research ideas, or explore opportunities. Feel free to reach out!</p>
  <div class="contact-links">
    <a href="mailto:charleysanchez7@gmail.com">📧 Email</a>
    <a href="https://github.com/charleysanchez" target="_blank">💻 GitHub</a>
    <a href="https://www.linkedin.com/in/charley-sanchez-034745297/" target="_blank">🔗 LinkedIn</a>
  </div>
</div>

<script>
  const btn = document.getElementById("theme-toggle");
  const root = document.documentElement;

  // load stored preference
  if (localStorage.theme === "dark") {
    root.setAttribute("data-theme", "dark");
    btn.textContent = "☀️ Light";
  }

  btn.addEventListener("click", () => {
    if (root.getAttribute("data-theme") === "dark") {
      root.removeAttribute("data-theme");
      localStorage.theme = "light";
      btn.textContent = "🌙 Dark";
    } else {
      root.setAttribute("data-theme", "dark");
      localStorage.theme = "dark";
      btn.textContent = "☀️ Light";
    }
  });
</script>
