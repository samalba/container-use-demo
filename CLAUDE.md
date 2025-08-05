# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a container-use demo repository showcasing a simple static website for "Sam's Blog" - a tech blog focused on AI, software development, and technology insights. The project is specifically designed to demonstrate web development workflows with Claude and container-use environments.

## Architecture

### File Structure
- `index.html` - Main blog homepage with article listings
- `about.html` - About page with personal and professional information  
- `styles.css` - Comprehensive CSS with responsive design, gradients, and modern styling
- `LICENSE` - Project license file
- `README.md` - Project documentation with container-use setup instructions

### Design System
- Uses a modern gradient-based design (purple/blue gradients)
- Responsive grid layout for blog posts
- Sticky header navigation
- Card-based design for articles and content sections
- Mobile-first responsive breakpoints at 768px and 480px

## Development Workflow

### Serving the Website
Since this is a static HTML/CSS website, it can be served using any simple HTTP server:
- Python: `python -m http.server 8000`
- Node.js: `npx http-server`  
- PHP: `php -S localhost:8000`

### Container-Use Integration
This project is specifically designed to work with container-use environments. The README provides the complete setup:

1. Install container-use: `brew install dagger/tap/container-use`
2. Configure Claude MCP: `claude mcp add container-use -- container-use stdio`
3. Use restricted tool set for container-only operations

### Theming and Customization
The CSS is well-structured for theme modifications:
- Main color scheme uses gradients defined in `.hero` and `.tag` classes
- Color variables are defined throughout for consistent theming
- Layout uses CSS Grid and Flexbox for responsive design

## Container-Use Commands

When working with this project in container-use environments:
- Use `container-use log <env_id>` to view environment logs
- Use `container-use checkout <env_id>` to access environment state
- Always work within container environments for consistency

## Common Tasks

### Creating Theme Variations
- Modify gradient values in `.hero` background and `.tag` background
- Update color scheme variables throughout styles.css
- Test responsive behavior across breakpoints

### Adding Blog Content
- Add new `<article class="post">` elements to index.html
- Follow existing structure: title link, post-meta, post-excerpt
- Maintain consistent date formatting and content style