---
permalink: /
layout: home
title: "Cosmology, simulations & machine learning"
excerpt: "Physicist building robust, interpretable machine-learning methods to learn about the Universe from galaxies and simulations."
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

<section class="home-hero" aria-labelledby="hero-title">
  <div class="home-hero__copy">
    <p class="eyebrow">Cosmologist · Machine-learning researcher · Science communicator</p>
    <h1 id="hero-title">Finding the physics hidden in <em>cosmic data.</em></h1>
    <p class="home-hero__lead">I’m <strong>Natalí de Santi</strong>, a physicist building robust, interpretable, and uncertainty-aware machine-learning methods to learn about the Universe from galaxies and simulations.</p>
    <p class="home-hero__affiliation">Postdoctoral Scholar at <a href="https://bccp.berkeley.edu">UC Berkeley’s BCCP</a> · Affiliate at <a href="https://www.lbl.gov">Lawrence Berkeley National Laboratory</a></p>
    <div class="home-actions">
      <a class="home-button home-button--primary" href="{{ '/publications/' | relative_url }}">Explore my research <span aria-hidden="true">→</span></a>
      <a class="home-button home-button--secondary" href="{{ '/cv/' | relative_url }}">View my CV</a>
    </div>
    <div class="home-social" aria-label="Research profiles">
      <a href="{{ site.author.googlescholar }}">Google Scholar</a>
      <a href="{{ site.author.github | prepend: 'https://github.com/' }}">GitHub</a>
      <a href="{{ site.author.orcid }}">ORCID</a>
      <a href="mailto:{{ site.author.email }}">Email</a>
    </div>
  </div>
  <div class="home-hero__portrait">
    <div class="home-hero__orbit" aria-hidden="true"></div>
    <img src="{{ '/images/profile.png' | relative_url }}" alt="Natalí de Santi" width="680" height="820">
    <div class="home-hero__caption"><span>Based in</span> Berkeley, California</div>
  </div>
</section>

<section class="home-proof" aria-label="Research at a glance">
  <div><strong>{{ site.publications | size }}</strong><span>publications & proceedings</span></div>
  <div><strong>{{ site.talks | size }}</strong><span>invited talks & presentations</span></div>
  <div><strong>3</strong><span>connected research directions</span></div>
  <p>From simulated universes to interpretable equations, I work across the full inference pipeline.</p>
</section>

<section class="home-section" aria-labelledby="research-title">
  <div class="section-heading">
    <p class="eyebrow">What I investigate</p>
    <h2 id="research-title">Research built for the messy, beautiful Universe.</h2>
    <p>My work connects cosmological theory, large simulations, and modern statistical learning—with reliability and physical insight as first-class goals.</p>
  </div>
  <div class="research-grid">
    <article class="research-card research-card--violet">
      <span class="research-card__number">01</span>
      <h3>Field-level cosmological inference</h3>
      <p>Extracting cosmological information directly from galaxy phase space with graph neural networks and simulation-based inference.</p>
      <a href="https://arxiv.org/abs/2302.14101">Read the foundational paper <span aria-hidden="true">↗</span></a>
    </article>
    <article class="research-card research-card--blue">
      <span class="research-card__number">02</span>
      <h3>The halo–galaxy connection</h3>
      <p>Modeling how galaxies inhabit dark-matter halos while preserving stochasticity, correlations, and calibrated uncertainty.</p>
      <a href="https://arxiv.org/abs/2410.17844">Explore probabilistic approaches <span aria-hidden="true">↗</span></a>
    </article>
    <article class="research-card research-card--gold">
      <span class="research-card__number">03</span>
      <h3>Efficient, interpretable ML</h3>
      <p>Denoising covariance matrices and translating neural-network predictions into analytic equations scientists can understand.</p>
      <a href="https://arxiv.org/abs/2205.10881">See the covariance work <span aria-hidden="true">↗</span></a>
    </article>
  </div>
</section>

<section class="home-section home-section--selected" aria-labelledby="selected-title">
  <div class="section-heading section-heading--row">
    <div>
      <p class="eyebrow">Selected work</p>
      <h2 id="selected-title">Recent research</h2>
    </div>
    <a class="text-link" href="{{ '/publications/' | relative_url }}">All publications <span aria-hidden="true">→</span></a>
  </div>
  {% assign featured_publications = site.publications | sort: 'date' | reverse %}
  <div class="work-list">
    {% for publication in featured_publications limit:3 %}
    <article class="work-item">
      <div class="work-item__meta"><span>{{ publication.date | date: '%Y' }}</span><span>{{ publication.venue }}</span></div>
      <div>
        <h3><a href="{{ publication.url | relative_url }}">{{ publication.title }}</a></h3>
        <p>{{ publication.excerpt }}</p>
      </div>
      <a class="work-item__arrow" href="{{ publication.url | relative_url }}" aria-label="Read {{ publication.title | escape }}">↗</a>
    </article>
    {% endfor %}
  </div>
</section>

<section class="home-section home-story" aria-labelledby="story-title">
  <div class="home-story__image">
    <img src="{{ '/images/4years.png' | relative_url }}" alt="A childhood Microsoft Paint drawing by Natalí" loading="lazy">
  </div>
  <div class="home-story__copy">
    <p class="eyebrow">The human behind the models</p>
    <h2 id="story-title">Curiosity has always been the throughline.</h2>
    <p>At four years old, I was drawing ducks in Microsoft Paint. Later came Astronomy Olympiads, experimental superconductivity, particle physics, black holes, and finally cosmology. The tools changed; the instinct to understand how things work did not.</p>
    <p>Today, that curiosity takes me from billions of simulated particles to the properties of a single galaxy—and to the question of what each can tell us about the cosmos.</p>
    <a class="text-link" href="{{ '/cv/' | relative_url }}">Follow the full journey <span aria-hidden="true">→</span></a>
  </div>
</section>

<section class="home-section" aria-labelledby="writing-title">
  <div class="section-heading section-heading--row">
    <div>
      <p class="eyebrow">Ideas in progress</p>
      <h2 id="writing-title">From the notebook</h2>
    </div>
    <a class="text-link" href="{{ '/year-archive/' | relative_url }}">All writing <span aria-hidden="true">→</span></a>
  </div>
  <div class="writing-grid">
    {% for post in site.posts limit:3 %}
    <article class="writing-card">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: '%B %Y' }}</time>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <a href="{{ post.url | relative_url }}" aria-label="Read {{ post.title | escape }}">Read essay <span aria-hidden="true">→</span></a>
    </article>
    {% endfor %}
  </div>
</section>

<section class="home-contact" aria-labelledby="contact-title">
  <p class="eyebrow">Let’s connect</p>
  <h2 id="contact-title">Interested in cosmology, robust ML, or a conversation across fields?</h2>
  <a class="home-button home-button--light" href="mailto:{{ site.author.email }}">Start a conversation <span aria-hidden="true">→</span></a>
</section>
