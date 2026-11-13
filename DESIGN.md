---
version: alpha
colors:
  ink: '#153e48'
  ocean: '#dff3f5'
  teal: '#087c78'
  paper: '#f8faf6'
  orange: '#f4ad55'
  lavender: '#eee9fc'
typography:
  display:
    fontFamily: 'Malgun Gothic, sans-serif'
  body:
    fontFamily: 'Malgun Gothic, sans-serif'
  utility:
    fontFamily: 'Consolas, monospace'
rounded:
  card: '24px'
  control: '16px'
spacing:
  unit: '8px'
components:
  Button:
    minHeight: '52px'
---
# Our little world
## Overview
A Korean children's travel atlas, built for Galaxy tablets. Product register. The signature is a real world map paired with a collectible passport and real documentary photographs, rather than a generic dashboard or a worksheet. Warm orange route markers contrast with calm blue water. Avoid babyish clutter and competitive countdowns.
## Colors
Runtime source: app.css :root variables --ink, --ocean, --teal, --paper, --orange, --lavender map directly to the six values above. Use dark ink for text, teal for actions, orange for itinerary accents. Success and error include words, not color alone.
## Typography
Local Korean-capable system fonts; no remote font dependency. Display is heavy with restrained tracking; body is at least 16px and 1.65 line-height. Utility labels use monospace. Use two typographic roles without shipping an unnecessary font.
## Layout
Max width 1440px. Tablet landscape: map beside destination card. Under 900px stack panels. Under 600px use two-column country/answer grids and horizontally scrollable navigation. Buttons >=52px, no hover-only interactions. Country list is the accessible alternative to small map markers.
## Elevation & Depth
Quiet white cards, thin gray-green borders, shallow shadow on map pins and floating nav only.
## Shapes
24px cards, 16px controls, round map markers. Country flags retain their 4:3 asset ratio and use contain, never emoji or crop.
## Components
Native buttons, select and dialog. Shared map, choices, feedback and travel-card renderers in app.js own recurring behavior. Global visible scrollbar. In-flow loading and feedback preserve layout. Respect reduced motion.
## Do's and Don'ts
Use a location and season with packing questions. Distinguish traditional homes from everyday present-day housing. Teach representative examples without describing a whole culture as one thing. Use actual photographs for food, homes and heritage. Each photograph has a full-image modal and visible creator/source/license attribution. Keep house forms uncropped in thumbnails; the enlargement always shows the entire photo.

Map controls reuse the existing rounded white buttons and teal/ocean palette. Touch targets are at least 48px. Zoom stays local to the map; page scrolling remains available outside it.
