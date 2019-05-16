---
title: Extra
permalink: /extra/
---




{% assign reference_types = "news|achievements|fun" | split: "|" %}

{% for type in reference_types %}

{% if type == 'news' %}
### **In the News**
 {% elsif type == 'achievements' %}
### **Great achievements for Team Schwessinger**
 {% elsif type == 'fun' %}
### **Lab extracurricular activities**
{% endif %}

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains type %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>
{% endfor %}
