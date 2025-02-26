---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- ## Published Papers -->

{% assign sorted_publications = site.publications | sort: "year" | reverse %}
{% for post in sorted_publications %}
  <p>{{ post.citation }} {% if post.doi %}<a href="{{ post.doi }}" target="_blank">{{ post.doi }}</a>{% endif %}</p>
{% endfor %}


## Manuscripts in Prep and Under Review

{% assign sorted_manuscripts = site.manuscripts | sort: "title" %}
{% for post in sorted_manuscripts %}
  <p>{{ post.authors }}. {{ post.title }}. {{ post.status }}.</p>
{% endfor %}
