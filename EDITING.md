# Customer Editing Guide — Suvidha & Shivendra Wedding Invitation (ever-after-bloom)

Hand-painted watercolour storybook invitation featuring an animated wax seal video opener, couple portraits, live countdown timer, wedding function schedule (Flower Haldi & Barat), Aditya Palace venue details, interactive lantern wishes, and calendar links.

---

## Wedding Overview

- **Bride**: Suvidha
- **Groom**: Shivendra
- **Wedding Date**: Saturday, 21 November 2026
- **Venue**: Aditya Palace

---

## Functions Itinerary

1. **Flower Haldi**: 21st November 2026 · 11:00 AM (Morning)
   - Venue: Aditya Palace
2. **Barat Procession**: 21st November 2026 · 7:00 PM (Evening)
   - Venue: Aditya Palace

---

## Normal Customer Changes

All routine customer edits are configured in:
→ `editable/wedding-data.js`

### 1. Couple Names & Initials
Edit `couple` in `editable/wedding-data.js`:
- `bride`: Bride's first name (`"Suvidha"`)
- `groom`: Groom's first name (`"Shivendra"`)
- `initials`: Monogram text on seal and hero (`"S & S"`)

### 2. Wedding Date & Times
Edit in `editable/wedding-data.js`:
- `dateISO`: ISO timestamp string (`2026-11-21T11:00:00+05:30`) used for calendar buttons & reminders
- `dateLabel`: Formatted date (`"Saturday, 21 November 2026"`)
- `timeLabel`: Formatted time (`"Flower Haldi: 11:00 AM · Barat: 7:00 PM"`)
- `dressCode`: Dress code guidance (`"Festive Indian Attire"`)

### 3. Hero & Story
Edit in `editable/wedding-data.js`:
- `hero.kicker`: Opening line above couple names
- `hero.eyebrow`: Subtitle badge
- `hero.blessing`: Poetic blessing line
- `story.title` / `story.subtitle`: Section titles
- `story.bride`: Bride name, role, and story bio
- `story.groom`: Groom name, role, and story bio

### 4. Story Chapters
Edit `chapters` array in `editable/wedding-data.js`:
- Each item has `no` (e.g. `"I"`), `title`, `when`, and narrative `text`.

### 5. Venue & Map
Edit `venue` in `editable/wedding-data.js`:
- `name`: Palace or venue name (`"Aditya Palace"`)
- `address`: Street address
- `mapsQuery`: Search term for Google Maps directions (`"Aditya Palace"`)

### 6. Footer
Edit `footer` in `editable/wedding-data.js`:
- `line1`, `line2`, and `signoff` text

### 7. Images & Video
Replace files in `editable/assets/` or update paths in `wedding-data.js`:
- `seal`: Wax seal artwork (`invite-seal.png`)
- `openVideo`: Seal opening animation video (`invite-open.mp4`)
- `portraitBride` & `portraitGroom`: Couple watercolour portraits
- `heroPalace` & `gardenCourtyard`: Venue background artwork
- `mapPlate`: Illustrated map illustration
- `sceneDancing`, `sceneWalking`, etc.: Illustrated chapter scenes

---

## Validation
Validate syntax after editing:
```bash
node --check editable/wedding-data.js
```
