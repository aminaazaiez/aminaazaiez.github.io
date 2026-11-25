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

{% for post in site.publications reversed %}
  {% if post.future_work %}
    {% include publication-item.html %}
  {% endif %}
{% endfor %}

{% for post in site.publications reversed %}
  {% unless post.future_work %}
    {% include publication-item.html %}
  {% endunless %}
{% endfor %}
