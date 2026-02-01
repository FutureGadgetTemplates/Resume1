---
layout: project
title: "Portfolio Website"
category: "Web Development"
description: "Custom portfolio website built with Jekyll featuring smooth animations and responsive design."
tags:
  - "Jekyll"
  - "HTML/CSS"
  - "JavaScript"
image: "/assets/images/project4.jpg"
external_link: "#"
date: 2024-04-12
---

## Overview

A modern, performant portfolio website built from scratch using Jekyll static site generator. The site showcases design and development work with a focus on storytelling, performance, and accessibility.

## Goals

- **Fast loading times** (< 2 seconds on 3G)
- **Excellent accessibility** (WCAG 2.1 AAA where possible)
- **Easy to update** for non-technical users
- **SEO optimized** for better discoverability
- **Delightful animations** that enhance the experience

## Technical Architecture

### Static Site Generator
Chose Jekyll for several reasons:
- No database or backend required
- Fast build times and page loads
- Markdown for easy content updates
- Built-in support for GitHub Pages
- Large plugin ecosystem

### Performance Optimizations
- **Lazy loading** for images and heavy content
- **Critical CSS** inlined in `<head>`
- **Deferred JavaScript** loading
- **WebP images** with fallbacks
- **Minified and concatenated** assets
- **CDN delivery** via Cloudflare
- **Service worker** for offline functionality

## Design Features

### Homepage
- Full-screen hero with animated gradient background
- Smooth scroll navigation
- Featured projects grid with hover effects
- Skills showcase with progress indicators
- Testimonials carousel
- Contact form with validation

### Project Pages
- Detailed case studies with rich media
- Image galleries with lightbox
- Embedded videos and prototypes
- Related projects suggestions
- Social sharing buttons

### Responsive Design
- Mobile-first approach
- Breakpoints: 640px, 768px, 1024px, 1280px
- Touch-friendly navigation on mobile
- Optimized images for different screen sizes
- Conditional loading based on viewport

## Key Features

### Dark Mode
- System preference detection
- Manual toggle with preference persistence
- Smooth transition between modes
- Optimized images for both modes
- Reduced motion for accessibility

### Animations
- Intersection Observer for scroll animations
- Smooth page transitions
- Micro-interactions on hover and click
- Loading animations
- Respect for `prefers-reduced-motion`

### Accessibility
- Semantic HTML5 markup
- ARIA labels where necessary
- Keyboard navigation support
- Focus visible indicators
- Alt text for all images
- Proper heading hierarchy
- Color contrast ratios exceeding WCAG AAA

### SEO
- Semantic markup and schema.org data
- Open Graph tags for social sharing
- Twitter Card support
- XML sitemap auto-generation
- Robots.txt configuration
- 301 redirects for changed URLs

## Content Management

### Data Files
Used Jekyll data files for easy updates:
- `resume.yml` - Work experience, education, skills
- `projects.yml` - Project metadata
- `testimonials.yml` - Client testimonials
- `social.yml` - Social media links

### Collections
- `_projects/` - Detailed project case studies
- `_posts/` - Blog articles (optional)

### Front Matter
Extensive front matter for project pages:
```yaml
layout: project
title: Project Name
category: Design Type
description: Short description
tags: [tag1, tag2]
featured: true
gallery: [img1.jpg, img2.jpg]
```

## Performance Metrics

### Lighthouse Scores (Mobile)
- **Performance**: 98/100
- **Accessibility**: 100/100
- **Best Practices**: 100/100
- **SEO**: 100/100

### Load Times
- **First Contentful Paint**: 0.8s
- **Largest Contentful Paint**: 1.2s
- **Time to Interactive**: 1.5s
- **Total Blocking Time**: 0ms
- **Cumulative Layout Shift**: 0.001

## Tech Stack

### Core
- Jekyll 4.3+
- Liquid templating
- Sass/SCSS
- Vanilla JavaScript (no jQuery)

### Build Tools
- npm for package management
- Gulp for task automation
- PostCSS for CSS processing
- Autoprefixer for browser compatibility
- PurgeCSS to remove unused styles

### Hosting & Deployment
- GitHub repository for version control
- GitHub Actions for CI/CD
- Cloudflare Pages for hosting
- Cloudflare CDN for global delivery
- Custom domain with SSL

## Challenges & Solutions

### Challenge: Large Image Files
**Solution**: Automated image optimization pipeline with sharp.js, generating multiple sizes and formats (WebP, AVIF, JPEG) with appropriate srcset attributes.

### Challenge: Smooth Page Transitions
**Solution**: Implemented custom JavaScript router with fetch API and History API for SPA-like navigation without framework overhead.

### Challenge: Contact Form on Static Site
**Solution**: Integrated Formspree for form handling with client-side validation and honeypot spam protection.

## Results

- **10,000+ visits** in first 3 months
- **Average session duration**: 3:42 minutes
- **Bounce rate**: 32%
- **15+ project inquiries** from the site
- **Featured** on CSS Design Awards

## Code & Resources

The site is built with modern web standards and best practices. Key learnings and code snippets are documented in the project repository.
