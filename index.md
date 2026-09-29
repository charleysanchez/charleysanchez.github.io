---
layout: default
---

<section class="intro">
  <img class="portrait" src="{{ '/assets/img/charley-portrait.jpg' | relative_url }}" alt="Photo of Charley Sanchez" width="480" height="600">
  <div class="intro-text">
    <h1>Charley Sanchez</h1>
    <p class="role">PhD student, Computer Science<br>University of Maryland, Baltimore County</p>
    <p>I'm a PhD student at UMBC, where I work with <a href="https://leetton.github.io/">Prof. Dong Li</a> in the <a href="https://leetton.github.io/fsi/">Future Sensing and Interaction (FSI) Lab</a>. I study the security of foundation models for physiological signals such as EEG, ECG, and wearable data. My current work examines how multimodal health models respond to realistic sensor faults and attacks, and how their design choices shape the damage.</p>
    <p>Before UMBC, I worked on mental health modeling from wearable data with Prof. Anind K. Dey at Georgia Tech, causal machine learning with Prof. Wenbo Wu at Johns Hopkins, and privacy-preserving perception with Prof. Nader Sehatbakhsh at UCLA, where I did my M.Eng. I have a B.S. in Physics from UCSB, and after graduating I worked in a clinical diagnostic lab, which is a big part of why I ended up in healthcare ML.</p>
    <p class="contact">
      <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
      <a href="{{ '/assets/docs/Charley_Sanchez_CV.pdf' | relative_url }}">CV</a>
      <a href="https://github.com/charleysanchez">GitHub</a>
      <a href="https://www.linkedin.com/in/charley-sanchez-034745297/">LinkedIn</a>
    </p>
  </div>
</section>

## News {#news}

<ul class="dated">
{% for item in site.data.news %}
  <li><span class="date">{{ item.date }}</span><span>{{ item.text | markdownify | remove: '<p>' | remove: '</p>' | strip }}</span></li>
{% endfor %}
</ul>

## Research {#research}

### Robustness of multimodal physiological foundation models
<p class="meta">UMBC, with Prof. Dong Li &middot; 2026 to present</p>

Foundation models trained on large collections of biosignals, such as EEG, ECG, EOG, and EMG, are increasingly proposed for clinical and wearable health monitoring. These systems combine several sensors, so an attacker, or simply a faulty electrode, can target a single input stream rather than the whole model. My research builds a threat-model-driven evaluation of these systems: realistic attacks defined at the level of the physical signal, applied consistently across models with different architectures, and measured with statistically careful, subject-level evaluation. The goal is to understand which design decisions make multimodal health models fragile or resilient, and what that means for deploying them safely.

<p class="meta">Adversarial machine learning &middot; Health AI security &middot; Multimodal fusion &middot; Biosignals &middot; Sleep staging</p>

### AI for mental health
<p class="meta">Georgia Tech, with Prof. Anind K. Dey &middot; 2026</p>

I built modeling pipelines for mental health assessment from wearable and behavioral time-series data. I investigated encoding the time series as images (Markov Transition Fields and Gramian Angular Fields) so convolutional and multimodal models could learn from them, and designed a gradient-boosted feature selection step to keep CNN training focused when data was limited. I finished the project and handed off the codebase and documentation to the next research cohort.

### Causal machine learning
<p class="meta">Johns Hopkins, with Prof. Wenbo Wu &middot; 2025–2026</p>

Double machine learning estimates treatment effects by first fitting flexible "nuisance" models, and I studied how the choice of deep architecture for those models (ResMLP, DCN, Transformers) affects the bias, variance, and stability of multi-treatment effect estimates. Across 500–2,000+ configurations, residual MLP blocks introduced the least covariate distortion, and a better-designed gamma model recovered true treatment effects 10–22% more accurately in nonlinear synthetic settings. I also started a literature review on cost-supervised embeddings of diagnosis codes (ICD/CPT) for estimating patient costs in Medicare Advantage plans.

### Privacy-preserving perception
<p class="meta">UCLA, with Prof. Nader Sehatbakhsh &middot; 2025</p>

In the Secure Systems and Architectures Lab, I worked on real-time face anonymization for camera-equipped robots, with Nokia Bell Labs as an industry partner. On a Jetson Orin Nano, I designed mosaic and noise-based anonymization that cut compute by over 92% while keeping the visual signal navigation depends on, and built the evaluation pipeline against Segment Anything masks. This work led to the Argus manuscript below.

## Papers and reports {#papers}

<ol class="papers">
{% for p in site.data.papers %}
  <li>
    <span class="paper-title">{{ p.title }}</span>
    <span class="authors">{{ p.authors | replace: 'C. Sanchez', '<strong>C. Sanchez</strong>' }}</span>
    <span class="venue">{{ p.venue }}{% if p.links %}{% for l in p.links %} <a href="{{ l[1] | relative_url }}">[{{ l[0] }}]</a>{% endfor %}{% endif %}</span>
  </li>
{% endfor %}
</ol>

## Projects {#projects}

<ul class="projects">
{% for p in site.data.projects %}
  <li>
    <img src="{{ p.image | relative_url }}" alt="" width="480" height="360" loading="lazy">
    <div>
      <h3>{{ p.title }}</h3>
      <p>{{ p.description }}</p>
      <p class="meta">{{ p.tech }}{% for l in p.links %} &middot; <a href="{{ l[1] | relative_url }}">{{ l[0] }}</a>{% endfor %}</p>
    </div>
  </li>
{% endfor %}
</ul>

## Experience {#experience}

<ul class="dated">
  <li>
    <span class="date">2026</span>
    <div><strong>Graduate Researcher</strong>, Georgia Institute of Technology<br>
    Prof. Anind K. Dey's lab. Mental health assessment from wearable and behavioral time-series data.</div>
  </li>
  <li>
    <span class="date">2026</span>
    <div><strong>Contracted Software Consultant</strong>, Econ One Research<br>
    Designed and deployed a self-hosted LLM system so the firm's expert witness work on antitrust cases could use LLMs without sending data to outside APIs. Served Qwen and Gemma models with vLLM, LiteLLM, and Open WebUI in Docker.</div>
  </li>
  <li>
    <span class="date">2025–2026</span>
    <div><strong>Research Volunteer</strong>, Johns Hopkins University<br>
    Prof. Wenbo Wu's lab. Double machine learning with deep nuisance models.</div>
  </li>
  <li>
    <span class="date">2025</span>
    <div><strong>Graduate Researcher</strong>, UCLA<br>
    Secure Systems and Architectures Lab, Prof. Nader Sehatbakhsh. Privacy-preserving perception on embedded hardware.</div>
  </li>
  <li>
    <span class="date">2024</span>
    <div><strong>Software Engineer</strong>, Econ One Research<br>
    Built a PostgreSQL document system for litigation discovery data (about 40% faster queries) and a multithreaded ingestion pipeline with 3x the throughput.</div>
  </li>
  <li>
    <span class="date">2023–2024</span>
    <div><strong>Lab Assistant</strong>, Pacific Diagnostic Laboratories<br>
    Processed 500+ specimens a day and tracked orders and results in Epic. This is where I first saw how much software choices affect patient care.</div>
  </li>
</ul>

## Education {#education}

<ul class="dated">
  <li>
    <span class="date">2026–</span>
    <div><strong>Ph.D., Computer Science</strong>, University of Maryland, Baltimore County</div>
  </li>
  <li>
    <span class="date">2025</span>
    <div><strong>M.Eng., Artificial Intelligence</strong>, UCLA<br>
    UCLA M.Eng. Fellowship (2024).</div>
  </li>
  <li>
    <span class="date">2023</span>
    <div><strong>B.S., Physics</strong>, UC Santa Barbara</div>
  </li>
</ul>
