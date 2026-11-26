---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub"><a href="https://cmor.rice.edu/" target="_blank" rel="noopener">Department of Computational Applied Mathematics and Operations Research</a><br><a href="https://www.rice.edu/" target="_blank" rel="noopener">Rice University</a></p>

<div class="chip-container" markdown="0">
<span class="chip chip-muted">LLM</span>
<span class="chip chip-muted">Uncertainty Quantification</span>
<span class="chip chip-muted">Bias and Fairness</span>
</div>

My research asks what happens to large language models after pre-training, when they are distilled, compressed, and fine-tuned, and whether they stay reliable along the way.
A question that runs through my work is model multiplicity: equally capable models often solve the same task through different reasoning, and I am interested in whether that diversity can be put to use.
I also study calibration, so that a model's confidence says something true about its answers, and the safety of the reasoning traces that models produce.

Previously, I received my master's degree in Computational and Applied Mathematics from Rice University in 2026 and my bachelor's degree in Mathematics and Applied Mathematics from Tongji University in 2024.

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Selected publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>
{% endif %}
