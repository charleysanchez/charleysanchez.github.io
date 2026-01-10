---
title: About
permalink: /about/
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<button id="theme-toggle">🌙 Dark</button>

## About Me

I'm a machine learning engineer and researcher currently working as a **research volunteer in Prof. Wenbo Wu's lab at Johns Hopkins University**. I focus on making models *useful*: clean training/evaluation pipelines, fast and reliable serving, and clear metrics that connect to real-world impact.

I hold an **M.Eng. from UCLA** (specializing in AI) and a **B.S. in Physics from UCSB**. My work spans the full ML stack—from model development and experimentation to edge deployment and production systems. I'm particularly interested in problems at the intersection of **efficient inference**, **medical imaging**, and **robust NLP**.

---

## What I Do

<div class="experience-card">
  <h4>Real-Time ML Systems</h4>
  <ul>
    <li>Built a real-time face anonymization system on NVIDIA Jetson (SCRFD + TensorRT) achieving ~24 FPS at 640×480</li>
    <li>Created evaluation harness against SAM with Dice/Recall metrics and environment/face-count aggregates</li>
    <li>Developed controllable RAG systems with audit logging and human-in-the-loop review</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Production Data Engineering</h4>
  <ul>
    <li>Shipped data systems at Econ One Research (PostgreSQL platform, multithreaded processing)</li>
    <li>Implemented accurate billing integrations with comprehensive testing</li>
    <li>Built data pipelines for large-scale economic litigation analysis</li>
  </ul>
</div>

---

## Research Interests

I'm excited about research that bridges the gap between ML capabilities and practical deployment:

- **Efficient Inference**: Quantization, pruning, and runtime optimization for edge devices
- **Medical Imaging**: Robust segmentation and privacy-preserving analysis
- **Robust NLP**: Understanding and mitigating spurious correlations in language models
- **Privacy-Aware ML**: On-device processing and anonymization techniques

---

## Let's Connect

I'm actively exploring PhD opportunities and industry roles where I can push the boundaries of practical ML systems.

<div class="contact-links" style="margin-top: 1.5rem;">
  <a href="mailto:charleysanchez7@gmail.com">📧 Email</a>
  <a href="https://github.com/charleysanchez" target="_blank">💻 GitHub</a>
  <a href="https://www.linkedin.com/in/charley-sanchez-034745297/" target="_blank">🔗 LinkedIn</a>
</div>

<script>
  const btn = document.getElementById("theme-toggle");
  const root = document.documentElement;
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
