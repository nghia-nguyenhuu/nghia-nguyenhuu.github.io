---
layout: page
permalink: /publications/
title: publications
description: Publications listed below (*indicates corresponding author).
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h1>preprints</h1>

{% bibliography -f preprints %}

<h1>conference &amp; journal articles</h1>

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<h1>technical reports &amp; short papers</h1>

{% bibliography -f reports %}

</div>
