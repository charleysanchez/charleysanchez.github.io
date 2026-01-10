---
title: About
permalink: /about/
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<button id="theme-toggle">🌙 Dark</button>

## About Me

I'm a machine learning researcher focused on building systems that strengthen the information pathways clinicians depend on. Currently a **research volunteer in Prof. Wenbo Wu's lab at Johns Hopkins**, working on causal inference for healthcare and privacy-preserving clinical NLP.

I hold an **M.Eng. from UCLA** (AI specialization) and a **B.S. in Physics from UCSB**. My path to ML wasn't linear — I explored several majors before settling on physics, then worked in a diagnostic lab where I saw firsthand how automation and data integrity shape clinical decisions. That experience is what pushed me toward research that improves patient care.

---

## Research Focus

<div class="experience-card">
  <h4>Causal Inference for Healthcare</h4>
  <ul>
    <li>Using Double-Debiased Machine Learning to estimate treatment effects from observational health data</li>
    <li>Building evaluation frameworks for deep learning architectures as nuisance models</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Privacy-Preserving Clinical NLP</h4>
  <ul>
    <li>Designing federated learning systems for LLMs to extract Social Determinants of Health from decentralized clinical notes</li>
    <li>Ensuring HIPAA compliance while enabling learning from sensitive patient data</li>
  </ul>
</div>

<div class="experience-card">
  <h4>Embedded Vision Systems</h4>
  <ul>
    <li>Real-time privacy-aware perception on edge devices (Jetson Orin Nano)</li>
    <li>Co-developed Argus for delivery robot privacy (ICRA 2026 submission)</li>
  </ul>
</div>

---

## Background

My background across physics, clinical work, and ML research gives me a practical perspective for creating impactful tools. In the diagnostic lab, I verified orders and turnaround times for patient samples in Epic — computing stopped feeling abstract when I saw how small design choices could affect patient care.

At UCLA, I worked with Prof. Nader Sehatbakhsh on embedded ML with privacy protections, learning that computing systems are shaped by strict demands for data protection and real-time deployment.

---

## Let's Connect

I'm actively exploring PhD opportunities where I can work alongside clinicians and researchers to build systems that genuinely improve how care is delivered.

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
