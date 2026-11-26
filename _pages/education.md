---
title: "Education"
layout: page
permalink: /education/
---

# Education

{% comment %}
  Entries come from `education` in _data/pi.yml, newest first.
  Each entry needs: institution, degree, years. Optional: location.
{% endcomment %}
<div class="section-card" markdown="0">
{% for edu in site.data.pi[0].education %}
<div{% unless forloop.first %} style="margin-top: var(--space-6); padding-top: var(--space-6); border-top: 1px solid var(--border-color);"{% endunless %}>
<div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: baseline; gap: 0 var(--space-6);">
<h3 style="margin: 0; font-size: 1.25rem;">{{ edu.institution }}</h3>
<span style="color: var(--text-secondary); font-size: 0.9375rem;">{{ edu.years | replace: "-", "&#8211;" }}</span>
</div>
<div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: baseline; gap: 0 var(--space-6); margin-top: var(--space-1);">
<span>{{ edu.degree }}</span>
{% if edu.location %}<span style="color: var(--text-secondary); font-size: 0.9375rem;">{{ edu.location }}</span>{% endif %}
</div>
</div>
{% endfor %}
</div>

{% if site.data.grants %}
<div class="section-card">
<h3>Grants</h3>
<ul>
{% for grant in site.data.grants %}
<li>{{ grant.name }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.awards %}
<div class="section-card">
<h3>Awards</h3>
<ul>
{% for award in site.data.awards %}
<li>{{ award.name | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
</div>
{% endif %}

{% if site.data.funders %}
<div class="section-card">
<h4>Sponsors</h4>
<div class="sponsor-logos" style="display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: var(--space-6);">
{% for funder in site.data.funders %}
<a href="{{ funder.url }}" target="_blank"><img src="{{ funder.image | prepend: '/images/' | relative_url }}" alt="Funder logo" style="max-height: 80px; max-width: 200px; border-radius: 0;" loading="lazy"></a>
{% endfor %}
</div>
</div>
{% endif %}
