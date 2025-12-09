---
title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<div class="hero">
  <img class="hero-pic" src="/assets/img/charley.jpeg" alt="Charley Sanchez portrait">
  <div class="hero-text">
    <h1>{{ site.title }}</h1>
    <p>Hi, I’m Charley. I build machine learning systems with a focus on reliable, real-time deployment and measurable impact. Welcome to my portfolio.</p>
    <p class="hero-links">
      <a href="/about/">About</a> · 
      <a href="/assets/docs/Charley_Sanchez_CV.pdf" target="_blank">CV</a>
    </p>
  </div>

  <button id="theme-toggle" style="
  margin-left:auto;
  padding: 0.4rem 0.8rem;
  border-radius: 6px;
  border: none;
  cursor: pointer;
  background: #e2e8f0;
  color: #111;
">
  🌙 Dark
</button>

</div>

---

## Projects

<ul class="grid">
{% for p in site.data.projects %}
  <li class="card">
    {% if p.image %}
      <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
    {% endif %}
    <h3>{{ p.title }}</h3>
    <p>{{ p.description }}</p>
    {% if p.tech %}
      <p class="meta">{{ p.tech | join: ' · ' }}</p>
    {% endif %}
    <p class="links">
      {% if p.repo %}<a href="{{ p.repo }}" target="_blank">Code</a>{% endif %}
      {% if p.demo %}{% if p.repo %} · {% endif %}<a href="{{ p.demo }}" target="_blank">Demo</a>{% endif %}
      {% if p.paper %}{% if p.repo or p.demo %} · {% endif %}<a href="{{ p.paper }}" target="_blank">Paper</a>{% endif %}
    </p>
  </li>
{% endfor %}
</ul>



---
## Skills & Tools

<div class="skills">
  <h3>Core ML</h3>
  <p>PyTorch · TensorFlow · Keras · GANs · VAEs · Diffusion Models · Transformers · CNNs · BiLSTM · Segmentation · Object Detection · Spurious Correlation Analysis (BERT, RoBERTa)</p>

  <h3>Deployment</h3>
  <p>Docker · ONNX Runtime · TensorRT · TorchServe · Flask · REST APIs · NVIDIA Jetson (Orin Nano, JetPack)</p>

  <h3>Infrastructure</h3>
  <p>CUDA · Multi-GPU HPC Clusters · GitHub Actions · Weights & Biases · SQL (PostgreSQL) · Data Pipelines</p>

  <h3>Data & Imaging</h3>
  <p>Medical Imaging (BraTS, ChestXray14) · Privacy-Aware Video Anonymization (RGB-D) · OpenCV · NumPy · Pandas · Scikit-learn</p>

  <h3>Software Engineering</h3>
  <p>Python · C · C++ · Bash · LaTeX · Multithreaded Systems (gfserver/gfclient) · Networking · Distributed Systems</p>
</div>

---

## Get in Touch {#contact}

I'm always excited to collaborate on impactful ML projects or discuss new ideas. Feel free to reach out via <a href="mailto:charleysanchez@gmail.com">email</a> or connect on <a href="https://github.com/charleysanchez" target="_blank">GitHub</a> or <a href="https://www.linkedin.com/in/charley-sanchez-034745297/" target="_blank">LinkedIn</a>.

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


