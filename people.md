---
title: People
permalink: /people/
---

{% assign people_sorted = (site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|gradstudent|visiting|staff|others|alumni" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif item == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif item == 'gradstudent' %}
<h3>Graduate Students</h3>
 {% elsif item == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif item == 'others' %}
 <h3>Staff</h3>
 {% elsif item == 'staff' %}
<h3>Honorary Members</h3>
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
| Xuelong Zhao | Postdoc (2016) | Postdoc at [Brian Litt  lab](http://littlab.seas.upenn.edu/), U Penn
| Bahram Yoosefizonooz | Visiting (2017) | Postdoc at U Montreal
| Elahe Arani | Visiting (2017) | Postdoc at U Montreal
| Luca Lonini | Postdoc (2017) | Postdoc with Arun at Northwestern U
| Ravi Garg | Undergrad Research | Researcher at Northwestern U
| Sohrob Saeb | Postdoc (2017) | Neuroscience in Bay Area
| [Eva Dyer](http://evadyer.github.io/) | Postdoc (2017) | Assistant Professor, Dept of Biomedical Engineering at Georgia Tech and Emory U
| [Pavan Ramkumar](http://kordinglab.com/people/pavan_ramkumar/index.html) | Postdoc (2017) | A secret startup in bay area
| [Pat Lawlor](http://kordinglab.com/people/pat_lawlor/index.html) | Graduate student (2016) | Northwestern Medical school
| [Hugo Fernandes](http://kordinglab.com/people/hugo_fernandes/index.html) | Postdoc (2016) | [rockets of awesome](https://www.rocketsofawesome.com/)
| [Torben Noto](http://kordinglab.com/people/torben_noto/index.html) | Rotation Student (2016) | Northwestern
| [Vivek Sagar](http://kordinglab.com/people/vivek_sagar/index.html) | Rotation Student (2016) | Northwestern
| [David Brandfonbrener](http://kordinglab.com/people/david_brandfonbrener/index.html) | Visiting Scholar (2016)  | PhD Student, Yale university
| [Daniel E. Acuna](http://kordinglab.com/people/daniel_e_acuna/index.html) | Postdoc (2016) | [iSchool at Syracuse](https://ischool.syr.edu/people/directories/view/deacuna/)
| [Mohammad Azar](http://mgazar.net/academic/) | Postdoc (2016) | Google Deepmind, secret location in London |
| [Cong Yin (Lily)](http://kordinglab.com/people/cong_yin/index.html) | Visiting scholar (2015-2016) | Peking University |
| [Youguo Chen](https://scholar.google.com/citations?user=wZQdEFAAAAAJ&hl=zh-CN) | Visiting scholar (2014 - 2015) | Associate Professor, Southwest University, Chongqing, China
| [Max Berniker](http://sensorimotorcontrolatorium.uic.edu/)   | Postdoc (2014) | Asst Prof, Univ of Illinois at Chicago, Mechanical &amp; Industrial Eng |
| [Mathieu d'Acremont](https://scholar.google.com/citations?user=D7ys4VQAAAAJ&hl=en) | Postdoc (2014) | - |
| [Iris Vilares](https://scholar.google.com/citations?user=Ztwn608AAAAJ&hl=en)   | Graduate Student (2009-2013) | Postdoc, University of Virginia and University College London (w. Peter Dayan) |
| Ben Walker     | Research Engineer (2010-2013) | MS in ME at Northwestern University, Masanet lab |
| Bill Lotter    | Research Scientist (2012-2013)| PhD at MIT |
| Mark Albert	   | (Dec 2009 - Dec 2012) | Asst Prof, Loyola University, Computer Science |
| Yoshiyuki (Yoshi) Sato | Visiting Professor (2012 - 2013) | Asst Prof, Univ of Electro-Communications, Tokyo |
