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

# Meeting Times

<i class="fa-solid fa-chalkboard-user"></i> **Lectures:** M & W 3-4:30 PM @ FRB 1050

<i class="fa-solid fa-flask"></i> **Labs:**
* F 12:30-2:30 PM @ FRB 1050
* F 2:30-4:30 PM @ FRB 1050

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

Office hours will be held in **FRB 2000** and on [**Zoom**](https://umich.zoom.us/j/93612493008) (Passcode: ROB 102).

The schedule can be found below. You must be logged in to your UM account in order to see the event details.
You can also access the calendar or add it to your calendar using [this link](https://calendar.google.com/calendar/u/0?cid=Y19mODgzMzJhMDg1NWZjZGE4ODY1OGYxMjZjMTZjMDc0NmUyZmUxZmQ3M2RjNzFjODUwOWVhZjYxMzQ2NzU3M2JjQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20).

<iframe src="https://calendar.google.com/calendar/embed?src=c_f88332a0855fcda88658f126c16c0746e2fe1fd73dc71c8509eaf613467573bc%40group.calendar.google.com&ctz=America%2FNew_York" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
