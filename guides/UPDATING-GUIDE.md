# Portfolio Updating Guide

This guide explains how to update different sections of your portfolio website. All content is managed through data files and markdown, making it easy to update without touching any code.

## Table of Contents

1. [About Section](#about-section)
2. [Skills Section](#skills-section)
3. [Experience Section](#experience-section)
4. [Education Section](#education-section)
5. [Projects Section](#projects-section)
6. [Contact Information](#contact-information)
7. [Social Links](#social-links)

---

## About Section

### Location
`_data/resume.yml` - Lines 1-16

### How to Update

Edit the following fields in `resume.yml`:

```yaml
# Personal Information
name: "Your Full Name"
title: "Your Professional Title"
email: "your.email@example.com"
phone: "+1 (555) 123-4567"
location: "Your City, State"

# About Section
about:
  image: "/assets/images/candidate.png"
  description: |
    Your bio/description goes here. You can write multiple paragraphs
    by continuing on new lines. This supports Markdown formatting, so you
    can use **bold**, *italic*, and other formatting.
  resume_url: "https://link-to-your-resume.pdf"  # Optional
```

### Tips

- **Image**: Place your photo in `assets/images/` and reference it in the `image` field
- **Description**: Keep it concise (2-4 sentences recommended)
- **Markdown**: You can use:
  - `**text**` for bold
  - `*text*` for italic
  - Line breaks by adding blank lines
- **Resume URL**: Add a link to your PDF resume if you want the Resume button to download it

### Example

```yaml
name: "Jane Smith"
title: "UX Designer & Frontend Developer"
about:
  description: |
    I'm a creative professional passionate about building beautiful,
    user-centered digital experiences. With 5+ years of experience in
    design and development, I help companies bridge the gap between
    aesthetics and functionality.
  resume_url: "https://drive.google.com/your-resume.pdf"
```

---

## Skills Section

### Location
`_data/resume.yml` - Lines 18-39

### How to Update

The skills section uses categories with items under each:

```yaml
skills:
  - category: "Category Name 1"
    items:
      - "Skill 1"
      - "Skill 2"
      - "Skill 3"

  - category: "Category Name 2"
    items:
      - "Skill A"
      - "Skill B"
```

### Tips

- **Categories**: Typically 3-4 categories work best
- **Items per category**: 4-6 skills per category is ideal
- **Order**: List skills from most important/proficient to least
- **Naming**: Be specific (e.g., "React.js" not just "JavaScript frameworks")

### Example

```yaml
skills:
  - category: "Frontend Development"
    items:
      - "React.js & Next.js"
      - "TypeScript"
      - "Tailwind CSS"
      - "HTML5 & CSS3"
      - "Responsive Design"

  - category: "Design Tools"
    items:
      - "Figma"
      - "Adobe XD"
      - "Sketch"
      - "Adobe Photoshop"

  - category: "Other"
    items:
      - "Git & GitHub"
      - "RESTful APIs"
      - "Agile/Scrum"
      - "Accessibility (WCAG)"
```

### Adding/Removing Categories

**To add a new category:**
```yaml
  - category: "New Category Name"
    items:
      - "Item 1"
      - "Item 2"
```

**To remove a category:** Simply delete the entire category block

---

## Experience Section

### Location
`_data/resume.yml` - Lines 41-74

### How to Update

Each job entry follows this format:

```yaml
experience:
  - title: "Job Title"
    company: "Company Name"
    location: "City, State"
    period: "Start Date - End Date"
    description: |
      Brief description of your role and responsibilities.
    highlights:
      - "Key achievement or responsibility 1"
      - "Key achievement or responsibility 2"
      - "Key achievement or responsibility 3"
```

### Tips

- **Order**: List jobs from most recent to oldest
- **Period format**: Use "2021 - Present" for current jobs
- **Description**: 1-2 sentences max, focus on big picture
- **Highlights**:
  - Use action verbs (Led, Designed, Implemented, Increased)
  - Include metrics when possible (40% increase, $1M revenue)
  - Keep to 3-5 highlights per job
  - Be specific and quantifiable

### Example

```yaml
experience:
  - title: "Senior Product Designer"
    company: "Tech Innovations Inc."
    location: "San Francisco, CA"
    period: "2022 - Present"
    description: |
      Leading design initiatives for enterprise SaaS products serving 50,000+ users.
    highlights:
      - "Redesigned core product interface, improving user satisfaction by 45%"
      - "Established design system used across 8 product teams"
      - "Mentored team of 3 junior designers"
      - "Led user research program with 100+ participants quarterly"

  - title: "Product Designer"
    company: "StartupCo"
    location: "Remote"
    period: "2020 - 2022"
    description: |
      Designed user experiences for mobile and web applications.
    highlights:
      - "Shipped 5 major product features from concept to launch"
      - "Reduced user onboarding time by 60% through UX improvements"
      - "Conducted 30+ user interviews and usability tests"
```

### Adding/Removing Jobs

**To add a new job:** Copy the template above and add it to the list

**To remove a job:** Delete the entire job entry block

---

## Education Section

### Location
`_data/resume.yml` - Lines 76-88

### How to Update

```yaml
education:
  - degree: "Degree Name"
    school: "School Name"
    location: "City, State"
    year: "Graduation Year"
    honors: "Honors/Awards"  # Optional

  - degree: "Another Degree"
    school: "Another School"
    location: "City, State"
    year: "Year"
```

### Tips

- **Order**: List most recent/relevant education first
- **Honors**: Include magna cum laude, summa cum laude, GPA (if 3.5+), awards
- **Certificates**: Include relevant certificates, bootcamps, etc.
- **Omit honors**: If you don't have honors, just leave that line out

### Example

```yaml
education:
  - degree: "Master of Science in Human-Computer Interaction"
    school: "Carnegie Mellon University"
    location: "Pittsburgh, PA"
    year: "2020"
    honors: "GPA: 3.9/4.0"

  - degree: "Bachelor of Arts in Graphic Design"
    school: "Rhode Island School of Design"
    location: "Providence, RI"
    year: "2018"
    honors: "Summa Cum Laude"

  - degree: "UX Design Bootcamp"
    school: "General Assembly"
    location: "Online"
    year: "2017"
```

---

## Projects Section

Projects are more complex as each has its own dedicated page.

### Quick Updates (Summary Info Only)

For quick updates to how projects appear on the homepage, you can edit the summary in each project's markdown file.

### Location
`_projects/` directory - Individual `.md` files

### Updating an Existing Project

1. **Open the project file** (e.g., `_projects/01-ecommerce-redesign.md`)

2. **Edit the front matter** (between the `---` lines):

```yaml
---
layout: project
title: "Your Project Title"
category: "Project Category"
description: "Brief description shown on homepage (1-2 sentences)"
tags:
  - "Tag 1"
  - "Tag 2"
  - "Tag 3"
image: "/assets/images/your-project-image.jpg"
external_link: "https://live-project-url.com"  # Optional
date: 2024-04-15  # For sorting (YYYY-MM-DD)
---
```

3. **Edit the content** (below the `---` markers):
   - Write in Markdown format
   - Use `##` for main headings
   - Use `###` for subheadings
   - Include images, lists, quotes, etc.

### Adding a New Project

1. **Create a new file** in `_projects/`:
   - Name it: `##-project-name.md` (e.g., `05-my-new-project.md`)
   - Lower numbers = newer projects (shown first)

2. **Copy this template:**

```yaml
---
layout: project
title: "Project Title"
category: "Design/Development/Branding"
description: "One-sentence description of the project for the homepage."
tags:
  - "Primary Skill"
  - "Secondary Skill"
  - "Tool Used"
image: "/assets/images/project-name.jpg"
external_link: "https://example.com"  # Optional - remove if none
date: 2024-04-15
---

## Overview

Brief overview of the project - what it is, who it's for, and what you did.

## Challenge

What problem were you solving? What were the constraints or difficulties?

## Solution

How did you approach the problem? What was your process?

### Research & Discovery (optional subsection)
Details about your research process.

### Design/Development Process (optional subsection)
Details about your approach.

## Key Features

- Feature 1 with description
- Feature 2 with description
- Feature 3 with description

## Results

What was the outcome? Include metrics if possible:
- **X% increase** in some metric
- **Y users** impacted
- **Award/recognition** received

## Technologies Used

List the tools, languages, frameworks, etc. you used:
- Figma for design
- React for development
- Node.js for backend
```

3. **Add your project image:**
   - Place image in `assets/images/`
   - Name it something memorable (e.g., `my-new-project.jpg`)
   - Update the `image` field in front matter

4. **Write your content** using Markdown

### Removing a Project

Simply delete the `.md` file from `_projects/` directory.

### Tips for Project Pages

- **Images**: Use high-quality screenshots, 1200px+ wide
- **Length**: Aim for 500-1000 words per project
- **Structure**: Use consistent sections (Overview, Challenge, Solution, Results)
- **Metrics**: Include numbers whenever possible (% increases, user counts, etc.)
- **Tags**: Use 3-5 relevant tags per project
- **External link**: Link to live project, GitHub, or case study if available

---

## Contact Information

### Location
`_data/resume.yml` - Lines 1-6

### How to Update

```yaml
email: "your.email@example.com"
phone: "+1 (555) 123-4567"
location: "City, State/Country"
```

This information appears in:
- The Contact section at the bottom
- Site metadata

### Tips

- Use a professional email address
- Include country code for phone numbers
- Location can be specific (city) or general (state/country)

---

## Social Links

### Location
`_data/resume.yml` - Lines 131-138

### How to Update

```yaml
social:
  - platform: "LinkedIn"
    url: "https://linkedin.com/in/your-profile"
    icon: "linkedin"
  - platform: "GitHub"
    url: "https://github.com/your-username"
    icon: "github"
```

### Adding New Social Links

Currently supported icons: `linkedin`, `github`

To add more social links (Twitter, Dribbble, etc.), you'll need to:
1. Add the entry to the `social` array
2. Create an SVG icon file in `_includes/icons/`

### Example with Twitter

1. Add to `resume.yml`:
```yaml
  - platform: "Twitter"
    url: "https://twitter.com/your-handle"
    icon: "twitter"
```

2. Create `_includes/icons/twitter.html` with Twitter SVG icon

### Removing Social Links

Delete the social media entry you don't want from the `social` array.

---

## Testing Your Changes

After making updates:

1. **Save all files**

2. **Rebuild the site:**
   ```bash
   bundle exec jekyll serve
   ```

3. **View in browser:**
   - Open `http://localhost:4000`
   - Check that your changes appear correctly
   - Test on mobile view (resize browser)

4. **Common issues:**
   - **YAML syntax errors**: Make sure indentation is correct (use spaces, not tabs)
   - **Images not showing**: Check file path and that image exists
   - **Changes not appearing**: Hard refresh browser (Ctrl+F5 or Cmd+Shift+R)

---

## Quick Reference: File Locations

| What to Update | File Location |
|---------------|---------------|
| Name, Title, Email, Phone | `_data/resume.yml` (lines 1-6) |
| About Section | `_data/resume.yml` (lines 10-16) |
| Skills | `_data/resume.yml` (lines 18-39) |
| Experience | `_data/resume.yml` (lines 41-74) |
| Education | `_data/resume.yml` (lines 76-88) |
| Project Summaries | Individual files in `_projects/` |
| Social Links | `_data/resume.yml` (lines 131-138) |
| Site Title | `_config.yml` (line 2) |
| Favicon | Replace files in `assets/favicon/` |
| Profile Photo | `assets/images/candidate.png` |
| Project Images | `assets/images/` |

---

## Getting Help

If you run into issues:

1. **Check YAML syntax**: Use a YAML validator like [yamllint.com](http://www.yamllint.com/)
2. **Check Jekyll errors**: Look at the terminal output when running `jekyll serve`
3. **Review examples**: Look at the existing content in `resume.yml` and `_projects/`
4. **Start small**: Make one change at a time and test

---

## Best Practices

1. **Backup first**: Always keep a backup of `resume.yml` before major changes
2. **Use version control**: Commit changes to git regularly
3. **Test locally**: Always preview changes locally before deploying
4. **Keep it current**: Update your portfolio every 3-6 months
5. **Quality over quantity**: Better to have 4 great projects than 10 mediocre ones
6. **Proofread**: Check for typos and grammatical errors
7. **Get feedback**: Ask others to review your content
8. **Mobile test**: Always check how it looks on mobile devices
