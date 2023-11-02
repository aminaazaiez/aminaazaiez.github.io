---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<h2>Work in Progress</h2>
{% for post in site.publications %}
  {% if post.future_work %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Publications</h2>
{% for post in site.publications %}
  {% unless post.future_work %}
    {% include archive-single.html %}
  {% endunless %}
{% endfor %}
