---
layout: default
title: Home
---

# Welcome to My Notes

This is my personal knowledge base where I collect notes on various topics.

## Recent Notes

{% assign sorted_notes = site.pages | where_exp: "item", "item.path contains 'notes/'" | sort: 'date' | reverse %}
{% if sorted_notes.size > 0 %}
<ul class="note-list">
{% for note in sorted_notes limit:10 %}
  {% if note.title %}
  <li>
    <a href="{{ note.url | relative_url }}">{{ note.title }}</a>
    <div class="note-meta">
      {% if note.category %}<span class="category">{{ note.category }}</span>{% endif %}
      {% if note.date %}{{ note.date | date: "%B %d, %Y" }}{% endif %}
      {% if note.tags %} | {{ note.tags | join: ", " }}{% endif %}
    </div>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% else %}
<p>No notes yet. Start taking notes with the Claude skill!</p>
{% endif %}

## Browse by Category

- [Topic Notes]({{ '/notes/topic/' | relative_url }}) - Organized by subject
- [Daily Notes]({{ '/notes/daily/' | relative_url }}) - Daily journal entries

---

*Use the `/notes` skill in Claude Code to quickly create new notes!*
