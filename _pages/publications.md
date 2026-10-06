---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true

# Sections appear in this order.
sections:
  - type: conference
    title: "Conference Papers"
  - type: journal
    title: "Journal Papers"
  - type: working
    title: "Working Papers"

# To add a paper, copy a block below and edit it.
# type: conference, journal or working. Working papers use "status" instead of "details".
papers:
  - type: conference
    title: "Refining Covariance Matrix Estimation in Stochastic Gradient Descent Through Bias Reduction"
    authors: "Ziyang Wei, Wanrong Zhu, Jingyang Lyu, Wei Biao Wu"
    venue: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
    details: "PMLR vol. 300, 2026"
    arxiv: "https://arxiv.org/abs/2604.21203"
  - type: conference
    title: "General Weighted Averaging in Stochastic Gradient Descent: CLT and Adaptive Optimality"
    authors: "Ziyang Wei, Wanrong Zhu, Wei Biao Wu"
    venue: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
    details: "PMLR vol. 300, 2026"
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
    details: "vol. 38, 2025"
    paperurl: "https://openreview.net/pdf/99e24e7827ceb1c84df73b66a26c5e78ff6d3c88.pdf"
  - type: journal
    title: "Central Limit Theorems for Stochastic Gradient Descent Quantile Estimators"
    authors: "Ziyang Wei, Jiaqi Li, Likai Chen, Wei Biao Wu"
    venue: "IEEE Transactions on Information Theory"
    details: "vol. 72, no. 8, pp. 6054–6070, 2026"
    paperurl: "https://ieeexplore.ieee.org/document/11563558"
    arxiv: "https://arxiv.org/abs/2503.02178"
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
---

You can also find my articles on <u><a href="https://scholar.google.com/citations?user=IysMzzwAAAAJ&hl=en">my Google Scholar profile</a>.</u>

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
