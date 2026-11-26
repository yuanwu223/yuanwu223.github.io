---
title: "Publications"
layout: page
permalink: /publications/
---

# Publications

<input type="text" class="pub-search" id="pubSearch" placeholder="Filter by title, author, or year...">

{% comment %}
  Each section appears only when ref.bib has an entry of that type:
    @inproceedings -> Conference Papers
    @unpublished   -> Preprints and Working Papers
    @article       -> Journal Articles
{% endcomment %}
{% capture proceedings %}{% bibliography --query @inproceedings %}{% endcapture %}
{% capture preprints %}{% bibliography --query @unpublished %}{% endcapture %}
{% capture journals %}{% bibliography --query @article %}{% endcapture %}

<div class="section-card" id="pubList">
{% if proceedings contains "pub-entry" %}
<h2>Conference Papers</h2>

{{ proceedings }}
{% endif %}

{% if preprints contains "pub-entry" %}
<h2>Preprints and Working Papers</h2>

{{ preprints }}
{% endif %}

{% if journals contains "pub-entry" %}
<h2>Journal Articles</h2>

{{ journals }}
{% endif %}
</div>
