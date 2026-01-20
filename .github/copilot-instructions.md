# GitHub Copilot Instructions for cheap-menus.poc

## Project Overview

This is **The Gelato & Icecream Factory** - a proof-of-concept static website showcasing a retro-styled ice cream parlor menu built with GitHub Pages and Jekyll.

### Purpose
A demonstration of themed menu presentation using markdown with embedded HTML/CSS to create a nostalgic, vintage ice cream parlor experience.

## Technology Stack

- **Hosting**: GitHub Pages
- **Static Site Generator**: Jekyll
- **Content Format**: Markdown with embedded HTML/CSS
- **Design Style**: Retro 1960s-1980s ice cream parlor aesthetic
- **Typography**: Monospace fonts (Courier New)
- **Layout**: CSS Grid for responsive design

## Repository Structure

```
/
├── index.md          # Welcome page and main navigation hub
├── 1.md - 4.md       # Menu pages (Classic Flavors, Premium, Specialty, Ultimate)
├── 5.md - 8.md       # Menu image pages
├── _config.yml       # Jekyll configuration
├── logo.png          # Ice cream parlor logo
└── .github/          # GitHub configuration files
```

## Coding Standards and Design Principles

### Visual Design Aesthetic
- **Color Palette**: Pink (#FFE8E8, #FFD5D5, #C85A7A), beige (#FFF5E6), brown (#4A1F1F), tan (#D4A574)
- **Background**: Candy-striped pattern using repeating linear gradients
- **Borders**: Bold 4-6px solid borders
- **Shadows**: Offset box shadows for depth (e.g., `5px 5px 0px #D4A574`)
- **Hover Effects**: Subtle scale and rotate transforms
- **Border Radius**: Rounded corners (12-20px) for a friendly feel

### CSS Style Conventions
- Inline `<style>` blocks within each markdown file for page-specific styling
- Use CSS Grid for responsive layouts (`grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))`)
- Maintain consistent spacing units (multiples of 5px: 20px, 25px, 30px, etc.)
- Font sizes use `em` units relative to base 20px
- Monospace font family: `'Courier New', monospace`

### Content Formatting
- YAML frontmatter for Jekyll page metadata:
  ```yaml
  ---
  layout: default
  title: "The Gelato & Icecream Factory - [Page Name]"
  ---
  ```
- Emoji usage for visual interest (🍦 🍓 🍫 etc.)
- Consistent naming: "flavour" instead of "flavor" in CSS classes
- Price format: `$X.XX` (always 2 decimal places)

### Navigation Standards
- Links use `.html` extension (Jekyll auto-converts from `.md`)
- Navigation bar present on all pages except index
- Consistent nav link styling: pink background (#C85A7A), bold, rounded corners

## Code Change Guidelines

### What to Preserve
- **Retro aesthetic**: Maintain the vintage color scheme, striped backgrounds, and playful typography
- **Consistent design language**: Keep border styles, shadows, and hover effects uniform across pages
- **Navigation structure**: Preserve existing page linking and numbering (1-8)
- **Responsive layouts**: Grid-based designs that adapt to different screen sizes
- **Emoji visual language**: Use emojis consistently for flavor icons

### When Making Changes
- **Maintain visual consistency**: New elements should match existing color palette and style
- **Test responsive behavior**: Ensure grid layouts work on various screen sizes
- **Keep file structure simple**: This is a static site - avoid adding unnecessary complexity
- **Preserve accessibility**: Ensure adequate color contrast and readable font sizes
- **Match existing patterns**: Follow the established CSS structure and naming conventions

### Testing and Validation
- Preview changes using Jekyll local server: `bundle exec jekyll serve`
- Test on GitHub Pages preview before merging
- Verify navigation links work correctly (remember .html extension)
- Check responsive behavior at mobile, tablet, and desktop widths
- Ensure hover effects work smoothly

## Boundaries and Constraints

### Never Do
- Remove or significantly alter the retro design aesthetic
- Change the fundamental color palette (pink, beige, brown)
- Modify the candy-striped background pattern
- Break existing navigation between pages
- Add external dependencies or frameworks
- Introduce JavaScript (keep it pure HTML/CSS/Markdown)
- Commit large binary files or build artifacts

### Always Do
- Preserve the vintage charm and nostalgic feel
- Keep designs simple and focused on content
- Maintain fast page load times (no heavy assets)
- Use semantic HTML where possible
- Keep CSS organized and commented when necessary
- Test changes in a local Jekyll environment before committing

## Common Tasks

### Adding a New Menu Item
1. Follow the existing `.flavour-card` structure
2. Use CSS gradients for background colors
3. Include emoji in the flavor name
4. Price in format `$X.XX`
5. Add semi-transparent emoji overlay on the flavor image

### Creating a New Page
1. Start with YAML frontmatter
2. Copy the standard `<style>` block and customize as needed
3. Include logo header: `<div class="logo-header"><img src="logo.png" alt="..."></div>`
4. Add navigation links at the bottom
5. Maintain the `.container` wrapper structure

### Modifying Styles
1. Keep changes within existing `<style>` blocks
2. Maintain the established color variables (use existing hex codes)
3. Preserve responsive grid patterns
4. Test hover effects and transitions

## Examples

### Good Flavor Card Structure
```html
<div class="flavour-card">
  <div class="flavour-name">🍦 Vanilla Bean Dream</div>
  <div class="flavour-image" style="background: linear-gradient(135deg, #FFF8DC, #FFFACD);">
    <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); font-size: 50px; opacity: 0.3;">👨</div>
  </div>
  <div class="price">$6.50</div>
</div>
```

### Good Navigation Pattern
```html
<div class="nav-links">
  <a href="index.html">Home</a>
  <a href="1.html">Page 1</a>
  <a href="2.html">Page 2</a>
</div>
```

## Project Context

This is a **proof-of-concept** demonstrating how to create an attractive, themed static website using only markdown, HTML, and CSS. The focus is on:

- Showcasing design creativity within GitHub Pages constraints
- Demonstrating CSS Grid and modern layout techniques
- Creating a cohesive visual experience with pure CSS
- Proving that simple tech stacks can create compelling results

The project celebrates retro design aesthetics and the charm of classic ice cream parlors from the 1960s-1980s era.
