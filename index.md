---
title: Home
layout: home
nav_order: 1
---
# Introduction to AI and Programming
{: .no_toc }
ROB 102, Fall 2024 at the University of Michigan
{: .fs-6 .fw-300 }

This is the course page for the Fall 2024 offering of [Hello, Robot! Introduction to AI and Programming](https://hellorob.org){:target="_blank"} at the University of Michigan. This site contains information relevant to Michigan students.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# Meeting Times

<i class="fa-solid fa-chalkboard-user"></i> **Lectures:** 

*coming soon*

<i class="fa-solid fa-flask"></i> **Labs:**

*coming soon*

# Instructors

<div class="staff-row">
{% assign instructors = site.staff | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}
</div>

# Graduate Instructor

<div class="staff-row">
{% assign gsis = site.staff | where: 'role', 'Graduate Student Instructor' %}
{% for staffer in gsis %}
{{ staffer }}
{% endfor %}
</div>

{% assign teaching_assistants = site.staff | where: 'role', 'Instructional Aide' %}
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

Office hours will be held in **FRB 2000** and on **Zoom**.

The schedule can be found below.

*coming soon*
