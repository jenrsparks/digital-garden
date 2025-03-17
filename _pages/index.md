---
layout: home
title: Home
id: home
permalink: /
---

# Welcome! 🌱

Somehow, you have stumbled upon a weird, mess of random content by yours truly. As content progresses, there will be more variety, but for the time being, check out the couple collections on the navigation along the top.

<strong>Recently updated notes</strong>
<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>
