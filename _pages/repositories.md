---
layout: page
permalink: /repositories/
title: github repositories
description: Recent GitHub repositories including thesis code.
nav: true
nav_order: 4
---


{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
