---
title: "HiPCastor - Publications"
layout: gridlay
excerpt: "HiPCastor -- Publications."
sitemap: true
permalink: /publications/
---


<p class="text-center">Highlighted recent publications from the group.</p>

<p class="text-center"><a href="#full-publication-list" class="hpc-arrow-link">All publications</a></p>


{% for publi in site.data.publist %}
{% if publi.highlight == 1 %}
<div class="hpc-card hpc-featured{% if publi.link.url != "" %} hpc-pub-card{% endif %}" markdown="0">
  {% if publi.link.url != "" %}<a href="{{ publi.link.url }}" class="stretched-link" aria-label="{{ publi.title }}"></a>{% endif %}
  <div class="hpc-featured-media">
    <img src="{{ '/images/pubpic/' | append: publi.image | relative_url }}" class="hpc-featured-img" width="220" loading="lazy" decoding="async" alt="{{ publi.title }}" />
  </div>
  <div class="hpc-featured-body">
    <span class="kbd hpc-featured-series">{{ publi.series }}</span>
    <strong class="pubtit">{{ publi.title }}</strong>
    <p class="hpc-featured-desc">{{ publi.description }}</p>
    <p class="hpc-featured-authors"><em>{{ publi.authors }}</em></p>
    <p class="hpc-featured-venue">In {{ publi.link.display }}</p>
    {% if publi.news1 %}<p class="text-danger hpc-featured-news"><strong>{{ publi.news1 }}</strong></p>{% endif %}
    {% if publi.news2 %}<p class="hpc-featured-news">{{ publi.news2 }}</p>{% endif %}
  </div>
</div>
{% endif %}
{% endfor %}

<p> &nbsp; </p>

## Full Publication List

{% for publi in site.data.publist %}
{% if publi.link.url != "" %}
<div class="hpc-item hpc-pub-card" markdown="0">
  <a href="{{ publi.link.url }}" class="stretched-link" aria-label="{{ publi.title }}"></a>
  <strong class="pubtit">{{ publi.title }}</strong>
  <p class="mb-0"><kbd>{{ publi.series }}</kbd> <em>{{ publi.authors }}</em></p>
  {% include instbadges.html publi=publi %}
</div>
{% else %}
<div class="hpc-item" markdown="0">
  <strong class="pubtit">{{ publi.title }}</strong>
  <p class="mb-0"><kbd>{{ publi.series }}</kbd> <em>{{ publi.authors }}</em></p>
  {% include instbadges.html publi=publi %}
</div>
{% endif %}
{% endfor %}
