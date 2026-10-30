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
<h2>News</h2>
<ul class="news-list">
{%- for item in site.data.news limit: 6 %}
<li><span class="news-date">{{ item.date }}</span><span>{{ item.text }}</span></li>
{%- endfor %}
</ul>
{%- if site.data.news.size > 6 %}
<details class="news-more">
<summary>Earlier news</summary>
<ul class="news-list">
{%- for item in site.data.news offset: 6 %}
<li><span class="news-date">{{ item.date }}</span><span>{{ item.text }}</span></li>
{%- endfor %}
</ul>
</details>
{%- endif %}
</div>

<div class="home-section" id="publications">
<h2>Selected Publications</h2>
<div class="pub-list">
{%- for pub in site.data.publications %}
{%- assign thumb = base_path | append: "/images/publications/" | append: pub.slug | append: ".webp" %}
<div class="pub">
{%- unless pub.thumb == false %}
<a class="pub-thumb image-popup" href="{{ thumb }}" title="{{ pub.title | escape }}"><img src="{{ thumb }}" alt="" loading="lazy"></a>
{%- endunless %}
<div class="pub-body">
<div class="pub-title"><a href="{{ pub.url }}">{{ pub.title }}</a></div>
<div class="pub-authors">{{ pub.authors | replace: "Chenxi Liu", '<span class="me">Chenxi Liu</span>' }}</div>
<div class="pub-meta"><span class="venue venue--{{ pub.venue }}">{{ pub.badge }}</span>{% if pub.highlight %}<span class="venue venue--highlight">{{ pub.highlight }}</span>{% endif %}{% for link in pub.links %}<a class="pub-link" href="{{ link.url }}">{{ link.name }}</a>{% endfor %}</div>
</div>
</div>
{%- endfor %}
</div>
<p class="pub-note">* Equal contribution. Full list on <a href="https://scholar.google.com/citations?user=GPzr7O4AAAAJ&amp;hl=en">Google Scholar</a>.</p>
</div>

<div class="home-section" id="experience">
<h2>Experience</h2>
<ul class="entry-list">
<li class="entry">
<div class="entry-logo"><img src="{{ base_path }}/images/logos/meta.svg" alt="Meta"></div>
<div class="entry-body">
<div class="entry-title">Meta FAIR</div>
<div class="entry-sub">Research Intern · May 2026 – Present</div>
<div class="entry-desc">Agentic systems for streaming video generation, distilled into the video model with on-policy self-distillation for real-time generation.</div>
</div>
</li>
<li class="entry">
<div class="entry-logo"><img src="{{ base_path }}/images/logos/bytedance.svg" alt="ByteDance"></div>
<div class="entry-body">
<div class="entry-title">ByteDance</div>
<div class="entry-sub">Research Intern · Jun 2025 – Sep 2025</div>
<div class="entry-desc">Reinforcement learning for LLM reasoning (<a href="https://arxiv.org/abs/2511.04800">ERPO</a>) and multi-agent security (<a href="https://arxiv.org/abs/2610.28966">ReMAS</a>).</div>
</div>
</li>
</ul>
</div>

<div class="home-section" id="education">
<h2>Education</h2>
<ul class="entry-list">
<li class="entry">
<div class="entry-body">
<div class="entry-title">Ph.D. in Computer Science, University of Maryland, College Park</div>
<div class="entry-sub">Aug 2023 – Present · Advisor: Prof. <a href="https://www.cs.umd.edu/people/heng">Heng Huang</a></div>
</div>
</li>
<li class="entry">
<div class="entry-body">
<div class="entry-title">M.S. in Electrical Engineering, Northwestern University</div>
<div class="entry-sub">Aug 2021 – Mar 2023 · Advisors: Prof. <a href="https://www.mccormick.northwestern.edu/research-faculty/directory/profiles/zhu-qi.html">Qi Zhu</a> and Prof. <a href="https://www.mccormick.northwestern.edu/research-faculty/directory/profiles/wang-xiao.html">Xiao Wang</a></div>
</div>
</li>
<li class="entry">
<div class="entry-body">
<div class="entry-title">B.S. in Opto-Electronics Information Science and Engineering, Sun Yat-sen University</div>
<div class="entry-sub">Sep 2016 – Jun 2020 · Advisor: Prof. <a href="https://spe.sysu.edu.cn/node/328">Xiao Zhang</a></div>
</div>
</li>
</ul>
</div>
