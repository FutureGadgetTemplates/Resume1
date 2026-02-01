# Resume1

A modern Jekyll resume website with a bold, creative design.

## Prerequisites

- Ruby 2.7+ installed
- Bundler gem (`gem install bundler`)

## Getting Started

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```

3. Open your browser to `http://localhost:4000`

## Customization

### Content Updates

For updating your portfolio content, see these guides:

- **[📖 UPDATING-GUIDE.md](guides/UPDATING-GUIDE.md)** - Comprehensive guide for updating all sections (About, Skills, Experience, Projects, etc.)
- **[⚡ QUICK-REFERENCE.md](guides/QUICK-REFERENCE.md)** - Quick cheat sheet for common updates
- **[🎨 PROJECTS.md](guides/PROJECTS.md)** - Guide for managing project pages

### Quick Start

1. **Update basic info**: Edit `_data/resume.yml`
2. **Add/edit projects**: Create/modify files in `_projects/` directory
3. **Change colors**: Modify `_sass/_variables.scss`
4. **Replace photos**: Update files in `assets/images/`

## Building for Production

```bash
bundle exec jekyll build
```

The static site will be generated in the `_site/` folder.
