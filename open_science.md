---
title: Open Science
permalink: /open_science/
---


### **Open Science and Contributions of Team Schwessinger to the Scientific Community**
<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains 'openscience' %}
    <div class="list-item">
    <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a> (<small>{{post.date | date: "%m/%d/%y" }}</small>)
        </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

