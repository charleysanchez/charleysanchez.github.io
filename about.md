---
title: About
permalink: /about/
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<button id="theme-toggle">🌙 Dark</button>

## About Me

I'm a machine learning researcher working on systems that help clinicians make better decisions. Right now I'm in Prof. Wenbo Wu's lab at Johns Hopkins, focused on causal inference and privacy-preserving NLP for clinical text.

I have an M.Eng. from UCLA (AI) and a B.S. in Physics from UCSB. My route to ML was indirect. I tried a few majors, landed on physics, then worked in a diagnostic lab after graduating. That job changed how I think about software: I verified orders and turnaround times in Epic, and I saw how small system bugs could delay patient care. After that, building reliable healthcare tools stopped being an abstract goal.

---

## What I'm Working On

<div class="experience-card">
  <h4>Causal Inference</h4>
  <ul>
    <li>Estimating treatment effects from observational health data with Double-Debiased ML</li>
    <li>Testing how different neural network architectures perform as nuisance models</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Clinical NLP</h4>
  <ul>
    <li>Designing federated systems so LLMs can learn from clinical notes across hospitals without sharing raw data</li>
    <li>Extracting Social Determinants of Health while staying HIPAA compliant</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Embedded Vision</h4>
  <ul>
    <li>Real-time face anonymization on Jetson hardware</li>
    <li>Co-developed Argus, a privacy system for delivery robots (ICRA 2026 submission)</li>
  </ul>
</div>

---

## Background

Before grad school, I worked in a diagnostic lab. I'd verify sample orders and check turnaround times in Epic. It sounds routine, but when something went wrong with the software, patients waited longer. That stuck with me.

At UCLA, I worked with Prof. Nader Sehatbakhsh on embedded ML with privacy constraints. The project taught me that real-world systems have to respect memory limits, latency budgets, and data protection rules all at once.

---

## What's Next

I'm looking for PhD programs where I can work closely with clinicians and build tools that actually get used in practice. If that sounds interesting to you, reach out.

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
