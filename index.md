---
layout: default
title: "Mohammed Laroussi — Resume"
---

<div class="header">
  <div>
    <h1>{{ site.data.resume.name }}</h1>
    <div class="subtitle">{{ site.data.resume.title }}</div>
    <div class="meta">{{ site.data.resume.location }} · <a href="mailto:{{ site.data.resume.email }}">{{ site.data.resume.email }}</a></div>
  </div>
</div>

<hr/>

{{ site.data.resume.summary }}

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
  <h2>Selected Projects</h2>
  <ul class="compact">
    {% for p in site.data.resume.projects %}
    <li><strong><a href="{{ p.url }}">{{ p.name }}</a></strong> — {{ p.desc }}</li>
    {% endfor %}
  </ul>
</section>

<section>
  <h2>Skills</h2>
  <ul class="tags">
    {% for s in site.data.resume.skills %}<li>{{ s }}</li>{% endfor %}
  </ul>
</section>

<section>
  <h2>Education</h2>
  <ul class="compact">
    {% for e in site.data.resume.education %}<li>{{ e.what }} — {{ e.where }} {{ e.extra }}</li>{% endfor %}
  </ul>
</section>

<section>
  <h2>Certifications</h2>
  <ul class="compact">
    {% for c in site.data.resume.certs %}<li>{{ c }}</li>{% endfor %}
  </ul>
</section>

<section>
  <h2>Languages</h2>
  {{ site.data.resume.languages | join: ", " }}
</section>

<section>
  <h2>Interests</h2>
  {{ site.data.resume.interests | join: " · " }}
</section>

---

*Links:* {% for l in site.data.resume.links %}[{{ l.label }}]({{ l.url }}){% if forloop.last == false %} · {% endif %}{% endfor %}
