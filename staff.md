---
layout: page
title: Staff
description: A listing of all the course staff members.
nav_order: 3
---

# Staff

## Instructor

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaçhing Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

{% assign graders = site.staffers | where: 'role', 'Grader' %}
{% assign num_graders = graders | size %}
{% if num_graders != 0 %}
## Grader

{% for staffer in graders %}
{{ staffer }}
{% endfor %}
{% endif %}


{% assign randoms = site.staffers | where: 'role', 'Random' %}
{% assign num_randoms = randoms | size %}
{% if num_randoms != 0 %}
## ![image](https://github.com/user-attachments/assets/bc0f9a26-53f0-4e02-972c-5b05e1a21c10)![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgKaVfFhWsnpPuvqAKBpM25Ir98dVvyVQPk0bL_10_pBee1AqKLbZPTK6S02_rXLGMvZ3rCPYUJBme2koRCsuXfpJvLoOTPlS6ork4X9aul_ZKDF3B6D54hdXpywKIAuIUC_AUJTAru-kI/s0/costa-rica-flag-icon-animation.gif)


{% for staffer in randoms %}
{{ staffer }}
{% endfor %}
{% endif %}
