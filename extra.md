---
title: Extra
permalink: /extra/
---




{% assign reference_types = "news|achievements|collaborators|fun" | split: "|" %}

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

### **Collaborators of Team Schwessinger**
Here are some cool people in fields that interest us. note: This list is in no way complete. We have a lot of collaborators – if you’ve collaborated with us and want a link here, let us know!

**Australian National University**

[John Rathjen - Plant Immunity](https://biology.anu.edu.au/research/labs/rathjen-group-plant-immunity)  
[Professor Eric Stone - Quantitative and Computational Biology](https://biology.anu.edu.au/research/labs/stone-group-quantitative-and-computational-biology)

**NSW Department of Primary Industries**

[Dr. Andrew Milgate - Research Plant Pathologist](https://www.dpi.nsw.gov.au/about-us/research-development/staff/staff-profiles/andrew-milgate)

**University of Sydney**

[Professor Wieland Meyer - Molecular Mycology Research](http://www.mycologylab.org/DefaultInfo.aspx?Page=Home)

**Denmark Department of Agroecology**

[Professor Mogens Støvring Hovmøller - Entomology and Plant Pathology](http://pure.au.dk/portal/en/mogens.hovmoller@agrsci.dk)
