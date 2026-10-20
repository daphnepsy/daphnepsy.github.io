---
title: My Projects
layout: landing
---

{% assign projects = site.projects | concat: site.data.project_cards | sort: "order" %}
<!-- Main -->
<div id="main">
<section id="one" class="spotlights">
	{% for project in projects %}
	{% include project-card.html project=project %}
	{% endfor %}
</section>
</div>
