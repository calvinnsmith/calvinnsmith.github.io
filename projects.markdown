---
layout : page
title : Github
permalink: /projects/
---

{% for repo in site.github.public_repositories %}

{% if repo.fork == false and repo.topics.size > 0 %}

## [{{ repo.name }}]({{ repo.html_url }})

{{ repo.description }}

Topics: {{ repo.topics | array_to_sentence_string }}



{% endif %}

{% endfor %}