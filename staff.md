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
## Teaching Assistants

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
## ~Honorary TA 🇨🇷

{% for staffer in randoms %}
{{ staffer }}
{% endfor %}
{% endif %}