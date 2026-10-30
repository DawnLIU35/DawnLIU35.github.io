---
permalink: /
title: "Chenxi Liu"
excerpt: "Chenxi Liu"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}
<!-- News and publications are rendered from _data/news.yml and _data/publications.yml. -->

<div class="home-intro">
<p>I am a Ph.D. student in Computer Science at the <a href="https://www.cs.umd.edu/">University of Maryland, College Park</a>, advised by Prof. <a href="https://www.cs.umd.edu/people/heng">Heng Huang</a>. I am currently a Research Intern at <b>Meta FAIR</b>, building agentic systems for real-time streaming video generation. Previously, I interned at <b>ByteDance</b>, working on reinforcement learning for LLM reasoning and multi-agent security.</p>
<p>My research interests include:</p>
<ul class="interest-chips">
<li>LLM/VLM Reasoning</li>
<li>Reinforcement Learning</li>
<li>Agentic Systems</li>
<li>World Models</li>
<li>Recursive Self-Improvement</li>
</ul>
</div>

<div class="home-section" id="news">
<h2>🔥 News</h2>
<ul class="news-list">
{%- for item in site.data.news limit: 6 %}
<li><span class="news-date">{{ item.date }}</span><span class="news-emoji">{{ item.emoji }}</span><span>{{ item.text }}</span></li>
{%- endfor %}
</ul>
{%- if site.data.news.size > 6 %}
<details class="news-more">
<summary>Earlier news</summary>
<ul class="news-list">
{%- for item in site.data.news offset: 6 %}
<li><span class="news-date">{{ item.date }}</span><span class="news-emoji">{{ item.emoji }}</span><span>{{ item.text }}</span></li>
{%- endfor %}
</ul>
</details>
{%- endif %}
</div>

<div class="home-section" id="publications">
<h2>📝 Selected Publications</h2>
<div class="pub-list">
{%- for pub in site.data.publications %}
{%- capture badges %}<span class="pub-badges"><span class="pub-badge pub-badge--{{ pub.venue }}">{{ pub.badge }}</span>{% if pub.highlight %}<span class="pub-badge pub-badge--highlight">{{ pub.highlight }}</span>{% endif %}</span>{% endcapture %}
{%- assign thumb = base_path | append: "/images/publications/" | append: pub.slug | append: ".webp" %}
<div class="pub-card">
{%- if pub.thumb == false %}
<div class="pub-thumb pub-thumb--empty">{{ badges }}</div>
{%- else %}
<a class="pub-thumb image-popup" href="{{ thumb }}" title="{{ pub.title | escape }}"><img src="{{ thumb }}" alt="Figure from {{ pub.title | escape }}" loading="lazy">{{ badges }}</a>
{%- endif %}
<div class="pub-body">
<p class="pub-title"><a href="{{ pub.url }}">{{ pub.title }}</a></p>
<p class="pub-authors">{{ pub.authors | replace: "Chenxi Liu", '<span class="me">Chenxi Liu</span>' }}</p>
<p class="pub-venue">{{ pub.venue_full }}{% if pub.highlight %} <span class="pub-highlight">{{ pub.highlight }}</span>{% endif %}</p>
<p class="pub-tldr">{{ pub.tldr }}</p>
<div class="pub-links">
{%- for link in pub.links %}
{%- case link.name %}
{%- when "Paper" %}{% assign icon = '<i class="fas fa-file-alt" aria-hidden="true"></i>' %}
{%- when "Code" %}{% assign icon = '<i class="fab fa-github" aria-hidden="true"></i>' %}
{%- when "Project" %}{% assign icon = '<i class="fas fa-globe" aria-hidden="true"></i>' %}
{%- when "Models" %}{% assign icon = '<span aria-hidden="true">🤗</span>' %}
{%- else %}{% assign icon = '<i class="fas fa-link" aria-hidden="true"></i>' %}
{%- endcase %}
<a href="{{ link.url }}">{{ icon }}{{ link.name }}</a>
{%- endfor %}
</div>
</div>
</div>
{%- endfor %}
</div>
<p class="pub-note">* Equal contribution. Full publication list on <a href="https://scholar.google.com/citations?user=GPzr7O4AAAAJ&amp;hl=en">Google Scholar</a>.</p>
</div>

<div class="home-section" id="experience">
<h2>💼 Experience</h2>
<ul class="timeline">
<li class="timeline-item">
<div class="timeline-logo"><img src="{{ base_path }}/images/logos/meta.svg" alt="Meta"></div>
<div class="timeline-body">
<div class="timeline-head"><span class="timeline-org">Meta FAIR</span><span class="timeline-date">May 2026 – Present</span></div>
<div class="timeline-role">Research Intern</div>
<p class="timeline-desc">Developing an agentic system for streaming video generation, and distilling its capabilities into the video model with on-policy self-distillation, so the model alone can generate streaming video in real time.</p>
</div>
</li>
<li class="timeline-item">
<div class="timeline-logo"><img src="{{ base_path }}/images/logos/bytedance.svg" alt="ByteDance"></div>
<div class="timeline-body">
<div class="timeline-head"><span class="timeline-org">ByteDance</span><span class="timeline-date">Jun 2025 – Sep 2025</span></div>
<div class="timeline-role">Research Intern</div>
<p class="timeline-desc">Reinforcement learning for LLM reasoning (<a href="https://arxiv.org/abs/2511.04800">ERPO</a>) and multi-agent security (<a href="https://arxiv.org/abs/2610.28966">ReMAS</a>).</p>
</div>
</li>
</ul>
</div>

<div class="home-section" id="education">
<h2>🎓 Education</h2>
<ul class="timeline">
<li class="timeline-item">
<div class="timeline-logo timeline-logo--text timeline-logo--umd">UMD</div>
<div class="timeline-body">
<div class="timeline-head"><span class="timeline-org">University of Maryland, College Park</span><span class="timeline-date">Aug 2023 – Present</span></div>
<div class="timeline-role">Ph.D. in Computer Science</div>
<p class="timeline-desc">Advisor: Prof. <a href="https://www.cs.umd.edu/people/heng">Heng Huang</a></p>
</div>
</li>
<li class="timeline-item">
<div class="timeline-logo timeline-logo--text timeline-logo--nu">NU</div>
<div class="timeline-body">
<div class="timeline-head"><span class="timeline-org">Northwestern University</span><span class="timeline-date">Aug 2021 – Mar 2023</span></div>
<div class="timeline-role">M.S. in Electrical Engineering</div>
<p class="timeline-desc">Advisors: Prof. <a href="https://www.mccormick.northwestern.edu/research-faculty/directory/profiles/zhu-qi.html">Qi Zhu</a> and Prof. <a href="https://www.mccormick.northwestern.edu/research-faculty/directory/profiles/wang-xiao.html">Xiao Wang</a></p>
</div>
</li>
<li class="timeline-item">
<div class="timeline-logo timeline-logo--text timeline-logo--sysu">SYSU</div>
<div class="timeline-body">
<div class="timeline-head"><span class="timeline-org">Sun Yat-sen University</span><span class="timeline-date">Sep 2016 – Jun 2020</span></div>
<div class="timeline-role">B.S. in Opto-Electronics Information Science and Engineering</div>
<p class="timeline-desc">Advisor: Prof. <a href="https://spe.sysu.edu.cn/node/328">Xiao Zhang</a></p>
</div>
</li>
</ul>
</div>
