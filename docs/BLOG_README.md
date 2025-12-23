# Jekyll Blog for CNC Pigment

This directory contains a Jekyll-based blog for the CNC Pigment project.

## Setup

1. Install Ruby and Bundler (if not already installed)
2. Install dependencies:
   ```bash
   cd docs
   bundle install
   ```

## Development

To run the blog locally:

```bash
cd docs
bundle exec jekyll serve
```

Then visit `http://localhost:4000/blog.html` in your browser.

## Adding New Posts

Create a new file in `_posts` with the format `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title:  "Your Post Title"
date:   YYYY-MM-DD HH:MM:SS +0000
categories: jekyll update
---

Your post content here...
```

## File Structure

- `_config.yml` - Jekyll configuration
- `_posts/` - Blog posts
- `_layouts/` - Page layouts (default, post)
- `_includes/` - Reusable components
- `assets/` - CSS, images, and other static files
- `blog.md` - Blog index page
- `Gemfile` - Ruby dependencies

## GitHub Pages

This blog is configured to work with GitHub Pages. Make sure GitHub Pages is enabled for this repository and set to use the `/docs` folder as the source.
