---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: false
hide_title: true
---

<div class="modern-page-header">
  <p class="eyebrow">Peer-reviewed work</p>
  <h1>Publications</h1>
  <p>Papers on field-level cosmological inference, the halo–galaxy connection, and interpretable machine learning.{% if site.author.googlescholar %} You can also find my articles on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.{% endif %}</p>
</div>

{% include base_path %}

<div class="modern-page">
  <div class="modern-list">
    {% for post in site.publications reversed %}
      {% include archive-single-modern.html %}
    {% endfor %}
  </div>
</div>
