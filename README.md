# Notes

My personal notes repository, hosted on GitHub Pages.

## Overview

This is a Jekyll-powered notes site with a hybrid organization system that supports both topic-based and daily journal-style notes.

## Features

- **Hybrid Organization**: Notes organized by topic categories and daily entries
- **Custom Jekyll Theme**: Clean, responsive design optimized for reading
- **Auto-Indexing**: Homepage automatically lists recent notes
- **Rich Metadata**: Full support for tags, categories, and timestamps
- **Claude Code Skill**: Custom skill for effortless note creation

## Structure

```
notes/
├── notes/
│   ├── topic/          # Topic-based notes (programming, learning, etc.)
│   └── daily/          # Daily journal entries
├── _layouts/           # Jekyll layouts (default, note)
├── _includes/          # Reusable components (navigation)
├── assets/css/         # Custom styles
├── _data/              # Data files (categories)
└── .claude/skills/     # Claude Code skill for note-taking
```

## Getting Started

### Prerequisites

- Ruby 2.7+
- Jekyll 4.0+
- Bundler

### Local Development

1. Install dependencies:
   ```bash
   gem install jekyll bundler
   bundle install
   ```

2. Run locally:
   ```bash
   bundle exec jekyll serve
   ```

3. Visit `http://localhost:4000`

### GitHub Pages Deployment

1. Push to GitHub
2. Go to repository Settings > Pages
3. Set source to `main` branch
4. Your site will be available at `https://username.github.io/notes`

## Taking Notes with Claude Code

This repository includes a custom Claude Code skill for easy note-taking:

1. Open Claude Code in this directory
2. Invoke the skill: `/notes` or use the Skill tool
3. Follow the prompts to create your note
4. The skill handles all formatting, categorization, and organization

### Note Types

**Topic Notes**: Organized by category
- Location: `notes/topic/{category}/`
- Use for: Technical notes, learning resources, references

**Daily Notes**: Journal-style dated entries
- Location: `notes/daily/{YYYY-MM-DD}.md`
- Use for: Daily logs, quick thoughts, time-based entries

## Categories

Configured in `_data/categories.yml`:
- Programming
- Personal
- Work
- Learning
- Ideas
- Reference

## Customization

- **Styles**: Edit `assets/css/style.css`
- **Layouts**: Modify `_layouts/` files
- **Navigation**: Update `_includes/navigation.html`
- **Config**: Adjust `_config.yml`
- **Categories**: Add/edit in `_data/categories.yml`

## License

Personal use. Feel free to fork and adapt for your own notes.
