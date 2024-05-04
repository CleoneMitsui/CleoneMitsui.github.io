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

I have taken the scenic route back to academia, so my publication list is still in the making. Manuscripts are now making their rounds in the rigorous world of peer review. Your patience and interest are greatly appreciated as I lay the first stones. Stay tuned for updates!

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
