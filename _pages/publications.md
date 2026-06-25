---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 2
---

<h2 class="pub-section">Journal Articles (SCIE)</h2>
<div class="publications">

{% bibliography --query @*[korean=false] %}

</div>

<h2 class="pub-section">Korean Journal Articles</h2>
<div class="publications">

{% bibliography --query @*[korean=true] %}

</div>

<h2 class="pub-section">Under Review &amp; In Preparation</h2>
<div class="publications publications-unnumbered">

{% bibliography --query @*[preprint=true] %}

</div>
