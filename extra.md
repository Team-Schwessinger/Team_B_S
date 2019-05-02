---
title: Extra
permalink: /extra/
---

{% assign reference_types = "news|fun|achievements" | split: "|" %}

{% for type in reference_types %}

{% if type == 'news' %}
### **In the News** 
 {% elsif type == 'fun' %}
### **Lab Extra-curricular activities** 
 {% elsif type == 'achievements' %}
### **Great Achievements for Team Schwessinger** 
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

