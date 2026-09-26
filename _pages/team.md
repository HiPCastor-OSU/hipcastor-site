---
title: "HiPCastor - Team"
layout: gridlay
excerpt: "HiPCastor: Team members"
sitemap: true
permalink: /team/
---

<div class="hpc-card text-center">
  <p>We are looking for new PhD students, undergrads, and MS students to join the team!</p>
  <p class="mb-0"><a href="{{ '/openings' | relative_url }}" class="hpc-arrow-link">See openings</a></p>
</div>

## Group Members

{% assign alumni_all = "" | split: "," %}
{% if site.data.alumni_members %}{% assign alumni_all = alumni_all | concat: site.data.alumni_members %}{% endif %}
{% if site.data.alumni_msc %}{% assign alumni_all = alumni_all | concat: site.data.alumni_msc %}{% endif %}
{% if site.data.alumni_bsc %}{% assign alumni_all = alumni_all | concat: site.data.alumni_bsc %}{% endif %}
{% if site.data.alumni_visitors %}{% assign alumni_all = alumni_all | concat: site.data.alumni_visitors %}{% endif %}

<div class="hpc-pill-nav" markdown="0">
  {% if site.data.faculty.size > 0 %}<a href="#faculty" class="hpc-pill">Faculty</a>{% endif %}
  {% if site.data.phd_students.size > 0 %}<a href="#phd-students" class="hpc-pill">PhD Students</a>{% endif %}
  {% if site.data.students.size > 0 %}<a href="#masters-and-undergraduate-students" class="hpc-pill">Masters &amp; Undergrads</a>{% endif %}
  {% if site.data.opensource.size > 0 %}<a href="#open-source-contributors" class="hpc-pill">Open Source</a>{% endif %}
  {% if site.data.incoming.size > 0 %}<a href="#incoming-members" class="hpc-pill">Incoming</a>{% endif %}
  {% if alumni_all.size > 0 %}<a href="#alumni" class="hpc-pill">Alumni</a>{% endif %}
</div>

{% if site.data.faculty.size > 0 %}
## Faculty
{% assign number_printed = 0 %}
{% for member in site.data.faculty %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% if site.data.phd_students.size > 0 %}
## PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.phd_students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% if site.data.students.size > 0 %}
## Masters and Undergraduate Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% if site.data.opensource.size > 0 %}
## Open Source Contributors
{% assign number_printed = 0 %}
{% for member in site.data.opensource %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% if site.data.incoming.size > 0 %}
## Incoming Members
{% assign number_printed = 0 %}
{% for member in site.data.incoming %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}

{% if alumni_all.size > 0 %}
## Alumni
{% assign number_printed = 0 %}
{% for member in alumni_all %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}{% if forloop.last %}<div class="row justify-content-center">{% else %}<div class="row">{% endif %}
{% endif %}

<div class="col-sm-6 clearfix">
  {% include member-card.html member=member %}
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
{% endif %}
