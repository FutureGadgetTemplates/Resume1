# Project Pages Structure

This document explains the organization of individual project pages in the codebase.

## Directory Structure

```
Resume1/
├── _projects/              # Individual project markdown files
│   ├── 01-ecommerce-redesign.md
│   ├── 02-brand-identity-system.md
│   ├── 03-mobile-app-design.md
│   └── 04-portfolio-website.md
├── _layouts/
│   ├── default.html       # Main site layout
│   └── project.html       # Project detail page layout
├── _sass/
│   ├── _project-detail.scss  # Styles for project pages
│   └── ...
└── index.html             # Main page (links to projects)
```

## How It Works

### 1. Jekyll Collections
Projects are managed as a Jekyll collection defined in `_config.yml`:
```yaml
collections:
  projects:
    output: true
```

### 2. Project Files (`_projects/`)
Each project is a separate markdown file with front matter:
```yaml
---
layout: project
title: "Project Name"
category: "Project Type"
description: "Short description"
tags:
  - "Tag 1"
  - "Tag 2"
image: "/assets/images/project.jpg"
external_link: "#"  # Optional
date: 2024-01-15    # For sorting
---

## Project content in Markdown...
```

### 3. Project Layout (`_layouts/project.html`)
The project layout template includes:
- Back to projects link
- Project header with title, category, and tags
- Main content area (rendered from markdown)
- Optional gallery section
- Navigation to previous/next projects
- Link back to all projects

### 4. Styling (`_sass/_project-detail.scss`)
Custom styles for:
- Project hero section
- Content formatting (headings, lists, quotes, code)
- Gallery grid
- Navigation between projects

## Adding a New Project

1. **Create a new markdown file** in `_projects/`:
   - Use naming convention: `##-project-name.md` (where ## is a number)
   - Higher numbers appear first (sorted by date, then filename)

2. **Add front matter** with all required fields:
   ```yaml
   ---
   layout: project
   title: "Your Project Title"
   category: "Project Category"
   description: "Brief description for preview"
   tags: ["Tag1", "Tag2", "Tag3"]
   image: "/assets/images/your-project.jpg"
   external_link: "https://example.com"  # Optional
   date: 2024-04-15
   ---
   ```

3. **Write project content** in Markdown:
   - Use `##` for main sections
   - Use `###` for subsections
   - Include lists, quotes, images, etc.
   - See existing projects for examples

4. **Optional: Add a gallery**:
   ```yaml
   gallery:
     - /assets/images/project-1.jpg
     - /assets/images/project-2.jpg
     - /assets/images/project-3.jpg
   ```

5. **Build the site** - Jekyll will automatically:
   - Generate a page at `/projects/##-project-name/`
   - Add it to the projects grid on the homepage
   - Link it in the project navigation

## Project URLs

Projects are accessible at:
- `/projects/01-ecommerce-redesign/`
- `/projects/02-brand-identity-system/`
- `/projects/03-mobile-app-design/`
- `/projects/04-portfolio-website/`

The homepage projects section automatically links to these pages.

## Editing Projects

To edit a project:
1. Open the corresponding `.md` file in `_projects/`
2. Edit the front matter or markdown content
3. Save the file
4. Rebuild the Jekyll site

## Removing Projects

To remove a project:
1. Delete the `.md` file from `_projects/`
2. The project will automatically disappear from the homepage grid

## Tips

- **Naming**: Use descriptive filenames (they become part of the URL)
- **Ordering**: Projects display in reverse chronological order by `date` field
- **Images**: Store project images in `/assets/images/` directory
- **Consistency**: Follow the same structure across all projects for a cohesive experience
- **Markdown**: Use standard markdown syntax - it's automatically converted to HTML
