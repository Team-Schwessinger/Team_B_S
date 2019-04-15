---
title: People
permalink: /people/
---

{% assign people_sorted = (site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|gradstudent|projectstudent|staff|alumni" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif item == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif item == 'gradstudent' %}
<h3>Graduate Students</h3>
 {% elsif item == 'projectstudent' %}
<h3>Undergraduate Project Students</h3>
 {% elsif item == 'staff' %}
<h3>Staff</h3>
 {% elsif item == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains item %}
    <div class="list-item-people">
      <p class="list-post-title">
        {% if profile.avatar %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
        {% else %}
        <a href="{{ site.baseurl }}{{ profile.url }}"><img width="200" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
        {% endif %}
        <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
      </p>
    </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>
{% endfor %}


| Who are they | When were they here | Where they went |
| :------------- |:-------------| :-----------|
| Aisha Ward | Staff (2019) | Nowhere at [Schwessinger lab](https://biology.anu.edu.au/research/groups/schwessinger-group-plants-fungi-evolution), ANU

