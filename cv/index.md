---
layout: plain
title: Curriculum Vitae
---

# {{ site.data.main.contact.name }}
{{ site.data.main.contact.title }}  
{{ site.data.main.contact.department }}  
{{ site.data.main.contact.institution }}  

## Contact ##
{{ site.data.main.contact.postal-address }}  
{{ site.data.main.contact.email }}  
[{{ site.data.main.contact.website }}]({{ site.data.main.contact.website }})

## Education ##
{% for edu in site.data.main.education %}
* _[{{ edu.dates}}]_ -- __{{ edu.degree }}__, {{ edu.institution }}, {{ edu.location }}    
  _thesis:_ {{ edu.thesis }}, _advisor:_ {{ edu.advisor }}
{% endfor %}

## Appointments ##
{% for apt in site.data.main.appointments %}
* _[{{ apt.dates}}]_ -- __{{ apt.title }}__, {{ apt.institution }}, {{ apt.location }}    
{% endfor %}

## Awards ##
{% for award in site.data.awards %}
* _[{{ award.date }}]_ -- {{ award.name }}
{% endfor %}

## Publications ##

### In Preparation / Submitted ###
{% bibliography  --query @unpublished %}

### Published / In Press ###
{% bibliography  --query @article %}

## Sponsored Projects ##

For collaborative projects, award amounts represent the Columbia portion only.

{% for project in site.data.projects %}
 * *{{project.code}}* -- {{project.amount}} ({{project.dates}}), {{project.role}} <br />
 {{project.title}}
{% endfor %}


## Teaching ##

{% for course in site.data.courses %}
 * [{{course.title}}]({{ course.url }}) -- {{course.description}} ({{course.offered}})
{% endfor %}


## Software ##

{% for code in site.data.codes %}
 * [{{code.name}}]({{ code.url }}) -- {{code.description}}
{% endfor %}

## Presentations ##

### Invited ###
{% for pres in site.data.presentations.invited %}
* _[{{ pres.date }}]_ -- {{ pres.title }}{% if pres.title %},{% endif %} {{ pres.location }}
{% endfor %}

### Conference ###
{% for pres in site.data.presentations.conference %}
* _[{{ pres.date }}]_ -- {{ pres.title }}{% if pres.title %},{% endif %} {{ pres.location }}
{% endfor %}

## Service ##

### Community ###
{% for item in site.data.service.community %}
* {{ item }}
{% endfor %}

### Univeristy ###
{% for item in site.data.service.university %}
* {{ item }}
{% endfor %}