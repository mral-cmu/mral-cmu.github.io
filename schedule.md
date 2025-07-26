---
layout: default
title: Schedule
---

# Class Schedule

<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Lecture</th>
      <th>Assignment Released</th>
      <th>Assignment Due</th>
    </tr>
  </thead>
  <tbody>
    {% for e in site.data.schedule %}
    <tr>
      <td>{{ e.date }}</td>
      <td>{{ e.lecture }} {% if e.slideurl %} <a href="{{ e.slideurl }}">slides</a>{% endif %}{% if e.videourl %} <a href="{{ e.videourl }}">video</a>{% endif %} {% if e.notesurl %} <a href="{{ e.notesurl}}">notes</a>{% endif %}</td>
      <td>{{ e.assignment_released }} {% if e.assignmenturl %} <a href="{{ e.assignmenturl }}">here</a> {% endif %}</td>
      <td>{{ e.assignment_due}}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
