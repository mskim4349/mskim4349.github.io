---
layout: page
permalink: /publications/
title: publications
description: Peer-reviewed journal articles, newest first. My name is shown in bold.
nav: true
nav_order: 2
---

{% include bib_search.liquid %}

<h2 class="pub-section">Selected Publications</h2>
<div class="publications publications-selected">

{% bibliography --query @*[selected=true] %}

</div>

<h2 class="pub-section">All Publications</h2>
<div class="publications">

{% bibliography %}

</div>
