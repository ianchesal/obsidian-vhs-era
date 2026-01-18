# VHS Era Obsidian Theme Development Guide

## Project Overview

This is an Obsidian theme that adapts the VHS Era color scheme (originally from a Neovim theme) to the LYT-Mode Obsidian theme structure. The goal is to bring the retro, high-contrast VHS aesthetic to Obsidian note-taking.

## Color Palette Reference

### VHS Era Core Colors

**Base Colors:**
- Background: `#161616`
- Float Background: `#131313`
- Foreground: `#f2f4f8`
- Cursor: `#ffffff`
- Selection: `#353535`
- Search: `#484848`
- Comment: `#525252`

**Syntax/Accent Colors:**
- Primary Blue: `#78a9ff`
- Cyan: `#3ddbd9`
- Attribute Cyan: `#08bdba`
- Property Blue: `#33b1ff`
- Light Blue: `#82cfff`
- Pink/Error: `#ff7eb6`
- Parameter Pink: `#ee5396`
- Purple: `#be95ff`
- Green: `#42be65`
- Yellow: `#ffcc66`
- White: `#ffffff`

## Theme Architecture

### File Structure
- `manifest.json` - Theme metadata (name, version, author)
- `theme.css` - Main stylesheet with color variables and base styling
- `obsidian.css` - Obsidian-specific UI element styling
- `publish.css` - Styles for Obsidian Publish
- `snippets/` - Optional CSS snippets for additional customization
- `README.md` - Installation, usage, and credits

### Color Mapping Strategy

**Background System:**
- Primary background: `#161616` (VHS Era bg)
- Secondary background: `#131313` (VHS Era float bg)
- Use grays from `#161616` → `#525252` for base color scale

**Foreground/Text:**
- Primary text: `#f2f4f8` (VHS Era fg)
- Muted text: `#525252` (VHS Era comment)
- White/bright text: `#ffffff`

**Accent Color Families (LYT-Mode Structure):**
- **Cyan family** → VHS Era cyans (`#3ddbd9`, `#08bdba`, `#33b1ff`, `#82cfff`)
- **Blue/Primary** → VHS Era blue (`#78a9ff`)
- **Magenta/Pink** → VHS Era pinks (`#ff7eb6`, `#ee5396`)
- **Purple** → VHS Era purple (`#be95ff`)
- **Green** → VHS Era green (`#42be65`)
- **Yellow** → VHS Era yellow (`#ffcc66`)

**UI Element Assignments:**
- Links: Primary Blue (`#78a9ff`)
- Selection: `#353535`
- Search highlights: `#484848`
- H1: Pink (`#ff7eb6`)
- H2: Cyan (`#3ddbd9`)
- H3: Purple (`#be95ff`)
- H4: Light Blue (`#82cfff`)
- H5: Green (`#42be65`)
- H6: Yellow (`#ffcc66`)
- Code blocks: Float background (`#131313`)
- Syntax highlighting: Use VHS Era syntax colors

## Development Guidelines

### Color Usage
- **Maintain exact hex values** from VHS Era for now
- Generate intermediate shades using HSL manipulation when needed for hover states
- Keep high contrast between background and foreground
- Use muted comment color (`#525252`) for less important UI elements

### Testing Approach
1. Test in both Light and Dark mode (theme is dark-focused)
2. Verify readability of all heading levels
3. Check link visibility and hover states
4. Test code block syntax highlighting
5. Verify selection and search highlighting
6. Test with common plugins (Dataview, Calendar, Kanban, Excalidraw)
7. Check both Live Preview and Reading modes

### Obsidian-Specific Considerations
- Use CSS variables for all colors (Obsidian's theming system)
- Support both Legacy Editor and Live Preview
- Consider mobile app rendering
- Test with various plugin UIs
- Ensure accessibility (contrast ratios)

## Credits & Attribution

This theme is derived from:
1. **VHS Era Neovim Theme** by Mistweaver Co.
   - GitHub: https://github.com/mistweaverco/vhs-era-theme.nvim
   - Original color scheme and aesthetic

2. **LYT-Mode Obsidian Theme** by Nick Milo
   - GitHub: https://github.com/nickmilo/LYT-Mode
   - Theme structure and CSS architecture

## Development Workflow

When making changes:
1. Modify color variables in `theme.css` first
2. Test changes in Obsidian (requires reload)
3. Update `obsidian.css` for specific UI adjustments
4. Document any color tweaks or adjustments
5. Update version in `manifest.json` for releases

## Known Considerations

- VHS Era is optimized for code, Obsidian is for prose - some color choices may need adjustment
- Obsidian has many UI elements not present in terminal editors
- Plugin compatibility may require additional styling
- Consider creating a light theme variant in the future
