---
title: DAT101 - Introduction to Data Science
permalink: index.html
layout: home
---

# DAT101 - Introduction to Data Science

Welcome to DAT101 - Introduction to Data Science

Use the links below to navigate the course.

{% assign pages = site.pages | where_exp:"page", "page.url contains '/course'" %}
| Topic |
| --- |
{% for activity in pages  %}| [{{ activity.topic.title }}]({{ site.github.url }}{{ activity.url }}) |{% endfor %}
