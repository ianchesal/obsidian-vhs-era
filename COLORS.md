# VHS Era Color Palette Reference

This document contains all colors extracted from the VHS Era Neovim theme for reference during development.

## Base Colors

| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Background | `#161616` | Primary background |
| Float Background | `#131313` | Secondary/floating backgrounds |
| Foreground | `#f2f4f8` | Primary text color |
| Cursor | `#ffffff` | Cursor/white accents |
| Selection | `#353535` | Selected text background |
| Search | `#484848` | Search highlight background |
| Comment | `#525252` | Muted/secondary text |

## Accent Colors

### Blues
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Primary Blue | `#78a9ff` | Keywords, primary accent |
| Property Blue | `#33b1ff` | Properties, methods |
| Light Blue | `#82cfff` | Numbers, hints |

### Cyans/Aquas
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Cyan | `#3ddbd9` | Punctuation, tags |
| Attribute Cyan | `#08bdba` | Attributes, labels |

### Pinks/Magentas
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Pink | `#ff7eb6` | Methods, errors |
| Parameter Pink | `#ee5396` | Parameters, diff delete |

### Purples
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Purple | `#be95ff` | Strings, warnings |

### Greens
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Green | `#42be65` | Constants, diff add, success |

### Yellows
| Color Name | Hex Value | Usage |
|------------|-----------|-------|
| Yellow | `#ffcc66` | Diff change, attention |

## Color Groups for Obsidian Mapping

### Background Spectrum (Dark to Light)
```
#131313 → #161616 → #353535 → #484848 → #525252
```

### Foreground Spectrum (Bright to Muted)
```
#ffffff → #f2f4f8 → #525252
```

### Accent Palette (Vibrant)
```
Blue:   #78a9ff, #33b1ff, #82cfff
Cyan:   #3ddbd9, #08bdba
Pink:   #ff7eb6, #ee5396
Purple: #be95ff
Green:  #42be65
Yellow: #ffcc66
White:  #ffffff
```

## Suggested Heading Hierarchy

- H1: `#ff7eb6` (Pink - highest emphasis)
- H2: `#3ddbd9` (Cyan - strong emphasis)
- H3: `#be95ff` (Purple - medium emphasis)
- H4: `#82cfff` (Light Blue - moderate emphasis)
- H5: `#42be65` (Green - subtle emphasis)
- H6: `#ffcc66` (Yellow - minimal emphasis)

## UI Element Recommendations

- **Links**: `#78a9ff` (Primary Blue)
- **Link Hover**: `#82cfff` (Light Blue)
- **Buttons**: `#78a9ff` (Primary Blue)
- **Active Elements**: `#3ddbd9` (Cyan)
- **Tags**: `#be95ff` (Purple)
- **Checkboxes**: `#42be65` (Green when checked)
- **Highlights**: `#ffcc66` (Yellow)
- **Errors**: `#ff7eb6` (Pink)
- **Success**: `#42be65` (Green)
- **Code Inline**: `#ee5396` (Parameter Pink)
- **Code Block BG**: `#131313` (Float Background)

## Accessibility Notes

All color combinations should be tested for WCAG contrast ratios:
- Text on `#161616` background should use light colors (`#f2f4f8` or brighter)
- Interactive elements should have clear hover states
- Links should be distinguishable from regular text
