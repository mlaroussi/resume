---
layout: default
title: "Mohammed Laroussi — Resume"
---

<div class="header">
  <div>
    <h1>{{ site.data.resume.name }}</h1>
    <div class="subtitle">{{ site.data.resume.title }}</div>
    <div class="meta">
      <i class="bi bi-geo-alt"></i> {{ site.data.resume.location }} ·
      <a href="mailto:{{ site.data.resume.email }}"><i class="bi bi-envelope"></i> {{ site.data.resume.email }}</a> ·
      <i class="bi bi-telephone"></i> {{ site.data.resume.phone }}
      {% assign li = site.data.resume.links | where: "label", "LinkedIn" | first %}
      <span class="no-print"> · <a href="{{ li.url }}"><i class="bi bi-linkedin"></i> LinkedIn</a></span>
    </div>
  </div>
  <div class="no-print header-actions">
    <button onclick="window.print()" class="print-btn"><i class="bi bi-download"></i> Download PDF</button>
  </div>
</div>

<hr/>

<div class="intro">{{ site.data.resume.summary }}</div>

<div class="two-col">
  <div class="col">

  <section>
    <h2><i class="bi bi-cpu"></i> Core</h2>
    <ul class="compact">
      {% for c in site.data.resume.core_competencies %}<li>{{ c }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2><i class="bi bi-terminal"></i> Skills</h2>
    <ul class="tags">
      {% for s in site.data.resume.skills %}<li>{{ s }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2><i class="bi bi-patch-check"></i> Certifications</h2>
    <ul class="compact">
      {% for c in site.data.resume.certifications %}<li>{{ c }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2><i class="bi bi-translate"></i> Languages</h2>
    <ul class="tags">
      {% for l in site.data.resume.languages %}<li>{{ l.name }} — {{ l.level }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2><i class="bi bi-heart"></i> Interests</h2>
    <ul class="tags">
      {% for i in site.data.resume.interests %}<li>{{ i }}</li>{% endfor %}
    </ul>
  </section>

  

  </div>
  <div class="col">

  <section>
    <h2><i class="bi bi-briefcase"></i> Experience</h2>
    {% for job in site.data.resume.experience %}
    <div class="item">
      <span class="role">{{ job.role }}</span> <span class="company">{{ job.company }}</span> · <span class="dates">{{ job.dates }}</span>
      <ul class="compact">
        {% for b in job.bullets %}<li>{{ b }}</li>{% endfor %}
      </ul>
    </div>
    {% endfor %}
  </section>

  <section>
    <h2><i class="bi bi-mortarboard"></i> Education</h2>
    <ul class="compact">
      {% for e in site.data.resume.education %}<li>{{ e.degree }} — {{ e.institution }}</li>{% endfor %}
    </ul>
  </section>

  </div>
</div>
