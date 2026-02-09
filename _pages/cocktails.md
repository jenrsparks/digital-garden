---
title: Cocktails
id: Cocktails
permalink: /cocktails
category: Cocktails
navigation_include: true
---

[Death & Co: Modern Classic Cocktails](https://app.thestorygraph.com/books/cc495afc-eaa6-46f4-a182-24551b3434e4) was my first cocktail book, and I've poured over it a dozen times to try to internalize the core concepts. Where I struggled, though, was that it felt as though I needed the right brand of a given liquor, and 20-30 different bottles to be able to make many of the drinks. Instead, I wanted to be able to take what was in my cabinet, riff something together, and understand what I was doing.

The book [Cocktail Codex: Fundamentals, Formulas, Evolutions](https://app.thestorygraph.com/books/4d477c60-4b1a-442d-9f9d-70c6f7cd0c47) by the same authors took me across the line and helped me begin my journey towards exactly that. It's arguably my favorite cocktail book, to the extent that I've gifted copies of it to fellow cocktail enthusiasts. 

Leaning on the Death & Co model of categorization, I've created an [[Core Templates|inventory starting with the core templates]]. Branching off from these are variants, all of which are connected in the Relationship Visualization section in the sidebar. As this inventory expands, I may have some without relationships, though they can still be found in the full index of recipes below.

### Recipe Index

<ul>
{% assign notes = site.notes | uniq | where: 'category',"Cocktails" | where: 'exclude_page', nil | sort "title" %}
{% for note in notes %}
    <li><a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a></li>
{% endfor %}
</ul>