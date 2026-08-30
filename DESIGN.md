---
name: Ghost Feed Experimental Forensic
colors:
  surface: '#131318'
  surface-dim: '#131318'
  surface-bright: '#39393f'
  surface-container-lowest: '#0d0e13'
  surface-container-low: '#1b1b21'
  surface-container: '#1f1f25'
  surface-container-high: '#29292f'
  surface-container-highest: '#34343a'
  on-surface: '#e4e1e9'
  on-surface-variant: '#c8c5cb'
  inverse-surface: '#e4e1e9'
  inverse-on-surface: '#303036'
  outline: '#929095'
  outline-variant: '#47464b'
  surface-tint: '#c8c5cb'
  primary: '#c8c5cb'
  on-primary: '#303034'
  primary-container: '#0b0b0f'
  on-primary-container: '#7b797e'
  inverse-primary: '#5f5e63'
  secondary: '#cac6be'
  on-secondary: '#31302b'
  secondary-container: '#484740'
  on-secondary-container: '#b8b5ad'
  tertiary: '#ffb3ac'
  on-tertiary: '#680008'
  tertiary-container: '#220001'
  on-tertiary-container: '#ea2b2f'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#e4e1e7'
  primary-fixed-dim: '#c8c5cb'
  on-primary-fixed: '#1b1b1f'
  on-primary-fixed-variant: '#47464b'
  secondary-fixed: '#e6e2d9'
  secondary-fixed-dim: '#cac6be'
  on-secondary-fixed: '#1c1c16'
  on-secondary-fixed-variant: '#484740'
  tertiary-fixed: '#ffdad6'
  tertiary-fixed-dim: '#ffb3ac'
  on-tertiary-fixed: '#410003'
  on-tertiary-fixed-variant: '#930010'
  background: '#131318'
  on-background: '#e4e1e9'
  surface-variant: '#34343a'
typography:
  data-lg:
    fontFamily: JetBrains Mono
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.05em
  data-md:
    fontFamily: JetBrains Mono
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.2'
    letterSpacing: 0.02em
  data-sm:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '400'
    lineHeight: '1.4'
    letterSpacing: 0.1em
  narrative-lg:
    fontFamily: Fira Sans
    fontSize: 22px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: '0'
  narrative-md:
    fontFamily: Fira Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: 0.01em
  narrative-sm:
    fontFamily: Fira Sans
    fontSize: 14px
    fontWeight: '300'
    lineHeight: '1.5'
    letterSpacing: 0.01em
  data-lg-mobile:
    fontFamily: JetBrains Mono
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.1'
spacing:
  unit: 4px
  gutter: 24px
  margin-safe: 40px
  section-gap: 80px
  col-span-1: calc(100% / 12)
---

## Brand & Style

The design system is built to evoke a clinical, forensic atmosphere—a digital autopsy of unseen data. It targets an audience seeking an unsettling, high-fidelity experience that feels less like a social feed and more like a terminal monitoring "ghost" activity.

The aesthetic combines **Minimalism** with **HUD-inspired technicality**. It prioritizes extreme clarity, heavy whitespace, and rigid structural alignment. Visual interest is derived from data density and precise typographic scales rather than decoration. There are no photographs, illustrations, or decorative icons; the UI is the content.

## Colors

The palette is restricted to three functional tiers to maintain a sterile, high-contrast environment:

- **Surface (#0B0B0F):** A near-black foundation that suggests an infinite digital void. Use for all primary backgrounds.
- **Content (#F5F1E8):** A warm, parchment-like off-white. This is the "human" element of the design, used for all narrative text and primary UI borders.
- **Data (#FF3B3B):** A sharp alarm-red. This is reserved exclusively for volatile data, active alerts, "ghost" metrics, and critical readouts. It should never be used for aesthetic purposes—only for information that is "active" or "unstable."

## Typography

This design system utilizes a binary typographic system to represent the tension between "Machine" and "Human."

- **The Machine (JetBrains Mono):** Used for all metrics, timestamps, coordinates, and technical labels. It must feel rigid and unsympathetic. Always use uppercase for `data-sm` labels to mimic terminal outputs.
- **The Human (Fira Sans):** Used for narrative descriptions, user logs, and witness accounts. The humanist qualities of the font provide a fragile contrast to the cold monospace data surrounding it.

All typography should be rendered with `subpixel-antialiasing` for maximum sharpness against the dark background.

## Layout & Spacing

The layout follows a **Fixed 12-Column Grid** on desktop (1280px max-width) and a **Fluid 4-Column Grid** on mobile. 

- **Alignment:** Elements should align to a strict 4px baseline grid. 
- **Whitespace:** Use generous, almost uncomfortable amounts of whitespace between narrative blocks to create a sense of isolation. 
- **The "HUD" Frame:** The outer edges of the viewport should contain fixed "safe area" margins (40px) that house persistent technical data (e.g., current time, coordinate drift, connection status).
- **Asymmetry:** Narrative text should often be offset (e.g., spanning columns 3 through 9) while technical data clings to the grid edges.

## Elevation & Depth

This design system rejects traditional shadows and material depth. It is a strictly 2D forensic interface.

- **Flat Layering:** Depth is conveyed through **Low-contrast outlines** (#24242A) and opacity shifts. 
- **The Scanline Overlay:** A subtle, fixed-position background pattern of horizontal lines (1px height, 4px apart, 3% opacity) can be used to simulate a monitor surface.
- **Tonal Tiers:** Use a slightly lighter neutral (#16161D) for "container" areas, but never use blurs or soft shadows. All transitions between surfaces must be immediate and sharp.

## Shapes

The shape language is **strictly geometric and sharp**. 

- **Corners:** Every element (buttons, input fields, containers) must have a 0px border radius. 
- **Lines:** Use 1px "hairline" borders for all containers. 
- **Technical Accents:** Use 45-degree clipped corners (dog-ears) for active state indicators or "ghost" detection windows to reinforce the HUD aesthetic.

## Components

- **Action Triggers (Buttons):** Transparent backgrounds with a 1px #F5F1E8 border. On hover, the background fills with #F5F1E8 and the text flips to #0B0B0F. No transitions; the state change should be instantaneous.
- **Data Feed (Cards):** No background fill. A top 1px hairline border in #24242A separates feed items. Narrative text sits on the left; red #FF3B3B monospace metrics sit on the far right.
- **Input Fields:** A single 1px bottom border in #F5F1E8. The cursor should be a solid, blinking block (not a line) to mimic a command-line interface.
- **Technical Readouts (Chips):** Small #FF3B3B text enclosed in brackets: `[ SIGNAL_STRENGTH: 04% ]`. No background fill.
- **Status Indicators:** Small 4px x 4px squares. Static is #F5F1E8; "detected" or "ghost" presence is #FF3B3B with a rapid 100ms blink rate.
- **Crosshairs:** A persistent, subtle crosshair at the center of the viewport or following the cursor, acting as a "targeting" or "focus" element for the forensic experience.