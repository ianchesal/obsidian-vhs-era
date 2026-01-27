# VHS Era Obsidian Theme Development Guide

## Project Overview

This is an Obsidian theme that adapts the VHS Era color scheme (originally from a Neovim theme) to the LYT-Mode Obsidian theme structure. The goal is to bring the retro, high-contrast VHS aesthetic to Obsidian note-taking.

## Color Palette Reference

### VHS Era Dark Mode Colors

**Base Colors:**
- Background: `#161616`
- Float Background: `#131313`
- Foreground: `#f2f4f8`
- Cursor: `#ffffff`
- Selection: `#525252`
- Active Line: `#242424`
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

### VHS Era Light Mode Colors

**Base Colors:**
- Background Primary: `#e8e5d8` (darker warm cream - better text contrast)
- Background Secondary: `#e0ddd0` (darker cream)
- Background Tertiary: `#d8d5c8` (warm depth)
- Foreground: `#1a1a1a` (nearly black)
- Muted Text: `#5a5a5a` (medium gray)
- Selection: `#d0cdc0` (warm gray)
- Active Line: `#e0ddd0` (subtle highlight)
- Search: `#c8c5b8` (warm highlight)

**Accent Colors (darkened for light backgrounds):**
- Primary Blue: `#4a7fd6`
- Property Blue: `#1a8fd6`
- Light Blue: `#4a9fd6`
- Cyan: `#1a9d9b`
- Attribute Cyan: `#067a78`
- Pink: `#d63582`
- Parameter Pink: `#c72a70`
- Purple: `#8b65d6`
- Green: `#2a9650`
- Yellow: `#b88a00` (amber/gold)

**Design Philosophy:**
- Warm, cream-toned backgrounds for retro aesthetic (not stark white)
- Eye-catching, vibrant accent colors that maintain readability on light backgrounds
- Same color families as dark mode but adjusted for brightness and contrast

## Theme Architecture

### File Structure
- `manifest.json` - Theme metadata (name, version, author)
- `theme.css` - Complete stylesheet with all styling (includes merged obsidian.css content)
- `publish.css` - Styles for Obsidian Publish
- `README.md` - Installation, usage, and credits
- `showcase-large.png` - Full-size theme showcase screenshot
- `cover.png` - 512x288 thumbnail for theme gallery submission

**Note:** The legacy `obsidian.css` file has been merged into `theme.css` to follow modern Obsidian theme conventions.

### Color Mapping Strategy

**Background System:**
- Main content area (markdown editor): `#242424` (color-base-20) - Lighter for better readability
- Sidebars/UI elements: `#161616` (VHS Era bg) - Darker for visual distinction
- Float/modal backgrounds: `#131313` (VHS Era float bg)
- Base color scale: `#131313` → `#161616` → `#242424` → `#353535` → `#525252`

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
- Selection: `#525252` (dark mode), `#d0cdc0` (light mode)
- Active Line: `#242424` (dark mode), `#e0ddd0` (light mode)
- Search highlights: `#484848`
- Active tabs: Cyan text (`#3ddbd9`) with 2px cyan border
- Sidebar active items: Cyan with border on hover
- H1: Pink (`#ff7eb6`)
- H2: Cyan (`#3ddbd9`) with 0.75em bottom margin
- H3: Purple (`#be95ff`)
- H4: Light Blue (`#82cfff`)
- H5: Green (`#42be65`)
- H6: Yellow (`#ffcc66`)
- Code blocks: Float background (`#131313`)
- Inline code: Themed with syntax colors
- Syntax highlighting: Use VHS Era syntax colors

## Implemented Features

### Custom Task Checkbox Icons
The theme includes 20+ custom checkbox icons using SVG data URIs and webkit-mask-image:
- `[!]` - Important (yellow)
- `[?]` - Question (cyan)
- `[*]` - Star/priority (yellow)
- `[n]` - Note (pink)
- `[l]` - Location (pink)
- `[i]` - Information (blue)
- `[S]` - Savings (green)
- `[I]` - Idea (yellow)
- `[p]` - Pro (green)
- `[c]` - Con (pink)
- `[b]` - Bookmark (pink)
- `[f]` - Fire/urgent (red)
- `[w]` - Win (purple)
- `[k]` - Key point (yellow)
- `[d]` - Down/declining (pink)
- And more...

### Styled Callout Boxes
All Obsidian callouts have themed styling with:
- Colored left borders (4px)
- Tinted background colors using rgba with 0.1 alpha
- Matching title colors
- Supported types: note, tip, warning, success, danger, info, example, quote, bug, etc.

### Enhanced UI Elements
- **Tab styling**: Active tabs use cyan text with colored borders
- **Sidebar**: Larger text (1.15em) with improved spacing and cyan hover states
- **Search results**: Cyan file titles with yellow highlighted matches
- **H2 spacing**: 0.75em bottom margin for better content separation
- **Background contrast**: Main editor area lighter (#242424), sidebars darker (#161616)

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
1. Modify color variables or styling in `theme.css`
2. Run `./sync-to-vault.sh` to sync changes to test vault (if available)
3. Restart Obsidian or switch themes to see changes
4. Test in different view modes (Reading, Live Preview, Source)
5. Verify sidebar, tabs, and main content area styling
6. Update version in `manifest.json` for releases
7. Update screenshots if visual changes are significant
8. Commit changes with descriptive messages

## Theme Submission

The theme is ready for submission to the Obsidian Community Themes gallery:

1. Repository: `ianchesal/obsidian-vhs-era`
2. Required files in place:
   - `manifest.json` with metadata
   - `theme.css` with all styling
   - `cover.png` (512x288) for gallery thumbnail
   - `README.md` with documentation
3. Follow modern Obsidian conventions (no legacy `obsidian.css`)
4. Screenshots showcase all major features

Submission process:
- Fork `obsidianmd/obsidian-releases`
- Add entry to `community-css-themes.json`
- Create pull request

## Known Considerations

- Theme supports both dark and light modes
  - Dark mode: High-contrast VHS aesthetic with dark backgrounds
  - Light mode: Warm, cream-toned backgrounds with retro feel and eye-catching accent colors
- VHS Era colors optimized for high contrast and retro aesthetic
- Some third-party plugins may need additional styling
- Custom checkbox icons use webkit-mask-image (may not work in all browsers)
- PDF exports use Obsidian's default styling
