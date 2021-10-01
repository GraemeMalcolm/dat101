---
title: Data Science Foundations
permalink: index.html
layout: home
---

# DAT101 - Data Science Foundations

Welcome to DAT101 - Data Science Foundations

Use the links below to navigate the course.

{% assign pages = site.pages | where_exp:"page", "page.url contains '/course'" %}
| Module | Topic |
| --- | --- |
{% for activity in pages  %}| [{{ activity.topic.module }}]| [{{ activity.topic.title }}]({{ site.github.url }}{{ activity.url }}) |{% endfor %}
