# CLAUDE.md - Mintlify Documentation Guide

## Build Commands
- `npm i -g mintlify` - Install Mintlify CLI
- `mintlify dev` - Run local development server
- `mintlify install` - Reinstall dependencies (troubleshooting)

## Documentation Structure
- `mint.json` - Main configuration file
- `*.mdx` - Content files
- `images/` - Documentation images
- `logo/` - Brand logos

## Style Guidelines
- Use MDX format for all documentation pages
- Include frontmatter with title and description
- Use Mintlify components like `<AccordionGroup>` and `<Accordion>`
- Maintain consistent heading hierarchy (## for main sections, ### for subsections)
- URLs should use the format `https://app.aitriumos.com`
- Image paths should be relative (e.g., `/images/example.png`)
- Use descriptive alt text for all images

## Theme Info
- Primary color: #0052CC (blue)
- Light color: #2684FF
- Dark color: #0052CC