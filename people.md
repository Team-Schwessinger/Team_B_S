---
title: People
permalink: /people/
---

{% assign people_sorted = (site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|postgrad|gradstudent|projectstudent|staff|alumni|previous" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
 {% elsif item == 'pi' %}
 {% elsif item == 'postgrad' %}
 {% elsif item == 'gradstudent' %}
 {% elsif item == 'projectstudent' %}
 {% elsif item == 'staff' %}
 {% elsif item == 'previous' %}
<h3>Previously (Co-)/Supervised Students</h3>
 {% elsif item == 'alumni' %}
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


| Who are they | When were they here | What were they | 
| :------------- |:-------------| :-----------| 
| Somasundhari Shanmuganadam  | 2018 | Masters Student |
| Amy MacKenzie | 2018 | Co-advised Honour Student | 
| Anjuni Peiris | 2018 | Co-advised Honour Student | 
| Miriam Schalamun | 2017 | Co-advised Master Student | 
| Richard Tien | 2017 | Undergraduate Summer Student | 
| Gamran Green | 2017 | Undergraduate Summer Student | 
| Yiheng Hu | 2016 | Co-advised Master Student | 
| Daniel Stephens | 2016 | Undergraduate Summer Student | 
| Ramawatar Nagar | 2015- | Co-advised PhD Student | 
| Furong Liu | 2014-2017 | Co-advised PhD Student | 
| Yen Nguyen | 2013-2015 | Undergraduate Project Student | 
| Marielle Palatino | 2013-2014 | Undergraduate Project Student | 
| Michael Owen | 2013 | Undergraduate Project Student | 
| Nick Thomas | 2012-2016 | Co-advised PhD Student | 
| Daniel Caddell | 2012-2015 | Co-advised PhD Student | 
| Thomas Dougan | 2012 | Undergraduate Project Student | 
| Isaac Shaker | 2011-2013 | Undergraduate Project Student | 
| Sonali Roy | 2010 | Co-advised PhD Rotation | 
| Johannes Hofberger | 2009 | Co-advised Master Student | 
