---
title: Home
layout: home
nav_order: 1
---
# Introduction to AI and Programming
{: .no_toc }
ROB 102, Fall 2023 at the University of Michigan
{: .fs-6 .fw-300 }

This is the course page for the Fall 2023 offering of [Hello, Robot! Introduction to AI and Programming](https://hellorob.org){:target="_blank"} at the University of Michigan. This site contains information relevant to Michigan students.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

<!-- # Meeting Times -->

<!-- <i class="fa-solid fa-chalkboard-user"></i> **Lectures:** Tues & Thurs 3-4:30 PM @ FRB 1060 -->

<!-- <i class="fa-solid fa-flask"></i> **Labs:** -->
<!-- * F 10:30 AM-12:30 PM @ FRB 1060 -->
<!-- * F 12:30-2:30 PM @ FRB 1060 -->
<!-- * F 2:30-4:30 PM @ FRB 1060 -->

# Instructors

<div class="staff-row">
{% assign instructors = site.staff | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}
</div>

{% assign gsi = site.staff | where: 'role', 'Graduate Student Instructor' %}
{% assign num_gsi = gsi | size %}
{% if num_gsi != 0 %}

# Graduate Instructor

<div class="staff-row">
{% for staffer in gsi %}
{{ staffer }}
{% endfor %}
</div>
{% endif %}

{% assign gsi = site.staff | where: 'role', 'Instructional Aide' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

# Instructional Aides

<div class="staff-row">
{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
</div>
{% endif %}

# Office Hours

Coming soon!

<!-- <iframe
    src="https://calendar.google.com/calendar/embed?src=c_0ifcv1flo2qjltm07u30o28kd8%40group.calendar.google.com&ctz=America%2FDetroit"
    style="border: 0" width="800" height="600" frameborder="0" scrolling="no">
</iframe> -->
