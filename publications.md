---
layout: default
title: Publications
permalink: /publications/
---

<h1>Publications</h1>
<p class="page-note">{{ site.data.publications | size }} entries · newest first</p>

<ol class="pub-list" aria-label="Publications, newest first">
{%- for pub in site.data.publications %}
  <li class="pub">
    <p class="pub__year">{{ pub.year }}</p>
    <div class="pub__body">
      <h2 class="pub__title">{{ pub.title }}</h2>
      <p class="pub__authors">{% for author in pub.authors %}{% if author == 'Gaofei Shen' %}<strong>{{ author }}</strong>{% else %}{{ author }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}</p>
      <p class="pub__meta">{{ pub.venue }}{% if pub.pages %}<span class="sep" aria-hidden="true">·</span>pp. {{ pub.pages }}{% endif %}</p>
      <ul class="pub__links">
        {%- if pub.doi %}
        <li><a href="https://doi.org/{{ pub.doi }}" aria-label="DOI: {{ pub.doi }}">DOI</a></li>
        {%- endif %}
        {%- if pub.arxiv %}
        <li><a href="https://arxiv.org/abs/{{ pub.arxiv }}" aria-label="arXiv preprint: {{ pub.arxiv }}">arXiv {{ pub.arxiv }}</a></li>
        {%- endif %}
        {%- if pub.code %}
        <li><a href="{{ pub.code }}" aria-label="Code for this paper">Code</a></li>
        {%- endif %}
      </ul>
    </div>
  </li>
{%- endfor %}
</ol>
