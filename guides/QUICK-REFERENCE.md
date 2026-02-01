# Quick Reference Guide

Fast reference for common portfolio updates.

## 📍 Main Data File
All content (except projects): `_data/resume.yml`

---

## ✏️ Common Updates

### Change Your Name/Title
```yaml
# _data/resume.yml (lines 2-3)
name: "Your Name"
title: "Your Job Title"
```

### Update About Section
```yaml
# _data/resume.yml (lines 11-16)
about:
  image: "/assets/images/your-photo.png"
  description: |
    Your bio here. You can write multiple
    lines and use **markdown** formatting.
  resume_url: "https://link-to-resume.pdf"
```

### Add a Skill
```yaml
# _data/resume.yml (lines 18-39)
skills:
  - category: "Category Name"
    items:
      - "New Skill Here"  # Add this line
```

### Add Work Experience
```yaml
# _data/resume.yml (lines 41+)
experience:
  - title: "Job Title"
    company: "Company Name"
    location: "City, State"
    period: "2023 - Present"
    description: |
      Brief role description.
    highlights:
      - "Achievement with metrics (e.g., Increased X by 40%)"
      - "Another achievement"
      - "One more achievement"
```

### Update Contact Info
```yaml
# _data/resume.yml (lines 4-6)
email: "new.email@example.com"
phone: "+1 (555) 999-8888"
location: "New City, State"
```

---

## 🎨 Add New Project

1. **Create file:** `_projects/05-project-name.md`

2. **Add this template:**
```yaml
---
layout: project
title: "Project Name"
category: "Type"
description: "One sentence description."
tags: ["Tag1", "Tag2", "Tag3"]
image: "/assets/images/project5.jpg"
external_link: "https://example.com"
date: 2024-04-15
---

## Overview
Project description here...

## Challenge
Problem you solved...

## Solution
How you solved it...

## Results
- **Metric 1:** 50% increase
- **Metric 2:** Impact statement
```

3. **Add image:** Place `project5.jpg` in `assets/images/`

---

## 🔧 Common Tasks

| Task | Action |
|------|--------|
| **Change profile photo** | Replace `assets/images/candidate.png` |
| **Add project image** | Add file to `assets/images/` |
| **Remove a project** | Delete file from `_projects/` |
| **Change social links** | Edit `resume.yml` lines 131-138 |
| **Update education** | Edit `resume.yml` lines 76-88 |
| **Test changes** | Run `bundle exec jekyll serve` |

---

## ⚠️ Important Rules

1. **Spacing matters** - Use spaces, NOT tabs in YAML files
2. **Backup first** - Copy `resume.yml` before major changes
3. **Test locally** - Always preview with `jekyll serve` before deploying
4. **Image paths** - Start with `/assets/images/`
5. **Date format** - Use `YYYY-MM-DD` (e.g., `2024-04-15`)

---

## 🚀 Deploy Changes

```bash
# 1. Test locally
bundle exec jekyll serve

# 2. View at http://localhost:4000

# 3. If good, commit and push
git add .
git commit -m "Update portfolio content"
git push
```

---

## 🆘 Troubleshooting

| Problem | Solution |
|---------|----------|
| **Site won't build** | Check YAML syntax with [yamllint.com](http://yamllint.com) |
| **Images not showing** | Verify file exists in `assets/images/` |
| **Changes not visible** | Hard refresh: Ctrl+F5 (Windows) or Cmd+Shift+R (Mac) |
| **Project not appearing** | Check filename starts with number (e.g., `01-name.md`) |
| **Broken layout** | Check for unclosed quotes or missing colons in YAML |

---

## 📂 File Structure

```
Resume1/
├── _data/
│   └── resume.yml          ← Edit this for most updates
├── _projects/              ← Project detail pages
│   ├── 01-project.md
│   ├── 02-project.md
│   └── ...
├── assets/
│   └── images/            ← Add photos here
│       ├── candidate.png  ← Your photo
│       ├── project1.jpg
│       └── ...
├── UPDATING-GUIDE.md      ← Detailed guide
└── QUICK-REFERENCE.md     ← This file
```

---

## 📝 YAML Syntax Cheat Sheet

```yaml
# Text field
name: "Your Name"

# Multi-line text (use |)
description: |
  First line
  Second line

# List
items:
  - "Item 1"
  - "Item 2"

# Nested structure
about:
  image: "/path/to/image.jpg"
  description: "Text here"

# Comments start with #
# This is a comment
```

---

For detailed instructions, see **UPDATING-GUIDE.md**
