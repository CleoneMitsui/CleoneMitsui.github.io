---
layout: editorial-record
editorial_title: "Papers"
title: "Papers"
permalink: /publications/
author_profile: false
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- ## Published Papers -->

{% assign sorted_publications = site.publications | sort: "year" | reverse %}
<ol>
{% for post in sorted_publications %}
  <li>
    <p>{{ post.citation }} {% if post.doi %}<a href="{{ post.doi }}" target="_blank">{{ post.doi }}</a>{% endif %}</p>
    {{ post.content }}
  </li>
{% endfor %}
</ol>



<h2 class="manuscripts-heading">Manuscripts in Prep or Under Review</h2>

{% assign sorted_manuscripts = site.manuscripts | sort: "title" %}
<ol>
{% for post in sorted_manuscripts %}
  <li><p>{{ post.authors }}. {{ post.title }}. <i>{{ post.status }}</i>.</p></li>
{% endfor %}
</ol>
