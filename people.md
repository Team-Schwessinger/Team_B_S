---
title: People
permalink: /people/
---

{% assign people_sorted = (site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|postgrad|gradstudent|projectstudent|staff|alumni|previous" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif item == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif item == 'postgrad' %}
<h3>PhD Students</h3>
 {% elsif item == 'gradstudent' %}
<h3>Masters and Honours Students</h3>
 {% elsif item == 'projectstudent' %}
<h3>Undergraduate Project Students</h3>
 {% elsif item == 'staff' %}
<h3>Research Fellows</h3>
 {% elsif item == 'previous' %}
<h3>Previously (Co-)/Supervised Students</h3>
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


| Who are they | When were they here | What were they | What did they research | Where they went |
| :------------- |:-------------| :-----------| :-----------| :-----------|
| Amy MacKenzie | 2018 | Co-advised Honour Student | BLANK | BLANK
| Anjuni Peiris | 2018 | Co-advised Honour Student | BLANK | BLANK
| Miriam Schalamun | 2017 | Co-advised Master Student | BLANK | BLANK
| Richard Tien | 2017 | Undergraduate Summer Student | BLANK | BLANK
| Gamran Green | 2017 | Undergraduate Summer Student | BLANK | BLANK
| Yiheng Hu | 2016 | Co-advised Master Student | BLANK | PhD with the Schwessinger lab
| Daniel Stephens | 2016 | Undergraduate Summer Student | BLANK | BLANK
| Ramawatar Nagar | 2015- | Co-advised PhD Student | BLANK | BLANK
| Furong Liu | 2014-2017 | Co-advised PhD Student | BLANK | BLANK
| Yen Nguyen | 2013-2015 | Undergraduate Project Student | BLANK | BLANK
| Marielle Palatino | 2013-2014 | Undergraduate Project Student | BLANK | BLANK
| Michael Owen | 2013 | Undergraduate Project Student | BLANK | BLANK
| Nick Thomas | 2012-2016 | Co-advised PhD Student | BLANK | BLANK
| Daniel Caddell | 2012-2015 | Co-advised PhD Student | BLANK | BLANK
| Thomas Dougan | 2012 | Undergraduate Project Student | BLANK | BLANK
| Isaac Shaker | 2011-2013 | Undergraduate Project Student | BLANK | BLANK
| Sonali Roy | 2010 | Co-advised PhD Rotation | BLANK | BLANK
| Johannes Hofberger | 2009 | Co-advised Master Student | BLANK | BLANK
