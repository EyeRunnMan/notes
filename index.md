---
layout: default
title: Home
---

# Welcome to My Notes

This is my personal knowledge base where I collect notes on various topics.

## Recent Notes

{% assign sorted_notes = site.pages | where_exp: "item", "item.path contains 'notes/'" | sort: 'date' | reverse %}
{% if sorted_notes.size > 0 %}
{% for note in sorted_notes limit:10 %}
  {% if note.title %}
### [{{ note.title }}]({{ note.url | relative_url }})
*{% if note.date %}{{ note.date | date: "%B %d, %Y" }}{% endif %}{% if note.tags %} | Tags: {{ note.tags | join: ", " }}{% endif %}*

  {% endif %}
{% endfor %}
{% else %}
No notes yet. Start taking notes with the Claude skill!
{% endif %}

---

## Browse by Category

- **Topic Notes** (`/notes/topic/`) - Organized by subject
- **Daily Notes** (`/notes/daily/`) - Daily journal entries

---

*Use the Claude Code skill to quickly create new notes!*
