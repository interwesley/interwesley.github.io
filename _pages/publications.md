---
layout: archive
title: "Research"
permalink: /research/
redirect_from: /publications/
author_profile: true

# Sections appear in this order.
sections:
  - type: working
    title: "Working Papers"
  - type: journal
    title: "Journal Papers"
  - type: conference
    title: "Conference Papers"

# Papers appear in the order listed. To add one, copy a block and edit it.
# type: working, journal or conference. Working papers use "status" instead of "details".
papers:
  - type: working
    title: "Finite-Sample Distribution Theory and Efficient Large-Scale Inference for Online Quantile Regression"
    authors: "Ziyang Wei, Jiaqi Li, Lan Wang, Wei Biao Wu"
    venue: "Journal of the American Statistical Association (T&M)"
    status: "under review"
    arxiv: "https://arxiv.org/abs/2610.05869"
  - type: working
    title: "Exact Tail Laws for Nonlinear SGD with Infinite-Variance Gradients"
    authors: "Xiaoli Li, Qianqian Lei, Ziyang Wei, Wei Biao Wu"
    venue: "International Conference on Learning Representations (ICLR 2027)"
    status: "under review"
  - type: working
    title: "High Confidence Level Inference is Almost Free using Parallel Stochastic Optimization"
    authors: "Wanrong Zhu, Zhipeng Lou, Ziyang Wei, Wei Biao Wu"
    venue: "The Journal of Machine Learning Research (JMLR)"
    status: "revision submitted"
    arxiv: "https://arxiv.org/abs/2401.09346"
  - type: journal
    title: "Central Limit Theorems for Stochastic Gradient Descent Quantile Estimators"
    authors: "Ziyang Wei, Jiaqi Li, Likai Chen, Wei Biao Wu"
    venue: "IEEE Transactions on Information Theory"
    details: "vol. 72, no. 8, pp. 6054–6070, 2026"
    paperurl: "https://ieeexplore.ieee.org/document/11563558"
    arxiv: "https://arxiv.org/abs/2503.02178"
  - type: journal
    title: "CALLR: A Semi-Supervised Cell-Type Annotation Method for Single-Cell RNA Sequencing Data"
    authors: "Ziyang Wei, Shuqin Zhang"
    venue: "Bioinformatics"
    details: "vol. 37, Supplement 1, pp. i51–i58, 2021"
    paperurl: "https://academic.oup.com/bioinformatics/article/37/Supplement_1/i51/6319673"
  - type: conference
    title: "Refining Covariance Matrix Estimation in Stochastic Gradient Descent Through Bias Reduction"
    authors: "Ziyang Wei, Wanrong Zhu, Jingyang Lyu, Wei Biao Wu"
    venue: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
    details: "PMLR vol. 300, pp. 3565–3573, 2026"
    paperurl: "https://virtual.aistats.org/virtual/2026/poster/13784"
    arxiv: "https://arxiv.org/abs/2604.21203"
  - type: conference
    title: "General Weighted Averaging in Stochastic Gradient Descent: CLT and Adaptive Optimality"
    authors: "Ziyang Wei, Wanrong Zhu, Wei Biao Wu"
    venue: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
    details: "PMLR vol. 300, pp. 1198–1206, 2026"
    paperurl: "https://virtual.aistats.org/virtual/2026/poster/13842"
    arxiv: "https://arxiv.org/abs/2307.06915"
  - type: conference
    title: "Gaussian Approximation and Concentration of Constant Learning-Rate Stochastic Gradient Descent"
    authors: "Ziyang Wei, Jiaqi Li, Zhipeng Lou, Wei Biao Wu"
    venue: "Advances in Neural Information Processing Systems (NeurIPS)"
    details: "vol. 38, pp. 85003–85033, 2025"
    paperurl: "https://proceedings.neurips.cc/paper_files/paper/2025/hash/7aae9e3ec211249e05bd07271a6b1441-Abstract-Conference.html"
  - type: conference
    title: "Asymptotic Theory of SGD with a General Learning-Rate"
    authors: "Or Goldreich, Ziyang Wei, Soham Bonnerjee, Jiaqi Li, Wei Biao Wu"
    venue: "Advances in Neural Information Processing Systems (NeurIPS)"
    details: "vol. 38, pp. 23242–23269, 2025"
    paperurl: "https://neurips.cc/virtual/2025/loc/san-diego/poster/115186"
---

<style>
  .page__title { display: none; }
  .archive__subtitle { font-size: 1.5em; }
  .archive > .archive__subtitle:first-of-type { margin-top: 0; }
  .archive__item-title { font-size: 1em; }
  .archive__item-title a { text-decoration: none; }
</style>

{% capture me %}<strong>{{ site.author.name }}</strong>{% endcapture %}
{% for section in page.sections %}
<h2 id="{{ section.type }}" class="archive__subtitle">{{ section.title }}</h2>
{% for paper in page.papers %}{% if paper.type == section.type %}{% assign link = paper.paperurl | default: paper.arxiv %}
<div class="list__item">
  <article class="archive__item" itemscope itemtype="http://schema.org/ScholarlyArticle">
    <h2 class="archive__item-title" itemprop="headline">{% if link %}<a href="{{ link }}">{{ paper.title }}</a>{% else %}{{ paper.title }}{% endif %}</h2>
    <p class="archive__item-excerpt">{{ paper.authors | replace: site.author.name, me }}</p>
    <p class="archive__item-excerpt">{% if paper.status %}<i>{{ paper.venue }}</i>, {{ paper.status }}{% else %}Published in <i>{{ paper.venue }}</i>, {{ paper.details }}{% endif %}</p>
    {% if paper.paperurl or paper.arxiv %}<p class="archive__item-excerpt">{% if paper.paperurl %}[<a href="{{ paper.paperurl }}">Paper</a>] {% endif %}{% if paper.arxiv %}[<a href="{{ paper.arxiv }}">arXiv</a>]{% endif %}</p>{% endif %}
  </article>
</div>
{% endif %}{% endfor %}
{% endfor %}

You can also find my articles on <u><a href="https://scholar.google.com/citations?user=IysMzzwAAAAJ&hl=en">my Google Scholar profile</a>.</u>
