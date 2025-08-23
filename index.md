---
layout: default
title: "Mohammed Laroussi — Resume"
---

<div class="header">
  <div>
    <h1>{{ site.data.resume.name }}</h1>
    <div class="subtitle">{{ site.data.resume.title }}</div>
    <div class="meta">{{ site.data.resume.location }} · <a href="mailto:{{ site.data.resume.email }}">{{ site.data.resume.email }}</a> · {{ site.data.resume.phone }}</div>
  </div>
</div>

<hr/>

<div class="intro">{{ site.data.resume.summary }}</div>

<div class="two-col">
  <div class="col">

  <section>
    <h2>Core</h2>
    <ul class="compact tinyindent">
      {% for c in site.data.resume.core_competencies %}<li>{{ c }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2>Skills</h2>
    <ul class="tags">
      {% for s in site.data.resume.skills %}<li>{{ s }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2>Languages</h2>
    <ul class="tags">
      {% for l in site.data.resume.languages %}<li>{{ l.name }} — {{ l.level }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2>Interests</h2>
    <ul class="tags">
      {% for i in site.data.resume.interests %}<li>{{ i }}</li>{% endfor %}
    </ul>
  </section>

  <section>
    <h2>Certifications</h2>
    <ul class="compact tinyindent">
      {% for c in site.data.resume.certifications %}<li>{{ c }}</li>{% endfor %}
    </ul>
  </section>

  <section class="no-print">
    <h2>Links</h2>
    <div class="small">{% for l in site.data.resume.links %}<a href="{{ l.url }}">{{ l.label }}</a>{% if forloop.last == false %} · {% endif %}{% endfor %}</div>
  </section>

  </div>
  <div class="col">

  <section>
    <h2>Experience</h2>
    {% for job in site.data.resume.experience %}
    <div class="item">
      <span class="role">{{ job.role }}</span> — <span class="company">{{ job.company }}</span> · <span class="dates">{{ job.dates }}</span>
      <ul class="compact">
        {% for b in job.bullets %}<li>{{ b }}</li>{% endfor %}
      </ul>
    </div>
    {% endfor %}
  </section>

  <section>
    <h2>Education</h2>
    <ul class="compact">
      {% for e in site.data.resume.education %}<li>{{ e.degree }} — {{ e.institution }}</li>{% endfor %}
    </ul>
  </section>

  </div>
</div>
